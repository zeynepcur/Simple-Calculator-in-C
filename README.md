A simple C program takes two numbers and an operator (+, -, *, /) from the user, then shows the result of the operation.

```c
#include <stdio.h>
int main() {
    double num1, num2, result;
    char op;

    printf("Enter the first number: ");
    scanf("%lf", &num1);

    printf("Enter the second number: ");
    scanf("%lf", &num2);

    printf("Select the operation (+, -, *, /): ");
    scanf(" %c", &op);

    switch (op) {
        case '+':
            result = num1 + num2;
            printf("Result: %.2lf\n", result);
            break;
        case '-':
            result = num1 - num2;
            printf("Result: %.2lf\n", result);
            break;
        case '*':
            result = num1 * num2;
            printf("Result: %.2lf\n", result);
            break;
        case '/':
            if (num2 == 0)
                printf("Error: division by zero is not allowed!\n");
            else {
                result = num1 / num2;
                printf("Result: %.2lf\n", result);
            }
            break;
        default:
            printf("İnvalid Operation!\n");
    }

    return 0;
}
