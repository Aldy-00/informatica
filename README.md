#include <stdio.h>

int main() {
    float peso, altura, bmi;

    printf("Ingrese el peso en kg: ");
    if (scanf("%f", &peso) != 1 || peso <= 0) {
        printf("Error: El peso  no es valido.\n");
        return 1;
    }
    printf("Ingrese la altura en metros: ");
    if (scanf("%f", &altura) != 1 || altura <= 0) {
        printf("Error: La altura  no es valida.\n");
        return 1;
    }
    bmi = peso / (altura * altura);
  
    printf("\nSu indice de masa corporal es: %.2f\n\n", bmi);
    printf("    Indice     |  Condicion\n");
    printf("-----------------------------\n");
    printf("    <18.5 |  Bajo peso\n");
    printf(" 18.5 a 24.9 |  Normal\n");
    printf(" 25.0 a 29.9 |  Sobrepeso\n");
    printf("     >=30 |  Obesidad\n");

    return 0;
}
