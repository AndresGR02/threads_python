# Laboratorio #3 - Hilos en Python

Con el código inicial, se puede observar un error a la hora de ordenar los elementos. La
razón de esto se debe a la falta de agregar el comando de sort al finalizar el ordenamiento de 
los subvectores para ordenar el vector final. Por lo que se hizo la modificación de la siguiente manera: 

```python
def unir_vectores(subvectores):
    vector_ordenado = [num for subvector in subvectores for num in subvector]
    vector_ordenado.sort()
    return vector_ordenado
```
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
