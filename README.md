# matrizes-exemplo-codigo-em-Java

Ir para o conteúdo principal
 
Moodle - IFRS

Programação Básica com Java III - Turma 2022B
Painel Meus cursos  PBJIII2022B 3. Matrizes  3.5. Matrizes em Java
3.5. Matrizes em Java
Em Java a declaração de matrizes é similar à de vetores. A diferença é a inclusão de mais pares de colchetes, um para cada dimensão da matriz. Por exemplo, para se declarar uma matriz bidimensional de N linhas por M colunas escrevemos:

tipo[][] nome da variável = new tipo[N][M];

Por exemplo, uma matriz 3x5 de números inteiros poderia ser declarada assim:

int[][] matriz = new int[3][5];

Lembrando que essa operação pode ser realizada em dois passos, como nos vetores, conforme mostrado abaixo:


int[][] matriz;

matriz = new int[3][5]

O acesso a uma posição da matriz é realizado utilizando-se diversos pares de colchetes em vez de vírgulas (como fizemos em pseudocódigo). Por exemplo, para acessar a posição localizada na linha 1 coluna 2 da matriz declarada anteriormente, fazemos:

matriz[1][2] = 10;

Assim, podemos escrever nosso programa de jogo da velha em Java, como mostrado abaixo. Note que neste programa, como prometido anteriormente, acrescentamos código para mostrar uma mensagem no final do jogo indicando quem venceu ou se houve empate. Também acrescentamos código para mostrar o tabuleiro ao usuário após cada jogada. Lembre-se que as matrizes, assim como vetores, tem índices começando em zero e não um.




public class JogoDaVelha {


public static void main(String[] args) {


char jogador = ‘X’, vencedor = ‘A’; // Já inicializamos aqui


int linha, coluna, cont, contaJogadas = 0;


char[][] tabuleiro = new char[3][3];


 


while(vencedor != ‘X’ && vencedor != ‘O’) {


       System.out.printf(“Jogador %c é a sua vez.\n”, jogador);


              System.out.print(“Linha: ”);


              linha = Integer.parseInt(System.console().readLine());


              System.out.print(“Coluna: ”);


              coluna = Integer.parseInt(System.console().readLine());


 


              if(linha >= 1 && linha <= 3 && coluna >= 1 && coluna <= 3) {                            

tabuleiro[linha-1][coluna-1] = jogador;


                     if(jogador == ‘X’)


                           jogador = ‘O’;


             else


                           jogador = ‘X’;


 


             contaJogadas++;

             if(contaJogadas == 9)

                    vencedor = ‘E’;




 


                    for(cont = 0; cont < 3; cont++) {


if(tabuleiro[cont][0] == tabuleiro[cont][1] && tabuleiro[cont][1] == tabuleiro[cont][2])



                                   vencedor = tabuleiro[cont][0];


            


if(tabuleiro[0][cont] == tabuleiro[1][cont] && tabuleiro[1][cont] == tabuleiro[2][cont])

vencedor = tabuleiro[0][cont];

            }

    if(tabuleiro[0][0] == tabuleiro[1][1] && tabuleiro[1][1] == tabuleiro[2][2])


                           vencedor = tabuleiro[0][0];


                  if(tabuleiro[0][2] == tabuleiro[1][1] && tabuleiro[1][1] == tabuleiro[2][0])


                           vencedor = tabuleiro[0][2];


 


                  // MOSTRA TABULEIRO


                  for(cont = 0; cont < 3; cont++) {


                           System.out.printf(“%c  %c  %c\n”, tabuleiro[cont][0], tabuleiro[cont][1], tabuleiro[cont][2]);


                  }


} else


                    System.out.println(“Essa posição não existe!”);


}

// MOSTRA VENCEDOR

if(vencedor == ‘E’)

       System.out.println(“\nHouve empate!\n”);

else

       System.out.printf(“\nVENCEDOR: Jogador %c\n”, vencedor);







}











}
Última atualização: domingo, 1 nov 2020, 19:20
Seguir para...
Academi
Dúvidas? 
Perguntas frequentes

Fale conosco | Suporte | Contato

Informação
Termos e Condições de Uso
Aviso de Privacidade e Proteção de Dados Pessoais
Contato
Rua Gen. Osório, 348, Bento Gonçalves/RS
Siga-nos
Copyright © 2017 - Desenvolvido por LMSACE.com. Distribuído por Moodle

Português - Brasil ‎(pt_br)‎
English ‎(en)‎
Español - Internacional ‎(es)‎
Français ‎(fr)‎
Italiano ‎(it)‎
Português - Brasil ‎(pt_br)‎
Mudar para o tema padrão
