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
QUESTÃO 16
#include using namespace std;

bool isPalindrome(int num) { int original = num; int invertido = 0;


if (num < 0) {
    return false;
}


while (num > 0) {
    int digito = num % 10;
    invertido = invertido * 10 + digito;
    num /= 10;
}

return original == invertido;
}

int main() { int num;

cout << "Digite um número: ";
cin >> num;

if (isPalindrome(num)) {
    cout << num << " é um palíndromo." << endl;
} else {
    cout << num << " não é um palíndromo." << endl;
}

return 0;
}

17-
#include using namespace std;

int main() { int num1, num2;

cout << "Digite o primeiro número: ";
cin >> num1;

cout << "Digite o segundo número: ";
cin >> num2;

if (num1 < 0 || num2 < 0) {
    cout << "Os números devem ser não-negativos." << endl;
    return 1;
}

int mdc = calcularMDC(num1, num2);

cout << "O Máximo Divisor Comum (MDC) de " << num1 << " e " << num2 << " é: " << mdc << endl;

return 0;
}

1-
#include using namespace std;
int main() { int num1, num2;

cout << "Digite o primeiro número: ";
cin >> num1;

cout << "Digite o segundo número: ";
cin >> num2;

if (num1 < 0 || num2 < 0) {
    cout << "Os números devem ser não-negativos." << endl;
    return 1;
}

int mmc = calcularMMC(num1, num2);

cout << "O Mínimo Múltiplo Comum (MMC) de " << num1 << " e " << num2 << " é: " << mmc << endl;

return 0;
}

19-
#include using namespace std;
int somaDivisores = 0;

for (int i = 1; i <= num / 2; ++i) {
    if (num % i == 0) {
        somaDivisores += i;
    }
}

return somaDivisores == num;
}

int main() { int num;

cout << "Digite um número: ";
cin >> num;

if (isPerfect(num)) {
    cout << num << " é um número perfeito." << endl;
} else {
    cout << num << " não é um número perfeito." << endl;
}

return 0;
}

20-
#include using namespace std;

int main() { int n;

cout << "Digite o número de elementos no vetor: ";
cin >> n;

int* arr = new int[n]; // Cria um vetor dinamicamente

cout << "Digite os elementos do vetor: ";
for (int i = 0; i < n; ++i) {
    cin >> arr[i];
}
bubbleSort(arr, n);

cout << "Vetor ordenado em ordem crescente: ";
exibirVetor(arr, n);

delete[] arr; // Libera a memória alocada para o vetor

return 0;
}

21-
#include using namespace std;
int main() { int n, valor;

cout << "Digite o número de elementos no vetor: ";
cin >> n;

int* arr = new int[n]; // Cria um vetor dinamicamente

cout << "Digite os elementos do vetor: ";
for (int i = 0; i < n; ++i) {
    cin >> arr[i];
}

cout << "Digite o valor a ser buscado: ";
cin >> valor;

int resultado = buscaLinear(arr, n, valor);

if (resultado != -1) {
    cout << "Valor " << valor << " encontrado no índice " << resultado << "." << endl;
} else {
    cout << "Valor " << valor << " não encontrado no vetor." << endl;
}

delete[] arr; // Libera a memória alocada para o vetor

return 0;
}

22-
#include using namespace std;

while (esquerda <= direita) {
    int meio = esquerda + (direita - esquerda) / 2;
    
    if (arr[meio] == valor) {
        return meio; // Valor encontrado, retorna o índice
    }
    
    if (arr[meio] < valor) {
        esquerda = meio + 1; // Descartar a metade esquerda
    } else {
        direita = meio - 1; // Descartar a metade direita
    }
}

return -1; // Valor não encontrado
}

int main() { int n, valor;

cout << "Digite o número de elementos no vetor: ";
cin >> n;

int* arr = new int[n]; // Cria um vetor dinamicamente

cout << "Digite os elementos do vetor (em ordem crescente): ";
for (int i = 0; i < n; ++i) {
    cin >> arr[i];
}

cout << "Digite o valor a ser buscado: ";
cin >> valor;

int resultado = buscaBinaria(arr, n, valor);

if (resultado != -1) {
    cout << "Valor " << valor << " encontrado no índice " << resultado << "." << endl;
} else {
    cout << "Valor " << valor << " não encontrado no vetor." << endl;
}

delete[] arr; // Libera a memória alocada para o vetor

return 0;
}
23-

24-
#include <stdio.h> #include <math.h> #include <string.h>
int binarioParaDecimal(const char *binario) { int decimal = 0; int comprimento = strlen(binario);

for (int i = comprimento - 1; i >= 0; i--) {
    if (binario[i] == '1') {
        decimal += pow(2, comprimento - 1 - i);
    }
}

return decimal;
}

int main() { char binario[65]; // Assumindo um máximo de 64 bits + 1 para o terminador nulo

printf("Digite um número binário: ");
scanf("%s", binario);

for (int i = 0; i < strlen(binario); i++) {
    if (binario[i] != '0' && binario[i] != '1') {
        printf("Número binário inválido.\n");
        return 1;
    }
}

int decimal = binarioParaDecimal(binario);

printf("O número decimal é: %d\n", decimal);

return 0;
}

25-
#include <stdio.h>
void decimalParaBinario(int numero) { 
if (numero == 0) {
    printf("0");
    return;
}

while (numero > 0) {
    binario[i] = numero % 2;  // Armazena o resto da divisão por 2
    numero /= 2;              // Divide o número por 2
    i++;
}

printf("Número binário: ");
for (int j = i - 1; j >= 0; j--) {
    printf("%d", binario[j]);
}
printf("\n");
}

int main() { int numeroDecimal;

printf("Digite um número decimal: ");
scanf("%d", &numeroDecimal);

decimalParaBinario(numeroDecimal);

return 0;
}

26-
#include <stdio.h>
#define MAX 10 // Definindo o tamanho máximo para as matrizes
int main() { int matriz1[MAX][MAX], matriz2[MAX][MAX], resultado[MAX][MAX]; int linhas, colunas;

printf("Digite o número de linhas e colunas das matrizes: ");
scanf("%d %d", &linhas, &colunas);

if (linhas > MAX || colunas > MAX || linhas <= 0 || colunas <= 0) {
    printf("Tamanho da matriz inválido.\n");
    return 1;
}

printf("Digite os elementos da primeira matriz:\n");
lerMatriz(matriz1, linhas, colunas);

printf("Digite os elementos da segunda matriz:\n");
lerMatriz(matriz2, linhas, colunas);

somarMatrizes(matriz1, matriz2, resultado, linhas, colunas);

printf("\nPrimeira matriz:\n");
imprimirMatriz(matriz1, linhas, colunas);

printf("\nSegunda matriz:\n");
imprimirMatriz(matriz2, linhas, colunas);

printf("\nMatriz resultante da soma:\n");
imprimirMatriz(resultado, linhas, colunas);

return 0;
}

27-
#include <stdio.h>
#define MAX 10 
for (int i = 0; i < linhas1; i++) {
    for (int j = 0; j < colunas2; j++) {
        resultado[i][j] = 0;
    }
}

for (int i = 0; i < linhas1; i++) {
    for (int j = 0; j < colunas2; j++) {
        for (int k = 0; k < colunas1; k++) {
            resultado[i][j] += matriz1[i][k] * matriz2[k][j];
        }
    }
}
}

int main() { int matriz1[MAX][MAX], matriz2[MAX][MAX], resultado[MAX][MAX]; int linhas1, colunas1, linhas2, colunas2;

printf("Digite o número de linhas e colunas da primeira matriz: ");
scanf("%d %d", &linhas1, &colunas1);

if (linhas1 > MAX || colunas1 > MAX || linhas1 <= 0 || colunas1 <= 0) {
    printf("Tamanho da matriz inválido.\n");
    return 1;
}

printf("Digite os elementos da primeira matriz:\n");
lerMatriz(matriz1, linhas1, colunas1);

printf("Digite o número de linhas e colunas da segunda matriz: ");
scanf("%d %d", &linhas2, &colunas2);

if (linhas2 > MAX || colunas2 > MAX || linhas2 <= 0 || colunas2 <= 0) {
    printf("Tamanho da matriz inválido.\n");
    return 1;
}

if (colunas1 != linhas2) {
    printf("A multiplicação não é possível. O número de colunas da primeira matriz deve ser igual ao número de linhas da segunda matriz.\n");
    return 1;
}

printf("Digite os elementos da segunda matriz:\n");
lerMatriz(matriz2, linhas2, colunas2);

multiplicarMatrizes(matriz1, linhas1, colunas1, matriz2, linhas2, colunas2, resultado);

printf("\nPrimeira matriz:\n");
imprimirMatriz(matriz1, linhas1, colunas1);

printf("\nSegunda matriz:\n");
imprimirMatriz(matriz2, linhas2, colunas2);

printf("\nMatriz resultante da multiplicação:\n");
imprimirMatriz(resultado, linhas1, colunas2);

return 0;
}

29-
#include <stdio.h> #include <ctype.h> // Para a função tolower
while ((c = *str++) != '\0') {
    c = tolower(c);
    if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') {
        contador++;
    }
}

return contador;
}

int main() { char str[100];

printf("Digite uma string: ");
fgets(str, sizeof(str), stdin);

int numeroDeVogais = contarVogais(str);

printf("Número de vogais na string: %d\n", numeroDeVogais);

return 0;
}

30-
#include <stdio.h> #include <ctype.h> // Para a função isdigit
while (isspace(*str)) {
    str++;
}

if (*str == '-') {
    sinal = -1;
    str++;
} else if (*str == '+') {
    str++;
}

while (*str && isdigit(*str)) {
    resultado = resultado * 10 + (*str - '0');
    str++;
}

return sinal * resultado;
}

int main() { char str[100];

printf("Digite uma string para converter em inteiro: ");
fgets(str, sizeof(str), stdin);

int numero = stringParaInteiro(str);

printf("Número inteiro convertido: %d\n", numero);

return 0;
}


