# Quadrati
## Esercizio differenza tra quadrati
Questo codice utilizza un ciclo for per calcolare la somma dei primi N numeri e la somma dei quadrati dei primi N numeri. Per calcolare il quadrato della somma, viene utilizzata la formula (1 + 2 + ... + N)^2 = 1^2 + 2^2 + ... + N^2 + 2*1*2 + 2*1*3 + ... + 2*1*N + 2*2*3 + ... + 2*2*N + ... + 2*(N-1)*N. Per calcolare la differenza tra il quadrato della somma e la somma dei quadrati, viene semplicemente sottratta la somma dei quadrati dal quadrato della somma.

```C
#include <stdio.h>

int main() {
    int N, somma = 0, somma_quadrati = 0;
    printf("Inserisci un numero intero positivo N: ");
    scanf("%d", &N);
	int i; 
    // calcola la somma dei primi N numeri
    for (i = 1; i <= N; i++) {
        somma += i;
    }
    int quadrato_somma = somma * somma;
    printf("Il quadrato della somma dei primi %d numeri e' %d.\n", N, quadrato_somma);

    // calcola la somma dei quadrati dei primi N numeri
    for (i = 1; i <= N; i++) {
        somma_quadrati += i * i;
    }
    printf("La somma dei quadrati dei primi %d numeri e' %d.\n", N, somma_quadrati);

    // calcola la differenza tra il quadrato della somma e la somma dei quadrati
    int differenza = quadrato_somma - somma_quadrati;
    printf("La differenza tra il quadrato della somma e la somma dei quadrati dei primi %d numeri e' %d.\n", N, differenza);

    return 0;
}

```
