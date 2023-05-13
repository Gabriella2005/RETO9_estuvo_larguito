# RETO 9

Bienvenidos, espero este repositorio sea de ayuda y aprecien mi esfuerzo.

# 1) De los retos anteriores seleciones 3 funciones y escribalas en forma de lambdas.

### a) Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.

```
def carne(N : int, K : int , M : int )-> int: #definimos 'carne' y sus parámetros
    return N + K + M #retornamos la suma de los kilos

if __name__ == "__main__":
    N_inicial = int(input("ingrese la cantidad de gallinas que hay: ")) #pedimos la cantidad de cada animal
    M_inicial = int(input("ingrese la cantidad de gallos que hay: "))
    K_inicial = int(input("ingrese la cantidad de pollitos que hay: "))
    N = 6*N_inicial #multiplicamos la cantidad de animales por su respectivo peso
    M = 7*M_inicial
    K = 1*K_inicial
    carnaves = carne(N, K, M) #ejecutamos la función carne
    print("la cantidad de carne de aves que hay en total es " + str(carnaves) +" kg")

if __name__ == "__main__":
    N_inicial = int(input("ingrese la cantidad de gallinas que hay: "))
    M_inicial = int(input("ingrese la cantidad de gallos que hay: "))
    K_inicial = int(input("ingrese la cantidad de pollitos que hay: "))
    N = 6*N_inicial
    M = 7*M_inicial
    K = 1*K_inicial
    carnita = lambda N, M, K: N + M + K #ejecutamos la función lambda
    carnaves = carnita(N, M, K)
    print("la cantidad de carne de aves que hay en total es " + str(carnaves) +" kg")


if __name__ == "__main__":
    N_inicial = int(input("ingrese la cantidad de gallinas que hay: "))
    M_inicial = int(input("ingrese la cantidad de gallos que hay: "))
    K_inicial = int(input("ingrese la cantidad de pollitos que hay: "))
    N = 6*N_inicial
    M = 7*M_inicial
    K = 1*K_inicial
    carnaves = (lambda x, y, z: x + y + z)(N, M, K)
    print("la cantidad de carne de aves que hay en total es " + str(carnaves) +" kg")
```

### b) Mi mamá me manda a comprar P panes a 300 cada uno, M bolsas de leche a 3300 cada una y H huevos a 350 cada uno. Hacer un programa que me diga la cuenta

```
def cuenta(P : int, L : int , H : int )-> int: #definimos 'cuenta' y sus parámetros
    return P + L + H #retornamos la suma de los parámetros

if __name__ == "__main__":
    panes = int(input("¿Cuántos panes tienes que comprar?: ")) #pedimos al usuario la cantidad que va a comprar de cada producto
    leche = int(input("¿Cuántas bolsas de leche tienes que comprar?: "))
    huevos =  int(input("¿Cuántos huevos tienes que comprar?: "))
    P = panes*300 #multiplicamos la cantidad de producto por su precio
    L = leche*3300
    H = huevos*350
    total = cuenta(P, L, H) #ejecutamos la función 'cuenta'
    print("tu compra costó $" + str(total))

if __name__ == "__main__":
    panes = int(input("¿Cuántos panes tienes que comprar?: "))
    leche = int(input("¿Cuántas bolsas de leche tienes que comprar?: "))
    huevos =  int(input("¿Cuántos huevos tienes que comprar?: "))
    P = panes*300
    L = leche*3300
    H = huevos*350
    tienda = lambda P, L, H: P + L + H #ejecutamos lambda
    total = tienda(P, L, H)
    print("tu compra costó $" + str(total))


if __name__ == "__main__":
    panes = int(input("¿Cuántos panes tienes que comprar?: "))
    leche = int(input("¿Cuántas bolsas de leche tienes que comprar?: "))
    huevos =  int(input("¿Cuántos huevos tienes que comprar?: "))
    P = panes*300
    L = leche*3300
    H = huevos*350
    total = (lambda x, y, z: x + y + z)(P, L, H)
    print("tu compra costó $" + str(total))
```

### c) Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.

```
def intereses(Ci : int, i : int , n : int )-> int: #definimos 'intereses' y sus parámetros
    return Ci*((1+(i/100)**n)) #retornamos el resultado de la formula de interes compuesto

if __name__ == "__main__":
    Ci = int(input("ingrese el capital inicial en pesos: ")) #pedimos al usuario los datos necesarios para operar
    i = int(input("ingrese la tasa de interés (%): "))
    n = int(input("ingrese el periodo de ahorro en meses: "))
    interes = intereses(Ci, i, n) #ejecutamos la funcion 'intereses'
    print("El capital final teniendo en cuenta la información dada es " + str(interes))

if __name__ == "__main__":
    Ci = int(input("ingrese el capital inicial en pesos: "))
    i = int(input("ingrese la tasa de interés (%): "))
    n = int(input("ingrese el periodo de ahorro en meses: "))
    banco = lambda Ci, i, n: Ci + i + n #ejecutamos lambda
    interes = banco(Ci, i, n)
    print("El capital final teniendo en cuenta la información dada es " + str(interes))


if __name__ == "__main__":
    Ci = int(input("ingrese el capital inicial en pesos: "))
    i = int(input("ingrese la tasa de interés (%): "))
    n = int(input("ingrese el periodo de ahorro en meses: "))
    interes = (lambda x, y, z: x + y + z)(Ci, i, n)
    print("El capital final teniendo en cuenta la información dada es " + str(interes))
```

# 2) De los retos anteriores seleciones 3 funciones y escribalas con argumentos no definidos (*args).
### a)
```
def carne(*args)-> int: #definimos la función 'carne' para cualquier parámetro
    return N + K + M # retornamos la suma de los kilos de carne

if __name__ == "__main__":
    N_inicial = int(input("ingrese la cantidad de gallinas que hay: "))#pedimos la cantidad de cada animal
    M_inicial = int(input("ingrese la cantidad de gallos que hay: "))
    K_inicial = int(input("ingrese la cantidad de pollitos que hay: "))
    N = 6*N_inicial #multiplicamos la cantidad de animales por su respectivo peso
    M = 7*M_inicial
    K = 1*K_inicial
    carnaves = carne(N, K, M)#ejecutamos la función carne
    print("la cantidad de carne de aves que hay en total es " + str(carnaves) +" kg")
```
### b)
```
def cuenta(*args)-> int:#definimos 'cuenta' y para cualquier parametro
    return P + L + H #retornamos la suma de los parámetros

if __name__ == "__main__":
    panes = int(input("¿Cuántos panes tienes que comprar?: ")) #pedimos al usuario la cantidad que va a comprar de cada producto
    leche = int(input("¿Cuántas bolsas de leche tienes que comprar?: "))
    huevos =  int(input("¿Cuántos huevos tienes que comprar?: "))
    P = panes*300 #multiplicamos la cantidad de producto por su precio
    L = leche*3300
    H = huevos*350
    total = cuenta(P, L, H)#ejecutamos la función 'cuenta'
    print("tu compra costó $" + str(total))
```
### c) 
```
def intereses(*args)-> int:#definimos 'intereses' para cualquier parametro
    return Ci*((1+(i/100)**n))#retornamos el resultado de la formula de interes compuesto

if __name__ == "__main__":
    Ci = int(input("ingrese el capital inicial en pesos: "))#pedimos al usuario los datos necesarios para operar
    i = int(input("ingrese la tasa de interés (%): "))
    n = int(input("ingrese el periodo de ahorro en meses: "))
    interes = intereses(Ci, i, n)#ejecutamos la funcion 'intereses'
    print("El capital final teniendo en cuenta la información dada es " + str(interes))
```

# 3) Escriba una función recursiva para calcular la operación de la potencia.
```
def potencia(n: int, pot:int) -> int: #definimos potencia y sus parámetros
    if pot == 0: #si eleva a la 0, retornamos 1
        return 1
    if pot == 1: #si eleva a la 1, retornamos la base
        return n
    if n == 0: #si la base es 0, retornamos 0
        return 0
    else:
        return n*potencia(n,pot-1) #multiplicamos 'n' por si mismo hasta que 'pot' sea igual a 1 y retorne n
    
if __name__ == "__main__":
    n = int(input("ingrese un número: ")) #pedimos la base 
    pot = int(input("ingrese la potencia para el numero dado: ")) #pedimos el exponente
    elevado = potencia(n,pot) #ejecutamos la funcion potencia
    print(elevado)
```

# 4) Realice pruebas para calcular fibonacci con iteración o con recursión. Determine desde que número de la serie la diferencia de tiempo se vuelve significativa.
```
import time

start_time = time.time()
def fib(*args)-> int: #definimos 'fib' para cualquier argumento dado
    num1 = 0 #le asignamos a 'num1' el valor de 0
    num2 = 1 #le asignamos a 'num2' el valor de 2
    if num == 0: #si el usuario pide 0 numeros de la serie, retornamos 0
        return 0
    if num == 1: #si el usuario pide 1 numero de la serie, retornamos 0
        return 0
    else:
        cont = 2 #iniciamos el contador en 2 e imprimimos los dos primeros valores
        print('0')
        print('1')
        while (cont < num): #realizamos el siguiente proceso hasta que el contador sea igual a los numeros pedidos por el usuario
            sum = num1 + num2 #definimos 'sum' como la suma de 'num1' y 'num2'
            num1 = num2 #ahora 'num1' tomara el valor de 'num2'
            num2 = sum # ahora 'num2' tomara el valor de la suma hecha
            print(sum) #imprimimos la suma
            cont = cont + 1 #sumamos 1 al contador
    
if __name__ == "__main__":
    num = int(input("cuantos numeros de la serie fibonacci deseas? ")) #preguntamos al usuario cuantos numeros de la serie desea
    sumita = fib(num) #ejecutamos 'fib'
    print(sumita)

end_time = time.time()

timer = end_time - start_time
print('tiempo : ',timer)
```

# 5) Cuenta stackoverflow

![image](https://user-images.githubusercontent.com/124614177/235529600-7aca4c76-1e0f-44e9-8095-f91b98ba769f.png)

# 6) Cuenta linked.in

![image](https://user-images.githubusercontent.com/124614177/235529662-66538f94-4093-4a14-9d6e-02e8c5cc8b8f.png)

