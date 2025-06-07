# Simple-Calculator-in-C
A console-based calculator program that performs basic arithmetic operations: addition, subtraction, multiplication, and division. The user inputs two numbers and selects an operation, then the program outputs the result. Handles division by zero with an error message.

#include <stdio.h>


int main() {
       
    double num1, num2;
    char op;

    printf("Simple Calculator\n");
    printf("Choose an operation (+, -, *, /): ");
    scanf(" %c", &op);

    printf("Enter the first number: ");
    scanf("%lf", &num1);

    printf("Enter the second number: ");
    scanf("%lf", &num2);

    switch (op) {
        case '+':
            printf("Result: %.2lf\n", num1 + num2);
            break;
        case '-':
            printf("Result: %.2lf\n", num1 - num2);
            break;
        case '*':
            printf("Result: %.2lf\n", num1 * num2);
            break;
        case '/':
            if (num2 != 0)
                printf("Result: %.2lf\n", num1 / num2);
            else
                printf("Error: Division by zero is not allowed.\n");
            break;
        default:
            printf("Invalid operation selected.\n");
    }

    return 0;
}
