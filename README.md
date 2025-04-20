import java.util.Scanner;

public class RecursionSum {

    // Recursive method to get the sum of numbers
    public static int getSum(Scanner scanner, int count) {
        if (count == 0) {
            return 0; // base case
        } else {
            System.out.print("Enter a number: ");
            int num = scanner.nextInt(); // read one number
            return num + getSum(scanner, count - 1); // recursive case
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int total = getSum(scanner, 5); // start with 5 numbers
        System.out.println("The sum of the numbers is: " + total);
        scanner.close();
    }
}
