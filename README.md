# soma,subtração, mutiplicação e divisão em linguagem C
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "portuguese");

    float num1, num2, resultado;
    char op;

    printf("Digite os dois números: ");
    scanf("%f %f", &num1, &num2);

    getchar();  // Limpa o '\n' que sobrou no buffer

    printf("Digite a operação (+, -, *, /): ");
    scanf("%c", &op);

    switch(op) {
        case '+':
            resultado = num1 + num2;
            printf("O resultado é: %f\n", resultado);
            break;

        case '-':
            resultado = num1 - num2;
            printf("O resultado é: %f\n", resultado);
            break;

        case '*':
            resultado = num1 * num2;
            printf("O resultado é: %f\n", resultado);
            break;

        case '/':
            if (num2 == 0) {
                printf("Denominador inválido\n");
            } else {
                resultado = num1 / num2;
                printf("O resultado é: %f\n", resultado);
            }
            break;

        default:
            printf("Operação inválida\n");
            break;
    }

    return 0;
}
