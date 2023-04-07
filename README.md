# Currency-Convertor
Basic java console
import java.util.Scanner;
public class Main {
    private static final double USD_TO_INR = 75.0;
    private static final double USD_TO_EUR = 0.85;
    private static final double USD_TO_GBP = 0.73;
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Welcome to Currency Converter!");
        System.out.print("Enter the amount in USD: ");
        double amountInUsd = scanner.nextDouble();
        System.out.println("Select the currency to convert to:");
        System.out.println("1. INR");
        System.out.println("2. EUR");
        System.out.println("3. GBP");
        System.out.print("Enter your choice: ");
        int choice = scanner.nextInt();
        double convertedAmount = 0.0;
        String currency = "";
        switch (choice) {
            case 1:
                convertedAmount = amountInUsd * USD_TO_INR;
                currency = "INR";
                break;
            case 2:
                convertedAmount = amountInUsd * USD_TO_EUR;
                currency = "EUR";
                break;
            case 3:
                convertedAmount = amountInUsd * USD_TO_GBP;
                currency = "GBP";
                break;
            default:
                System.out.println("Invalid choice.");
                scanner.close();
                return;
        }
        System.out.println("Amount in " + currency + ": " + convertedAmount + " " + currency);
        scanner.close();
    }
}

