import java.util.Arrays;
import java.util.Scanner;
import java.util.Random;

public class Project {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String[] ans = RandomNum();

        System.out.println("JAVABET!!");
        System.out.println("---------------------");
        System.out.println("How to play : Guess 4 Number");
        System.out.println("x = Wrong Number \n* = Correct Number BUT Wrong Position");
        System.out.println("---------------------");
        System.out.print("Type 4 number to start.. ");

        for (int k = 0; k < 6; k++) {

            String userinput = sc.nextLine();

            String[] input = userinput.split("");
            boolean[] CorrectPosition = CheckPosition(input, ans);
            boolean[] CorrectNum = CheckNum(input, ans, CorrectPosition);
            String[] result = CheckResult(input, ans, CorrectPosition, CorrectNum);

            if (Arrays.equals(result, ans)) {
                System.out.println(Arrays.toString(result) + " CORRECT ANSWER!!!");
                break;
            } else {
                System.out.println(Arrays.toString(result) + " TRY AGAIN ;-;\n");
            }
        }

        System.out.println("Answer : " + Arrays.toString(ans));

        sc.close();
    }

    public static String[] RandomNum() {
        Random r = new Random();
        String[] ansNum = { "", "", "", "" };
        for (int i = 0; i < 4; i++) {
            ansNum[i] = Integer.toString(r.nextInt(10));
        }
        return ansNum;
    }
    public static boolean[] CheckPosition(String[] input, String[] ans) {
        boolean[] CorrectPosition = { false, false, false, false };
        for (int a = 0; a < 4; a++) {
            if (input[a].equals(ans[a])) {
                CorrectPosition[a] = true;
            }
        }
        return CorrectPosition;
    }

    public static boolean[] CheckNum(String[] input, String[] ans, boolean[] CorrectPosition) {

        boolean[] CorrectNum = { false, false, false, false };

        for (int b = 0; b < 4; b++) {
            for (int c = 0; c < 4; c++) {
                if (input[b].equals(ans[c])) {
                    CorrectNum[b] = true;
                    break;
                }
            }

        }
        return CorrectNum;
    }

    // Check Result
    public static String[] CheckResult(String[] input, String[] ans, boolean[] CorrectPosition, boolean[] CorrectNum) {
        String[] result = { "x", "x", "x", "x" };
        for (int j = 0; j < 4; j++) {
            if (CorrectPosition[j] == true) {
                result[j] = input[j];
            } else if (CorrectNum[j] == true) {
                result[j] = input[j] + "*";
            }
        }
        return result;

    }

}
