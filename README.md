# trabajos-en-clase
/******************************************************************************



*******************************************************************************/
#include <stdio.h>
#include <stdlib.h>
#define tam 10

void inicializarArreglo(int[]);
void datosVector(int);
void numBuscar(int,int);
void main()
{
    int op=1,arreglo[tam]={5,4,3,2},cantNum,num; //Inicializar el arreglos
    
    while(op<=2)
    {
    printf("1.inicialicacion de arreglo\n2.arreglo\n3.salir\n");
    printf("Escoja una opcion:");
    scanf("%d",&op);
    
            switch(op)
            {
                case 1:
                    inicializarArreglo(arreglo);
                break;
                
                case 2:
                    printf("Ingrese la cantidad de elementos del vector: ");
                    scanf("%d",&cantNum);
            
                    datosVector(cantNum);
                break;
                
                case 3:
                    printf("Ingrese la cantidad de elementos del vector: ");
                    scanf("%d",&cantNum);
                    
                    numBuscar(cantNum, num);
                break;
                
                case 4:
                    exit(0);
                break;
                default:
				    printf("Opcion invalida");
			    break;
            }
    }
}
void inicializarArreglo(int arreglo[tam])
{
    int cont=0;
    
    while(cont<4)
    {
        printf("arreglo [%d],%d\n",cont,arreglo[cont]);
        
        cont++;
    }
}
void datosVector(int cantNum)
{
    int cont=0,arreglo[tam];
    
    while(cont<cantNum)
    {
        printf("Ingrese el elemento[%d]: ",cont);
        scanf("%d",&arreglo[cont]);
        
        cont++;
    }
    printf("elementos del vector: \n");
    cont=0;
    
    while(cont<cantNum)
    {
        printf("elemento[%d]=%d\n",cont,arreglo[cont]);
        
        cont++;
    }
}
void numBuscar(int cantNum,int num)
{
	int cont=0,arreglo[tam],cuenta=0;
	while(cont<cantNum)
	{
		printf("Ingrese el elemento:");
		scanf("%d",&arreglo[cont]);
		cont++;
	}
	cont=0;
	printf("Elementos del Arreglos\n");
	while(cont<cantNum)
	{
		printf("Elemento[%d]=%d\n",cont,arreglo[cont]);
		if(num==arreglo[cont])
		cuenta++;
	cont++;
	}
	printf("El numero %d se repite %d veces",num,cont);
}

