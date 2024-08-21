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
