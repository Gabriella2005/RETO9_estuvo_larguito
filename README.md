# RETO 9

Bienvenidos, espero este repositorio sea de ayuda y aprecien mi esfuerzo.

# 1) De los retos anteriores seleciones 3 funciones y escribalas en forma de lambdas.

### a) Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.

```
def carne(N : int, K : int , M : int )-> int:
    return N + K + M

if __name__ == "__main__":
    N_inicial = int(input("ingrese la cantidad de gallinas que hay: "))
    M_inicial = int(input("ingrese la cantidad de gallos que hay: "))
    K_inicial = int(input("ingrese la cantidad de pollitos que hay: "))
    N = 6*N_inicial
    M = 7*M_inicial
    K = 1*K_inicial
    carnaves = carne(N, K, M)
    print("la cantidad de carne de aves que hay en total es " + str(carnaves) +" kg")

if __name__ == "__main__":
    N_inicial = int(input("ingrese la cantidad de gallinas que hay: "))
    M_inicial = int(input("ingrese la cantidad de gallos que hay: "))
    K_inicial = int(input("ingrese la cantidad de pollitos que hay: "))
    N = 6*N_inicial
    M = 7*M_inicial
    K = 1*K_inicial
    carnita = lambda N, M, K: N + M + K
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
def cuenta(P : int, L : int , H : int )-> int:
    return P + L + H

if __name__ == "__main__":
    panes = int(input("¿Cuántos panes tienes que comprar?: "))
    leche = int(input("¿Cuántas bolsas de leche tienes que comprar?: "))
    huevos =  int(input("¿Cuántos huevos tienes que comprar?: "))
    P = panes*300
    L = leche*3300
    H = huevos*350
    total = cuenta(P, L, H)
    print("tu compra costó $" + str(total))

if __name__ == "__main__":
    panes = int(input("¿Cuántos panes tienes que comprar?: "))
    leche = int(input("¿Cuántas bolsas de leche tienes que comprar?: "))
    huevos =  int(input("¿Cuántos huevos tienes que comprar?: "))
    P = panes*300
    L = leche*3300
    H = huevos*350
    tienda = lambda P, L, H: P + L + H
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
def intereses(Ci : int, i : int , n : int )-> int:
    return Ci*((1+(i/100)**n))

if __name__ == "__main__":
    Ci = int(input("ingrese el capital inicial en pesos: "))
    i = int(input("ingrese la tasa de interés (%): "))
    n = int(input("ingrese el periodo de ahorro en meses: "))
    interes = intereses(Ci, i, n)
    print("El capital final teniendo en cuenta la información dada es " + str(interes))

if __name__ == "__main__":
    Ci = int(input("ingrese el capital inicial en pesos: "))
    i = int(input("ingrese la tasa de interés (%): "))
    n = int(input("ingrese el periodo de ahorro en meses: "))
    banco = lambda Ci, i, n: Ci + i + n
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
# 3) Escriba una función recursiva para calcular la operación de la potencia.
# 4) Realice pruebas para calcular fibonacci con iteración o con recursión. Determine desde que número de la serie la diferencia de tiempo se vuelve significativa.
# 5) Cuenta stackoverflow

![image](https://user-images.githubusercontent.com/124614177/235529600-7aca4c76-1e0f-44e9-8095-f91b98ba769f.png)

# 6) Cuenta linked.in

![image](https://user-images.githubusercontent.com/124614177/235529662-66538f94-4093-4a14-9d6e-02e8c5cc8b8f.png)

