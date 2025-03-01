# Stiven-Bravo
### UNIVERSIDAD ESTATAL AMAZONICA
#### Asignatura: Fundamentos de la programacion
##### Paralelo: "D"
# Definamos una matriz con 3 filas y 3 columnas
# Definir la matriz 3x3
matriz = [
    [9, 3, 7],
    [5, 2, 6],
    [8, 1, 4]
]

# Función para buscar un valor en la matriz
def buscar_valor(matriz, valor):
    for i in range(len(matriz)):
        for j in range(len(matriz[i])):
            if matriz[i][j] == valor:
                return (i, j)  # Retorna la posición (fila, columna)
    return None  # Si no se encuentra el valor

# Función para ordenar una fila de la matriz usando Bubble Sort
def ordenar_fila(matriz, fila):
    n = len(matriz[fila])
    # Aplicar Bubble Sort
    for i in range(n):
        for j in range(0, n-i-1):
            if matriz[fila][j] > matriz[fila][j+1]:
                matriz[fila][j], matriz[fila][j+1] = matriz[fila][j+1], matriz[fila][j]

# Función para mostrar la matriz
def mostrar_matriz(matriz):
    for fila in matriz:
        print(fila)

# Valor a buscar en la matriz
valor_buscar = 6

# Mostrar la matriz original
print("Matriz original:")
mostrar_matriz(matriz)

# Buscar el valor en la matriz
posicion = buscar_valor(matriz, valor_buscar)
if posicion:
    print(f"\nEl valor {valor_buscar} se encontró en la posición {posicion}")
else:
    print(f"\nEl valor {valor_buscar} no se encontró en la matriz.")

# Ordenar la fila 1 (segunda fila) usando Bubble Sort
ordenar_fila(matriz, 1)

# Mostrar la matriz con la fila ordenada
print("\nMatriz después de ordenar la fila 1 (segunda fila):")
mostrar_matriz(matriz)