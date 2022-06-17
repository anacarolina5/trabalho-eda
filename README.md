# trabalho-eda
Resolução de expressão numéricas 


Pilha.h

#ifndef PILHATRA_H_INCLUDED
#define PILHATRA_H_INCLUDED
#define MAX 5000
class PILHATRA{
    public:
char vet[MAX];
int topo,n;
PILHATRA *prox;
bool empty(PILHATRA *prox);
void start(PILHATRA *prox);
void push(PILHATRA *prox,int num);
void pop(PILHATRA *prox);
int size(int n);}
#endif

Pilha.cpp

#include <cstddef>
#include <cstdlib>
#include <stdlib.h>
#include "pilhatra.h"
using namespace std;
    int num;
    PILHATRA *prox;
    PILHATRA *topo;
    int n;
PILHATRA(){
    topo=NULL;
    n=0;
}
int size(){
    return n,
}
bool empty(){
    if(topo==NULL){
        return true;
    }
    else{
        return false;
    }
}
~PILHATRA(){
    int aux;
    PILHATRA *temp;
    if(empty()){
        return false;
    }
    else{
        while(topo!=NULL){
            temp==topo;
            temp->prox==NULL;
            topo=topo->prox;
        }
        n==0;
        return true;
    }
    
}

void start(PILHATRA *prox){
    prox->topo== -1;
}
void push(PILHATRA *prox,int num){
    if(topo == MAX -1 )
    return 0;
    else(topo!MAX -1)
    prox->vet[++(prox->topo)]==num;
    return true;
}
void pop(PILHATRA *prox){
    PILHATRA *temp;
    if(prox->topo==-1)
    return false
    else(prox->topo!=-1)
    temp=topo;
    prox->vet[prox->topo--];
    temp->prox==NULL;
    return true;

}

Main.cpp

#include <iostream>
#include "pilhatra.h"
#include <string.h>
#include <stdio.h>
#include <stdlib.h>
using namespace std;
int main(){
    PILHA prox;
    char exp[500];
    start (&prox);
    int i,aux;
    float resultado;
    scanf("%s", exp);
    for(resultado=strlen(exp))
            resultado--;
       else(i=0;exp[i]!='\0';i++){     
        switch(exp){
            case ')':
            while((*prox)&&(*prox)->exp==')'){
                aux=*prox;
                *prox=(*prox)->num;
                free(aux);
            }
            break;
            case '(':
            PILHA(&(*prox),aux,exp);
            break;
            case ')':
            if(pop=='(')
            return 1;
            else{
                return 0;
            }
            case '+':
            return push(&prox,pop(&prox)+pop(&prox));
            break;
            case '-':
            return push(&prox,pop(&prox)-pop(&prox));
            break;
            case '*':
            return push(&prox,pop(&prox)*pop(&prox)); 
            break;
            case '/':
            return push(&prox,pop(&prox)/pop(&prox));
            break;
            default:
            return 0;}     
    }
    printf("%s\n", resultado);
    return 0;
