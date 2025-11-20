# server-1
Aquí tienes la versión limpia, directa y sin elementos decorativos innecesarios, ideal para documentación técnica o material de estudio formal.

***

**Arreglo Bidimensional: Presupuesto y Cálculos**

**1. Declaración y Estado Inicial (La Matriz de Datos)**
Creamos la matriz `Presupuesto[4, 3]` (4 filas, 3 columnas) con los valores originales planificados.

*Estado Inicial:*

| Categoría | Mes 1 (j=0) | Mes 2 (j=1) | Mes 3 (j=2) |
| :--- | :--- | :--- | :--- |
| Alimentos (i=0) | 120 | 130 | 125 |
| Transporte (i=1) | 40 | 35 | 45 |
| Servicios (i=2) | 60 | 60 | 70 |
| Ahorro (i=3) | 100 | 110 | 95 |

**2. Actualización de Valores**
Antes de realizar los cálculos, actualizamos los datos accediendo a su posición `[Fila, Columna]`.

```text
// A. Corrección: El gasto de Servicios (Fila 2, Columna 2)
 fue 68, no 70.
Presupuesto[2, 2] = 68 

// B. Actualización: Aumento de 15 en Transporte
 (Fila 1, Columna 0).
// Valor actual (40) + 15 = 55.
Presupuesto[1, 0] = Presupuesto[1, 0] + 15
```

*Estado Actualizado (Valores Finales en Memoria):*

| Categoría | Mes 1 (j=0) | Mes 2 (j=1) | Mes 3 (j=2) |
| :--- | :--- | :--- | :--- |
| Alimentos (i=0) | 120 | 130 | 125 |
| Transporte (i=1) | **55** | 35 | 45 |
| Servicios (i=2) | 60 | 60 | **68** |
| Ahorro (i=3) | 100 | 110 | 95 |

**3. Cálculo 1: Gasto Total General**
Usamos un bucle anidado para sumar todos los elementos de la matriz con los datos actualizados.

```text
Total_General = 0 

// Bucle Externo: Recorre las Filas (Categorías)
Para i desde 0 hasta 3 hacer
    // Bucle Interno: Recorre las Columnas (Meses)
    Para j desde 0 hasta 2 hacer
        Total_General = Total_General + Presupuesto[i, j] 
    Fin Para
Fin Para

Imprimir: "El Gasto Total acumulado es: " + Total_General
```
*Resultado: La suma total es 1003.*

**4. Cálculo 2: Promedio Mensual**
Calculamos el promedio simple basado en el total obtenido.

```text
Cantidad_Meses = 3 
Promedio_Mensual = Total_General / Cantidad_Meses 

Imprimir: "El Gasto Promedio por mes fue: " + Promedio_Mensual
```
*Resultado: 1003 / 3 = 334.33*

**Conclusión**
Este proceso demuestra cómo los arreglos permiten estructurar información, modificar datos específicos mediante índices y realizar análisis masivos con bucles.

¿Te gustaría ver un ejemplo aplicado a un mapa de videojuego (coordenadas x,y) o prefieres otro ejercicio numérico?