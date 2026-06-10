# Code-1
#include <stdio.h>
#include <math.h>

int main() {
    int choice;
    double num1, num2, result;

    do {
        printf("\n===== Scientific Calculator =====\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Power (x^y)\n");
        printf("6. Square Root\n");
        printf("7. Logarithm (base 10)\n");
        printf("8. Sine\n");
        printf("9. Cosine\n");
        printf("10. Tangent\n");
        printf("11. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch(choice) {
            case 1:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                printf("Result = %.2lf\n", num1 + num2);
                break;

            case 2:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                printf("Result = %.2lf\n", num1 - num2);
                break;

            case 3:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                printf("Result = %.2lf\n", num1 * num2);
                break;

            case 4:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                if(num2 != 0)
                    printf("Result = %.2lf\n", num1 / num2);
                else
                    printf("Error! Division by zero.\n");
                break;

            case 5:
                printf("Enter base and exponent: ");
                scanf("%lf %lf", &num1, &num2);
                result = pow(num1, num2);
                printf("Result = %.2lf\n", result);
                break;

            case 6:
                printf("Enter a number: ");
                scanf("%lf", &num1);
                if(num1 >= 0)
                    printf("Result = %.2lf\n", sqrt(num1));
                else
                    printf("Error! Negative number.\n");
                break;

            case 7:
                printf("Enter a number: ");
                scanf("%lf", &num1);
                if(num1 > 0)
                    printf("Result = %.2lf\n", log10(num1));
                else
                    printf("Error! Log undefined.\n");
                break;

            case 8:
                printf("Enter angle in degrees: ");
                scanf("%lf", &num1);
                printf("Result = %.2lf\n", sin(num1 * M_PI / 180));
                break;

            case 9:
                printf("Enter angle in degrees: ");
                scanf("%lf", &num1);
                printf("Result = %.2lf\n", cos(num1 * M_PI / 180));
                break;

            case 10:
                printf("Enter angle in degrees: ");
                scanf("%lf", &num1);
                printf("Result = %.2lf\n", tan(num1 * M_PI / 180));
                break;

            case 11:
                printf("Exiting Calculator...\n");
                break;

            default:
                printf("Invalid Choice!\n");
        }

    } while(choice != 11);

    return 0;
}
