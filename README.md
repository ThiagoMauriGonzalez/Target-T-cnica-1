#include <stdio.h>

int pertenceFibonacci(int n) {
    if (n < 0) {
        return 0;
    }

    int a = 0, b = 1, c = 0;

    while (c < n) {
        c = a + b;
        a = b;
        b = c;
    }

    return (c == n);
}

int main() {
    int num;

    printf("Informe um número: ");
    scanf("%d", &num);

    if (pertenceFibonacci(num)) {
        printf("O número %d pertence à sequência de Fibonacci.\n", num);
    } else {
        printf("O número %d não pertence à sequência de Fibonacci.\n", num);
    }

    return 0;
}
