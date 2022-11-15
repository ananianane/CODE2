# CODE2Thanushan    
#include <stdio.h>
#include <string.h>

void saisieEcrire(char tab[20]){
    printf("cous avez juste a rentrer les valeurs : ");
    gets(tab);
    fflush(stdin);
    printf("%s",tab);
}
void maj(char chaine[1000]){
    for(int i = 0; i< strlen(chaine);i++){
        if(chaine[i]>=97 && chaine[i]<=122){
            chaine[i] -= 'a' -'A';
        }
    }
    printf("les lettres en maj : ");
    printf("%s \n",chaine);
}
void min(char chaine[1000]){
    for(int i = 0; i< strlen(chaine);i++){
        if(chaine[i]>=65 && chaine[i]<=90){
            chaine[i] -= 'A' -'a';
        }
    }
    printf("les lettres en min : ");
    printf("%s \n",chaine);
}

void voyellesMinMaj1104(char chaine[1000]){
    int min = 0;
    int maj = 0;
    for(int i = 0; i< strlen(chaine);i++){
        if(chaine[i]==97 ||chaine[i]==101 ||chaine[i]==105 ||chaine[i]==111 ||chaine[i]==117 ||chaine[i]==121){
            min++;
        }
        else if(chaine[i]==65 ||chaine[i]==69 ||chaine[i]==73 ||chaine[i]==79 ||chaine[i]==85 ||chaine[i]==89){
            maj++;
        }
        else{
            continue;
        }
    }
    printf("Il y a %d de minuscule de voyelle.\nIl y a %d de majuscule dans le voyelle.\n",min,maj);
}
int main() {
    int tab[20];
    saisieEcrire(tab);
    maj(tab);
    min(tab);
    voyellesMinMaj1104(tab);
    return 0;
}

#include <Arduino.h>
int thermistance =A0;
int led=3;
float valeur=0;

void setup() {
  pinMode(thermistance,INPUT);
  pinMode(led,INPUT);   }