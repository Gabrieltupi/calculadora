# calculadora


// Online C compiler to run C program online
#include <stdio.h>
#include <stdlib.h>
#include <math.h>
int main() {
    // Write C code here
    //Gabriel Antonio Nunes de Souza
    //Analise e desenvolvimento do sistema, LaSalle.
    //matricula:202220863
    
    float n1;
    float n2;
    float x;
    int resp;
    do {
        puts("que operação desejaria fazer?\n 1- Soma.\n 2- Subtracao.\n 3- Multiplicacao.\n 4- Divisao.\n 5- Raiz Quadrada.\n 6- Potenciacao.\n 0- Sair.");
        scanf ("%d", &resp);
        
        switch (resp) {
            case 0:
                printf ("saindo...\n");
                break;
            case 1:
                puts("escreva os numeros que deseja somar:\n n1: ");
                scanf("%f",&n1);
                puts("n2: ");
                scanf("%f",&n2);
                printf("a soma é: %0.2f", n1 + n2);
                break;
            case 2:
                puts ("escreva os numeros que deseja subitrair:\n n1: ");
                scanf("%f",&n1);
                puts("n2: ");
                scanf("%f",&n2);
                printf("a subitracao é: %0.2f", n1 - n2);
                break;
            case 3:
                puts ("escreva os numeros que deseja multiplicar:\n n1: ");
                scanf("%f",&n1);
                puts("n2: ");
                scanf("%f",&n2);
                printf("a multiplicacao é: %0.2f", n1 * n2);
                break;
            case 4:
                puts("escreva os numeros que deseja dividir:\n Lebrando que o divisor(n2) nao pode ser 0.\n n1: ");
                scanf("%f",&n1);
                puts ("n2: ");
                scanf("%f",&n2);
                while (n2==0){
                    puts("hey mano, nao pode 0. escolha outro numero!");
                    puts ("n2: ");
                    scanf("%f",&n2);
                }
                printf("a divisao é: %0.2f",n1/n2);
                break;
            case 5:
                puts ("qual numero deseja saber a raiz quadrada: ");
                scanf("%f",&n1); 
                printf("a quaiz quadrada é:%0.2f ",sqrt(n1));
                break;
            case 6:
                puts ("a potencializacao de qual numero deseja fazer?\n n1: ");
                scanf("%f",&n1);
                puts ("em qual expoente?\n n2: ");
                scanf ("%f",&n2);
                printf("a potencializacao é: %0.2f", pow(n1,n2));
            default:
                printf("opção invalida, escreva outro numero!");
        }
    } while(resp !=0);
}
