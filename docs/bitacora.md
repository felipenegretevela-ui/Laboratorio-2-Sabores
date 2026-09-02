# Bitácora - Laboratorio 2 Sabores

## Ejercicio 0

1. Calcular el promedio de estrellas de un restaurante: **Dominio**.

2. Mostrar 4.333... como "4.3": **UI**.

3. La lista de los restaurantes de muestra: **Datos**.

4. "El comentario debe tener al menos 15 caracteres": **Dominio**.

5. El botón "Publicar" se pinta gris: **UI**.

6. Recordar cuántas estrellas lleva marcadas el usuario: **ViewModel**.

7. Decidir a qué pantalla ir después de guardar: **UI**.

8. Convertir priceLevel = 2 en "$$": **Dominio**.


## Ejercicio B2

### 1. Cambiar NavType.IntType por StringType sin cambiar getInt

Da un error porque la ruta espera un texto, pero el código intenta leer un número entero. Los tipos ya no coinciden.

### 2. Tocar la misma tarjeta varias veces y después regresar

Se guardan varias copias de la misma pantalla en el back stack. Por eso hay que presionar "Atrás" varias veces.

Esto se evita usando `launchSingleTop = true`, para no abrir varias veces la misma pantalla.

## Ejercicio B4

### 1. ¿Cuál de las tres pruebas de la Parte 0 detecta este error?

La prueba de girar el teléfono lo detecta. Al girar, el estado guardado con `remember` se pierde.

### 2. ¿A quién le pertenecen las reseñas: al detalle, a la lista, o a ninguno de los dos?

Las reseñas no pertenecen solamente al detalle ni solamente a la lista. Las necesitan varias pantallas.

El detalle muestra las reseñas y la lista usa esas reseñas para mostrar el promedio.


### 3. Si las reseñas estuvieran en un remember dentro de SaboresApp(), ¿se arreglan los dos experimentos?

El Experimento 1 sí se arreglaría, porque al regresar a la pantalla el estado seguiría en `SaboresApp()`.

El Experimento 2 no se arreglaría, porque al girar el teléfono la Activity se vuelve a crear y el `remember` se pierde. Para evitar eso se necesita un `ViewModel`.