## IES Ágora – Examen 2ª Evaluación CFGS DAM 1º EEDD—18 de marzo de 2024
Ejercicios sobre las partes Refactorización y Depuración
### Ejercicio 1. (4 puntos)
Parte git/github, ve a la url https://github.com/amg-ia/Examen y sigue las instrucciones que el fichero readme.md indica.

----


### Ejercicio 2. (6 puntos)
1. Utilizando la depuración intenta arreglar el error del siguiente código. Este es el algorimto quicksort un algorimo que permite ordenar elementos en una estructura.
2. Añade un segundo parámetro a la función quicksort(arr, asc), ***asc*** será un parámetro booleano, si es *True* se ordena de mayor a menor si es *False* al contrario. Por defecto el parámetro será *True*.


~~~python
def quicksort(arr):
    """
    Ordena la lista utilizando Quicksort.
    """
    if len(arr) <= 1:
        return arr

    pivot = arr[0]
    left, right = [], []
    for x in arr[1:]:
        if x > pivot:
            left.append(x)
        else:
            right.append(x)

    # Llamada recursiva con el error
    return [pivot] + quicksort(right) +  quicksort(left)

# Ejemplo de uso
if __name__ == "__main__":
    lista = [5, 2, 9, 1, 5, 6]
    lista_ordenada = quicksort(lista)
    print("Lista ordenada:", lista_ordenada)
~~~
