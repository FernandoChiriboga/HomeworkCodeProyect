"# HomeworkCodeProyect" 
#include<iostream>
using namespace std;
void IngresoD(int*,int*);
void Calcular(int*,int*,int*);
void Imprimir(int*);
int main(){
	int numero=0,denominador=0,resultado;
	IngresoD(&numero,&denominador);
	Calcular(&numero,&denominador,&resultado);
	Imprimir(&resultado);
	if(numero==2*resultado+denominador){
		resultado+=2*denominador;
	}else{
		resultado+=denominador;
	}
	Imprimir(&resultado);
}
void IngresoD(int*a,int*b){
	do{
		cout<<"Ingresa el numero"<<endl;
		cin>>*a;
	}while(*a<=0);
	do{
		cout<<"Ingresa el divisor"<<endl;
		cin>>*b;
	}while(*b<=0);
}
void Calcular(int*a,int*b,int*resultado){
	int aux=*a;
	for(int i=aux-1;i>0;i--){
		if(i%*b==0){
			*resultado=i;
			break;
		}
	}
}
void Imprimir(int*numero){
	cout<<*numero<<"\n";
}
