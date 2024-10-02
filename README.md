# PRÁCTICA 2. VISIÓN POR COMPUTADOR

> Trabajo realizado por:
> - David Koschel Henríquez
> - Pablo Nicolás Santana Hernández

### TAREA 1

Para esta tarea se copió el código existente del conteo de píxeles blancos en las columnas y se modificaron ciertos valores para realizar el conteo
por filas. Se cambió el segundo parámetro del _reduce_ a 1 para que cogiese las filas. Luego se normalizaron los datos
para que se muestren en porcentaje y se pinta el histograma. Además, se realizó el cálculo del _maxfil_, valor máximo de 
las filas, para poder compararlo y averiguar cuántas veces se daba el 95% de este valor o más.

El resultado obtenido es que este valor para la imagen del mandril es de 0.4296875 y su 95% del valor se da en dos ocaciones
en la fila 12 y la 100, así se muestra en la gráfica.

![](results/t1_canny.png)

### TAREA 2
Para esta tarea se reutilizó el código anterior para el conteo de las filas, las columnas y los máximos. Estos métodos
se aplicaron tanto en la imagen _sobel_ como en la _canny_. Por último, para el resaltado de las filas y columnas
máximas (que ya las teníamos gracias al cófigo anterior), se dibujaron líneas sobre las filas y columnas
correspondientes.


#### Resultados obtenidos

![](results/t2_marked_images.png)

![](results/t2_count_sobel.png)

![](results/t2_count_canny.png)

#### Comparación Sobel vs Canny
En la comparativa de las gráficas podemos apreciar de que al aplicar _Sobel_ el valor máximo es mayor, cerca del 50%
en el conteo de filas, mientras que _Canny_ está en un 40% aproximadamente. En el conteo de columnas sucede lo mismo, _Canny_ está
cerca del 35%-40% como valores más altos, mientras que el _Sobel_ supera ligeramente el 40%.

Por otro lado, en las imágenes con las filas y columnas de mayor valor resaltadas, podemos ver que _Sobel_ detecta un mayor
número de ambas. 

Es por todo esto, que concluimos que _Sobel_ captura un mayor número de detalles mientras que _Canny_ detecta bordes
más nítidos o mejor definidos.

### TAREA 3

Para esta tarea se decidió crear dos filtros.

El primero detecta el movimiento (contando los píxeles que han cambiado entre dos frames en cierto margen), y pixela la
imagen (reduciéndola y volviendo a ampliarla) dependiendo del movimiento que detecta. A mayor movimiento, más se pixela la
imagen.

![](results/t3_gif.gif)

Para mejor resolución [ver aquí](results/video.mp4)

El segundo filtra aplica una máscara para detectar cuál es el color RGB que más presente está en cada pixel, y solo
muestra ese color en su máximo valor.

![](results/t3_color_img.png)


### TAREA 4

Basándonos en el vídeo de "Messa di voce" decidimos aplicar al vídeo capturado un filtro _Canny_ y sobre el _frame_ generado 
pintar líneas en los bordes y círculos dentro de los contornos o recintos cerrados. Estos contornos deben de ser de un 
tamaño superior a 300 píxeles para ser detectado.

![gif_circles](results/t4_gif1.gif)


![gif_lines](results/t4_gif2.gif)
