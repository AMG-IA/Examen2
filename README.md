## IES Ágora – Examen 2ª Evaluación CFGS DAM 1º EEDD—15 de marzo de 2024
Ejercicios sobre las partes Refactorización y Depuración
### Ejercicio 1. (4 puntos)
Parte git/github, ve a la url https://github.com/amg-ia/Examen y sigue las instrucciones que el fichero readme.md indica.

----

### Ejercicio 2. (2 puntos)
Refactoriza y limpia el siguiente código en python:

~~~python
# Cálculo del área de un círculo y su circunferencia
import math

# Datos del círculo
radio = 5

# Cálculo del área
area = math.pi * radio ** 2

# Cálculo de la circunferencia
circunferencia = 2 * math.pi * radio

# Mostrar resultados
print(f"Área del círculo: {area:.2f}")
print(f"Circunferencia del círculo: {circunferencia:.2f}")
~~~
----

### Ejercicio 3. (4 puntos)
Necesitas arreglar tu informe de gastos, aparentemente algo no cuadra del todo.
Específicamente, necesitas encontrar las dos entradas que suman **2020** y luego multiplicar esos dos números.
Por ejemplo, supongamos que su informe de gastos contiene lo siguiente:

1721
979
366
299
675
1456

En esta lista, las dos entradas que suman 2020 son 1721 y 299. Multiplicarlos produce 1721 * 299 = 514579, por lo que la respuesta correcta es **514579**.
Por supuesto, su informe de gastos es mucho mayor y se encuentra disponible en el fichero **gastos.dat** del repositorio. Encuentre las dos entradas que suman **2020**; ¿Qué obtienes si los multiplicas?

El siguiente código es capaz de resolver el problema aunque tiene un error. Copialo en tu IDE y busca opciones de refactorización y de optimización. 
Revisa el código para encontrar el error y procede a realizar las refactorizaciones que encuentre más adecuadas.
***¡¡NOTA!!*** El resultado esperado es ***646779***
~~~python
a = open("gastos.dat","r")
data = a.read().splitlines()
numbers = []
for x in range (0,len(data)):
    y = data[x]
    y_int = int (y)
    numbers.append(y_int)

print(numbers)
encontrado = False

longitud_completa_de_la_lista_de_numeros = len(numbers)
for x in range (0, longitud_completa_de_la_lista_de_numeros):
    encontrado = False
    for i in range(0, longitud_completa_de_la_lista_de_numeros):

        if numbers[x]+numbers[i] == 2020 and encontrado == False:
            r = numbers[x] + numbers[i]
            print("Los dos números que suman 2020 multiplicados dan: ",r)
            encontrado = True #No buscamos más

print("Fin del programa")
~~~
