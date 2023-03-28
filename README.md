# Reto 7
##### **1.** Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.
```python
i : int = 0 #se declara i como entero e inicia desde 0
j = int #se declara i como entero, este ayudrará a guardar y mostrar los cuadrados
while(i < 100): #mientras que i sea menor a 100
  i += 1 #se le sumará 1 a i cada vez que se repita el ciclo
  j = i**2 #j será el cuadrado del valor de i
  print("El cuadrado del número" ,i, "es" ,j) #se imprime los valores de las variables respectivamente
```
##### **2.** Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.
```python
i : int = 0 #se declara i como entero e inicia desde 0
print("Los números impares desde 1 hasta 999 son:") #se imprime este mensaje
while(i < 1000): #Mientras que el valor i sea menor a 1000
  i += 1 #se le suma 1 al valor de i cada vez que se repita el ciclo
  if i % 2 == 1: #Si el residuo de la operación i/2 es igual a 1, imprimirá el valor de i y por ende, es impar.
    print (i)
i = 0 #Se inicia de nuevo i desde 0
print("Los números pares desde 2 hasta 1000 son:") #se imprime este mensaje
while(i < 1000): #Mientras que el valor i sea menor a 1000
  i += 1 #se le suma 1 al valor de i cada vez que se repita el ciclo
  if i % 2 == 0: #Si el residuo de la operación i/2 es igual a 0, imprimirá el valor de i y por ende, es par.
    print (i)
```
##### **3.** Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado
```python
i = int(input("Ingrese cualquier número natural mayor o igual a 2: ")) #se declara i como entro y se le pide al usuario que defina la variable
print("Los números pares que son mayores o iguales a 2 y menores o iguales al número" ,i, "son:") #Se imprime este mensaje
while i >= 2: #Mientras que i sea mayor o igual a 2
    if i % 2 == 0: #Si el residuo de la operacio i/2 es igual a 0, imprimirá el valor de i, por ende, éste será par.
        print(i)
    i -= 1 #Se le resta 1 al valor de i, y se repetirá el ciclo hasta que la condición de éste cumpla
```
##### **4.** En 2022 el país A tendrá una población de 25 millones de habitantes y el país B de 18:9 millones. Las tasas de crecimiento anual de la población serán de 2% y 3% respectivamente. Desarrollar un algoritmo para informar en que año la población del país B superará a la de A.
```python
a : float = 25000000 #se declara a como flotante e inicia desde 25000000
b : float = 18900000 #se declara b como flotante e inicia desde 18900000
year : int = 2022 #se declara year como entero e inicia desde 2022
while a>b: #mientras que valor de a sea mayor que b, éste imprimirá e valor de la variables
    print("Para",year, "el país A tendrá una población de",a, "de habitantes y el país B de",b)
    year += 1 #el ciclo se repite cada vez que se le sume 1 al valor de year, y este termina cuando la condición de while sea falsa
    a *= 1.02
    b *= 1.03
if b>a:
    print("Para",year, "el país B habrá superado la población del país A") #Se hace una última condición e imprimirá el año en el que el país B tenga mayor población que la del A
```
##### **5.** Imprimir el factorial de un número natural n dado.
```python
i = int(input("Ingrese el número que desea saber su factorial: ")) #se declara i como entero y se le pide al usuario que ingrese el valor inicial de este
j = i #la variable j se usará como contador y guardará el valor del factorial
while i>1: #mientras que i sea mayor que 1
    i -= 1 #se le resta 1 a i cada vez que se repita el ciclo
    j *= i #se multiplica j por el valor de j cadavez que se repita el ciclo
print("El factorial del número ingresado es:" ,j) #se imprime el valor de j, es decir el factorial del número ingresado por el usuario
```
##### **6.** Implementar un algoritmo que permita adivinar un número dado de 1 a 100, preguntando en cada caso si el número es mayor, menor o igual.
```python
inferior:int = 1 #se declara inferior como entero e inicia desde 1
superior:int = 100 #se declara superior como entero e inicia desde 100
respuesta = '' #respuesta es una variable tipo string
while respuesta != '=': #si el usuario ingresa la cadena = quiere decir que el algoritmo advinó su número
  numero = (inferior + superior) // 2 #el valor de número será la suma de los valores de inferior y superior dividido entre 2, este será entero
  respuesta = input(f"¿Es {numero} mayor (>), menor (<) o igual (=) el número en el que estas pensando?") #el usuario contanrá con tres opciones <, > y =, dependiendo de lo escoja, se efectuará un condiconal diferente
  if respuesta == '>':
    inferior = numero - 1
  elif respuesta == '<':
    superior = numero + 1
print(f"El número en que está pensando es {numero}")#cuando se rompa el ciclo, la consola mostarará el valor que el usuario pensó
```
##### **7.** Implementar un programa que ingrese un número de 2 a 50 y muestre sus divisores.
```python
i = int(input("Ingrese un número natural entre 2 y 50: ")) #se decalara i como entero y el usuario determinará su valor
j = 1 #j será también un entero que inice desde 1, servirá como contador
while i<2 or i>50:
    i = int(input("¿Papi yo hablo en chino? Dije un número natural entre 2 y 50: ")) #en dado caso de que el usuario sea bobo, se imprimirá el siguiente mensaje hasta que ingrese un valor apropiado
print("Los números divisibles de",i, "son:")#se imprime el siguiente mensaje
while i>=j: #mientras que el valor de i sea mayor o igual a j, se repetirá el ciclo
    if i%j == 0:
        print(j) #si el residuo de la división entre i y j es igual a 0, se imprimirá j
    j += 1 #esto se repite hasta que j sea igual i
```
##### **8.** Implementar el algoritmo que muestre los números primos del 1 al 100. nota: use funciones
```python
def es_primo(numero): 
    i = 2
    if numero < 2:
        return False
    while i != int(numero**0.5) + 1:
        if numero % i == 0:
          return False
        i += 1  
    return True
x = 1
while x != 100:
  if es_primo(x): 
     print(x)
  x += 1
```
