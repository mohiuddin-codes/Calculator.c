calculator.c
#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;

    // Displaying menu
    printf("Simple Calculator in C\n");
    printf("-----------------------\n");
    printf("Available operations: +  -  *  /\n");

    // Taking operator input
    printf("Enter an operator: ");
    scanf(" %c", &operator);

    // Taking two numbers
    printf("Enter first number: ");
    scanf("%lf", &num1);

    printf("Enter second number: ");
    scanf("%lf", &num2);

    // Performing operation
    switch (operator) {
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
            if (num2 != 0)
                result = num1 / num2;
            else {
                printf("Error: Division by zero is not allowed.\n");
                return 1;
            }
            printf("Result: %.2lf\n", result);
            break;
        default:
            printf("Invalid operator.\n");
    }

    return 0;
}
