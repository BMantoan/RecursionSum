import java.util.Scanner;

public class RecursionSum {

    // Recursive method 
    public static int getSum(Scanner scanner, int count) {
        if (count == 0) {
            return 0; // base case
        } else {
            int num;
            while (true) {
                System.out.print("Enter a number: ");
                if (scanner.hasNextInt()) {
                    num = scanner.nextInt();
                    break; // valid input, exit loop
                } else {
                    System.out.println("Invalid input. Please enter a valid number.");
                    scanner.next(); // discard the invalid input
                }
            }
            return num + getSum(scanner, count - 1); // recursive call
        }
    }
    //Try-with-resource
    public static void main(String[] args) {
        try (Scanner scanner = new Scanner(System.in)) {
            int total = getSum(scanner, 5); // ask for 5 numbers
            System.out.println("The sum of the numbers is: " + total);
        }
    }
}
