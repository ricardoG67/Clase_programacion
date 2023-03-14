## Ejercicios

1. Dado un array de numeros determinar si la suma de los elementos es par o impar.
2. Dado dos palabras, determinar cual es la más corta.
3. Obten el promedio de una lista.
4. Dado una lista cambiar los 2 por 0
5. Dado un string imprime las vocales.
6. Proyecto:

Haz una calculadora basandote en la interfaz de [video](https://youtu.be/fcz-v3x9Z6w?list=PL8dzsytd6ch1XwyB_mbo1dYOLOjKviCAv&t=158)

Datos:

Coloca en 1: Sumar, 2: multiplicar, 3: dividir, 4: exponente y 5: salir.

La aplicación mostrara un menu, con las 5 opciones, en donde una vez seleccionada una opcion se debera introducir los dos numeros con los que se hara la operacion.

Consejos: usa for para que sea infinito hasta que se presione 5. Utiliza input("Ingrese el valor: ") para obtener la data.

7. Dada una matriz, obten la suma de las diagonales.
8. Dado una lista de enteros se busca encontrar el ratio de los valores, negativos, positivos y ceros.

arr = [1,1,0,-1,-1]

El ratio para tanto positivo y negativo seria de 0.4 y el de ceros 0.2.

9. Explica que hace el siguiente código escrito en C

```C
#include <conio.h>
#include <stdio.h>

int main()
{
    int numero;
    int x = 0;
    int y = 0;

    printf( "\n   " );

    for ( numero = x ; numero <= y ; numero += 2 )
    {
        printf( "%d ", numero );
    }

    getch(); /* Pausa */

    return 0;
}
```

10. Explica que hace el siguiente codigo

```python
def funcion(numero):
    if numero < 2:
        return False
    elif number == 2:
        return True
    elif number > 2 and number % 2 == 0:
        return False
    else:
        for i in range(3,number):
            if number % i == 0:
                return False

    return True
```


## Resolución

1. 
```python
def suma_par_impar(a,b):
    suma = a + b
    if suma % 2 == 0:
        return "La suma es par."
    else:
        return "La suma es impar."

suma_par_impar(3,5) #par
suma_par_impar(2,4) #par
suma_par_impar(9,0) #impar
```
2. 
```python
def palabra_mas_corta(palabra1, palabra2):

    if len(palabra1) < len(palabra2):
        return palabra1

    else if len(palabra1) == len(palabra2):
        return "Son del mismo tamaño"

    else:
        return palabra2

palabra_1 = "Python"
palabra_2 = "Programación"
print(palabra_mas_corta(palabra_1, palabra_2)) # Output: Python

```
3. 
```python
#Metodo 1:
def promedio(lista):
    suma = sum(lista)
    promedio = suma / len(lista)
    return promedio

#Metodo2:
def promedio(lista):
    suma = 0
    for elemento in lista:
        suma = suma + elemento
    promedio = suma / len(lista)
    return promedio

mi_lista = [4, 6, 2, 8, 5]
print(promedio(mi_lista)) # Output: 5.0

```
4. 
```python
def cambiar_dos_por_cero(lista):
    for i in range(len(lista)):
        if lista[i] == 2:
            lista[i] = 0
    return lista
```
5. 
```python
def imprimir_vocales(cadena):
    vocales = "aeiouAEIOU"
    for letra in cadena:
        if letra in vocales:
            print(letra)
```
6. 
```python
# Multiples soluciones
```
7. 
```java
//Resolucion en java
public static int diagonalDifference(List<List<Integer>> arr) {
        arr.toArray();
        int n = arr.size();
        int diag1 = 0, diag2=0;
        int cont=0;
        for (int i=0; i<n; i++){
            for (int j=0; j<n; j++){
                if (i == j){
                    diag1 += (arr.get(i)).get(j);
                }
            }
            for (int j2=n-1; j2>=0; j2--){
                if (i+j2 == n-1){
                    diag2+= (arr.get(i)).get(j2);
                }
            }
        }

        return Math.abs(diag1 - diag2);
    }

```
8. 
```java
public static void plusMinus(List<Integer> arr) {
    // Write your code here
        int negativos=0;
        int positivos=0;
        int ceros=0;
        int n = arr.toArray().length;

        for(int i: arr){
            if (i==0){
                ceros++;
            }
            else if (i<0){
                negativos++;
            }else{
                positivos++;
            }
        }
        System.out.printf("%01.6f%n%01.6f%n%01.6f", (double)positivos/n, (double)negativos/n, (double)ceros/n);
}
```
9. Obtiene los numeros pares desde x hasta y.

10. Determina si es un numero primo 