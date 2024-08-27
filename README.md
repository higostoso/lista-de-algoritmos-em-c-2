# lista-de-algoritmos-em-c-2
11- numeros primos
#include <stdio.h>
#include <math.h>


int main () {
   
   int numero = 1;
   
   printf("digite um numero:\n");
   scanf("%d", &numero);
   
   if (numero <= 1) {
printf("esse numero nao e primo.\n");
return 0;
}

if (numero == 2){
printf("esse numero e primo\n");
return 0;
}

if (numero % 2 == 0) {
	printf("esse numero e divisivel por dois, portanto não é primo.\n");
	return 0;
	
}

    printf("esse numero e primo.\n");
    return 0;
   	
}
12- Soma dos Números Naturais
#include <stdio.h>

int main () {
	
	int N;
	
	printf("digite o valor de N:\n");
	scanf("%d", &N);
	
  if (N < 1) {
  	printf("N deve ser um numero natural! (N >= 1).\n");
  	return 1;
	}
	
	int soma = N * (N + 1)/2;
	 
	printf("esse e o resultado da soma %d desses numeros naturais: %d\n", N, soma);
	
	return 0;
	
}
13- Fibonacci
#include <stdio.h>

int main() {
    int N;
    
    printf("Digite o número de termos da sequência de Fibonacci: ");
    scanf("%d", &N);

    if (N <= 0) {
        printf("O número de termos deve ser positivo.\n");
        return 1;
    }

    unsigned long long int a = 0, b = 1, c;

    printf("Sequência de Fibonacci com %d termos:\n", N);
    for (int i = 0; i < N; i++) {
        if (i == 0) {
            printf("%llu ", a);
        } else if (i == 1) {
            printf("%llu ", b);
        } else {
            c = a + b;
            a = b;
            b = c;
            printf("%llu ", c);
        }
    }
    printf("\n");

    return 0;
}
14- Numeros Invertidos

#include <stdio.h>

int main() {
    int numero, numeroInvertido = 0, resto;

    printf("Digite um número para inverter os dígitos: ");
    scanf("%d", &numero);

    int numeroOriginal = numero;

    while (numero != 0) {

        resto = numero % 10;

        numeroInvertido = numeroInvertido * 10 + resto;
        numero /= 10;
    }


    printf("Número original: %d\n", numeroOriginal);
    printf("Número invertido: %d\n", numeroInvertido);

    return 0;
}
15- Cauculo de Potencia

#include <stdio.h>

int main() {
    double base;
    int expoente;

    printf("Digite a base: ");
    scanf("%lf", &base);
    printf("Digite o expoente: ");
    scanf("%d", &expoente);

    double resultado = (base * expoente);

    printf("%.2lf elevado a %d é %.2lf.\n", base, expoente, resultado);

    return 0;
}
16- Palindromo


