# Contador de Monedas con OpenCV

Este proyecto utiliza OpenCV y NumPy para contar monedas en una imagen aplicando técnicas de procesamiento de imágenes como el suavizado gaussiano, detección de bordes y operaciones morfológicas.

## Descripción

El script procesa una imagen (euros.jpeg) para convertirla a escala de grises, aplicar un desenfoque gaussiano, realizar una detección de bordes con el algoritmo de Canny, y luego utilizar una operación de cierre morfológico para mejorar los contornos detectados. Finalmente, el código cuenta el número de monedas detectadas en la imagen y dibuja los contornos sobre la imagen original.

## Requisitos

Para ejecutar este proyecto, necesitas tener instaladas las siguientes librerías:

- **OpenCV**: Para el procesamiento de imágenes.
- **NumPy**: Para el manejo de matrices.

### Instalación de Dependencias

Puedes instalar las dependencias ejecutando:

bash
pip install opencv-python numpy


## Cómo Ejecutar el Proyecto

1. Coloca la imagen euros.jpeg en el mismo directorio que el script.
2. Ejecuta el script de Python:

bash
python contador_monedas.py


## Explicación del Código

1. **Lectura de la imagen**: El script carga la imagen euros.jpeg utilizando cv2.imread().
2. **Conversión a escala de grises**: Convierte la imagen a una versión en escala de grises usando cv2.cvtColor().
3. **Desenfoque Gaussiano**: Aplica un filtro gaussiano para reducir el ruido en la imagen.
4. **Detección de bordes**: Usa el algoritmo de Canny para detectar los bordes de las monedas.
5. **Cierre morfológico**: Aplica una operación de cierre para unir bordes y mejorar los contornos.
6. **Detección de contornos**: Encuentra los contornos de las monedas utilizando cv2.findContours().
7. **Visualización**: Muestra varias etapas del procesamiento de imágenes en ventanas separadas.

## Resultados

El script imprime el número de monedas detectadas en la consola:

yaml
monedas encontradas: X


Donde X es el número de monedas detectadas en la imagen.

## Personalización

Puedes ajustar los siguientes parámetros en el código para mejorar la detección:

- **valorGauss**: Controla el nivel de suavizado gaussiano.
- **valorKernel**: Afecta el tamaño del kernel usado en el cierre morfológico.

## Capturas de Pantalla

- **Imagen Original con Contornos Dibujados**
- **Imagen en Escala de Grises**
- **Detección de Bordes Canny**
- **Resultado del Cierre Morfológico**

## Licencia

Este proyecto está bajo la Licencia MIT. Puedes encontrar más detalles en el archivo [LICENSE](LICENSE).
