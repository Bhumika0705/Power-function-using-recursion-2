# Power-function-using-recursion-2
power function using recursion in java
import java.util.Scanner;

public class Powerbyrecurr2 {
    public Powerbyrecurr2() {
    }

    static int func(int a, int b) {
        if (b == 0) {
            return 1;
        } else {
            int result;
            if (b % 2 == 0) {
                result = func(a, b / 2);
                return result * result;
            } else {
                result = func(a, (b - 1) / 2);
                return a * result * result;
            }
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int ans = func(a, b);
        System.out.println(ans);
    }
}
