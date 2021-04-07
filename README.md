#include <iostream>
#include <stdlib.h>
#include <ctime>
#include <cstdlib>
#include <conio.h>
using namespace std;
int main(){
    /*
    estou usando a palavra amor e vou esconder elas no meio das letras aleatórias
    */
    int m;
    int i;
    int l;//linha que vou colocar a palavra
    srand(time(NULL));
    int N;
    char R [3];
    R[0]='a'; R[1]='m'; R[2]='o'; R[3]='r';
    int T;
    char letras[25];
    letras[0]='a';letras[1]='b';letras[2]='c';letras[3]='d';letras[4]='e';
    letras[5]='f';letras[6]='g';letras[7]='h';letras[8]='i';letras[9]='j';
    letras[10]='k';letras[11]='l';letras[12]='m';letras[13]='n';letras[14]='o';
    letras[15]='p';letras[16]='q';letras[17]='r';letras[18]='s';letras[19]='t';
    letras[20]='u';letras[21]='v';letras[22]='w';letras[23]='x'; letras[24]='y'; letras[25]='z';
    char letter[29][29];
    for(T=0;T<30;T++){
    for(N=0;N<30;N++){
        i = rand() %26;
    letter[N][T]=letras[i];
    }
    }
    T = rand() % 26;//linha aleatória que a palavra vai ser escondida
    i = rand() % 30;//coluna aleatória que a palavra vai ser escondida
    m = 0;
    for(N=0;N<=3;N++){
        letter[T][i]= R[m];
        T++;
        m++;
    }
    for(N=0;N<30;N++){
        for(T=0;T<30;T++){
            if(T<29){
            cout << letter[T][N] << " ";
            }else{
                cout << letter[T][N] << endl;
            }
        }
    }
    cout << "digite a palavra escondida";
  return 0;

}
