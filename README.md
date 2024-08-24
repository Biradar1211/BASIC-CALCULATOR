# BASIC-CALCULATOR
#include <stdio.h>

int main() {
    char operation;
    float num1, num2, result;

    printf("Basic Calculator\n");
    printf("Enter operation (+, -, *, /): ");
    scanf(" %c", &operation);

    printf("Enter two numbers: ");
    scanf("%f %f", &num1, &num2);

    switch (operation) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            if (num2 != 0) {
                result = num1 / num2;
            } else {
                printf("Error: Division by zero!\n");
                return 1;
            }
            break;
        default:
            printf("Invalid operation!\n");
            return 1;
    }

    printf("Result: %.2f\n", result);

    return 0;
}
