# Laboratorio #3 - Hilos en Python

Con el código inicial, se puede observar un error a la hora de ordenar los elementos. 

*Vector ordenado final: [9, 12, 29, 34, 50, 52, 80, 82, 84, 86, 12, 20, 32, 42, 52, 68, 69, 69, 73, 73, 11, 13, 25, 31, 48, 78, 83, 88, 90, 95, 5, 10, 11, 31, 40, 66, 82, 88, 95, 100, 13, 23, 28, 39, 43, 50, 65, 71, 74, 92, 1, 2, 11, 14, 32, 39, 43, 58, 84, 87, 4, 19, 74, 76, 85, 89, 94, 95, 96, 100, 2, 12, 19, 23, 40, 52, 57, 64, 85, 100, 30, 36, 40, 40, 41, 44, 45, 58, 75, 84, 8, 12, 16, 38, 48, 64, 81, 85, 99, 100]*

La razón de esto se debe a la falta de agregar el comando de sort al finalizar el ordenamiento de 
los subvectores para ordenar el vector final. Por lo que se hizo la modificación de la siguiente manera: 

```python
def unir_vectores(subvectores):
    vector_ordenado = [num for subvector in subvectores for num in subvector]
    vector_ordenado.sort()
    return vector_ordenado
```

*Vector ordenado final: [2, 3, 4, 5, 6, 6, 7, 8, 10, 12, 13, 13, 14, 14, 14, 18, 18, 20, 20, 20, 20, 20, 21, 23, 24, 24, 27, 28, 30, 31, 32, 33, 33, 35, 36, 38, 38, 38, 41, 41, 41, 42, 42, 42, 43, 43, 43, 44, 49, 51, 51, 52, 52, 52, 55, 56, 56, 56, 59, 60, 61, 61, 62, 64, 64, 65, 67, 68, 69, 70, 71, 73, 74, 75, 75, 75, 77, 77, 77, 78, 78, 80, 80, 81, 82, 82, 84, 85, 87, 91, 92, 92, 94, 94, 96, 96, 96, 96, 97, 99]*

**Ahora, hagamos una comparativa de los tiempos dependiendo de la cantidad de hilos:**

Tiempos:

1 hilo:

0.0014109612

0.0014269352

0.0014424324

2 hilos:

0.0014572144

0.0014858246

0.0015003681

3 hilos:

0.0015182495

0.0015344620

0.0015509129


4 hilos:

0.0015699863

0.0015978813

0.0016138554


5 hilos:

0.0016307831

0.0016477108

0.0016660690


6 hilos:

0.0016853809

0.0017080307

0.0017282963


10 hilos: 

0.0017521381

0.0017745495

0.0018014908


De acuerdo a los resultados de las diferentes pruebas que se hicieron, 
se concluye que hay un mejor tiempo de ejecución cuando se utilizan menos hilos, en este caso 
cuando se utiliza sólamente 1 hilo.
