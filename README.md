#include <stdio.h>

int main() {
    double num1, num2, result;
    char op;

    printf("Birinci sayıyı girin: ");
    scanf("%lf", &num1);

    printf("İkinci sayıyı girin: ");
    scanf("%lf", &num2);

    printf("İşlemi seçin (+, -, *, /): ");
    scanf(" %c", &op);

    switch (op) {
        case '+':
            result = num1 + num2;
            printf("Sonuç: %.2lf\n", result);
            break;
        case '-':
            result = num1 - num2;
            printf("Sonuç: %.2lf\n", result);
            break;
        case '*':
            result = num1 * num2;
            printf("Sonuç: %.2lf\n", result);
            break;
        case '/':
            if (num2 == 0)
                printf("Hata: Sıfıra bölme yapılamaz!\n");
            else {
                result = num1 / num2;
                printf("Sonuç: %.2lf\n", result);
            }
            break;
        default:
            printf("Geçersiz işlem!\n");
    }

    return 0;
}
