# HarshadRR-SE_OOP-assignment--6[ Implement a program to handle Arithmetic exception, Array Index Out of Bounds. The user enters two numbers Num1 and Num2. The division of Num1 and Num2 is
displayed. If Num1 and Num2 are not integers, the program would throw a Number
Format Exception. If Num2 were zero, the program would throw an Arithmetic
Exception. Display the exception]




import java.util.Scanner;
class ExceptionHandlingExample {
public static void main(String[] args) {
Scanner scanner = new Scanner(System.in);
try {
// Input two numbers
System.out.print("Enter the first number (Num1): ");
String input1 = scanner.nextLine();
System.out.print("Enter the second number (Num2): ");
String input2 = scanner.nextLine();
// Convert inputs to integers
int num1 = Integer.parseInt(input1);
int num2 = Integer.parseInt(input2);
// Perform division
int result = num1 / num2;
System.out.println("Result of division: " + result);
// Example of ArrayIndexOutOfBoundsException
int[] array = new int[1];
System.out.println("Accessing array element: " + array[2]); // This will throw
ArrayIndexOutOfBoundsException
} catch (NumberFormatException e) {
System.out.println("Error: Invalid number format. Please enter valid
integers.");
} catch (ArithmeticException e) {
System.out.println("Error: Division by zero is not allowed.");
} catch (ArrayIndexOutOfBoundsException e) {
System.out.println("Error: Array index out of bounds.");
}
}
}
