#include <stdio.h>

int main() {
    int idades[10], i;
    int maisNova, maisVelha;

    // Entrada das idades
    for(i = 0; i < 10; i++) {
        printf("Digite a idade da pessoa %d: ", i + 1);
        scanf("%d", &idades[i]);
    }

    // Inicializar as variáveis com a primeira idade
    maisNova = idades[0];
    maisVelha = idades[0];

    // Encontrar a mais nova e a mais velha
    for(i = 1; i < 10; i++) {
        if(idades[i] < maisNova) {
            maisNova = idades[i];
        }
        if(idades[i] > maisVelha) {
            maisVelha = idades[i];
        }
    }

    // Saída do resultado
    printf("A pessoa mais nova tem %d anos.\n", maisNova);
    printf("A pessoa mais velha tem %d anos.\n", maisVelha);

    return 0;
}
