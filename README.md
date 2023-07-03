java
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        double num1, num2, result;
        char operator;

        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите первое число: ");
        num1 = scanner.nextDouble();

        System.out.print("Введите второе число: ");
        num2 = scanner.nextDouble();

        System.out.print("Выберите оператор (+, -, *, /): ");
        operator = scanner.next().charAt(0);

        switch (operator) {
            case '+':
                result = num1 + num2;
                System.out.println("Результат: " + result);
                break;
            case '-':
                result = num1 - num2;
                System.out.println("Результат: " + result);
                break;
            case '*':
                result = num1 * num2;
                System.out.println("Результат: " + result);
                break;
            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println("Результат: " + result);
                } else {
                    System.out.println("Ошибка: деление на ноль");
                }
                break;
            default:
                System.out.println("Ошибка: некорректный оператор");
                break;
        }
    }
}
