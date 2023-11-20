# RETO3
## Pseudocodigo de numeros primos

```pseudocode
	
x : entero
y : lista que contega (2,3,5,7)

inicio
  x := un numero entero
  Mientras (x > 1) hacer
    Si modulo (x,2 valores de y (2,3,5,7) != 0
      escribir ("x es primo")
    sino
      y := y - 1
  fin mientras
fin	  
```
##Diagrama de flujo:

```mermaid
flowchart TD
    A[Inicio]--> B
    B[Numero x] --> D
    D[y = lista de 2,3,5,7] -->E
    E{residuo x/2 valores de y = 0?}
    E -->|Si| F[x no es primo] -->H
    E -->|No| G[x es primo] -->H 
    H[x:x-1] --> I 
    I{x menor a 2?}
    I -->|Si| J[fin]
    I -->|No| E
```
## Pseudocodigo de racies

```pseudocode

x : entero
y : el primer valor de la lista en x
v : los demas valores de x sin y
z : numero mas cercano a y que multiplicado por si mismo sea <= y
w : z * 2
u : lista del 1 al 9
t : entero
r : w agregado y multiplicado por el mismo valor de u

inicio
 Mientras x > 99
   separar x en una lista en pares
     (sacar (z-y) y agregardo v) = t
       si w agregado y multiplicado por el mismo valor de u == t entonces
	 escribir( r "es la raiz de (x))
       sino probar con otro numero de u
         si en ningun valor de u se encuentra
	   escribir (x "no tiene raiz exacta")
 fin para

 Para 1 < x > 100
   si u*u == x
     escribir (s "es raiz de x)  
   sino
     escribir (x "no tiene raiz exacta")
 fin para
Fin	   	

```
## Diagrama de flujo

```mermaid
flowchart TD
    A[Inicio]--> B
    B[Numero x] --> D
    D[u = lista de 1 al 9 ] -->E
    E{x > 99?}
    E -->|Si| F[separar x en pares] -->H 
    H[buscar un numero que multiplicado por si mismo sea <= al primer par de x 'y'] -->I
    I[primer par de x restado y*2] -->J
    J[se agrega un valor de u a z*2] -->K
    K[se multiplica por el mismo num agregado] -->L
    L{La operacion da igual a x?}
    L -->|si| M[es la raiz de x] -->Q
    L -->|NO, Probar con otro valor de u| J 
    E -->|No| G[u * u] -->N
    N{u * u = x?} 
    N --> |si| O[es la raiz de x] -->Q
    N --> |no, Probar con otro valor de u| G 
    Q[FIN]
```
