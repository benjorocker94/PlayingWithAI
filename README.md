# Generación de Objetos 3D a partir de Imágenes 2D con TripoSR en Google Colab

Este proyecto utiliza un notebook de Google Colaboratory para generar un archivo de objeto 3D (formato `.obj`) a partir de una imagen 2D proporcionada por el usuario. Se basa en la tecnología de reconstrucción 3D **TripoSR** desarrollada por VAST AI Research, aprovechando las potentes bibliotecas **Hugging Face Transformers**, **Accelerate** y **huggingface_hub** dentro del entorno gratuito de Google Colab.

## ¿Qué es TripoSR?

TripoSR es un modelo de inferencia eficiente para la reconstrucción 3D a partir de una única vista de imagen. Destaca por su velocidad y la calidad de los modelos 3D generados, representando una alternativa accesible a otros métodos de reconstrucción 3D.

## Uso de TripoSR de Forma Gratuita y Académica

Este Colab ofrece una manera práctica y gratuita de experimentar con la tecnología TripoSR. Al ejecutarse en el entorno de Google Colab, los usuarios pueden aprovechar la aceleración por GPU sin incurrir en costos adicionales. Este proyecto tiene un **propósito principalmente académico y de experimentación**, permitiendo a estudiantes, investigadores y entusiastas explorar las capacidades de los modelos de reconstrucción 3D y la integración de las herramientas de Hugging Face en un entorno de desarrollo accesible.

## Tecnologías Utilizadas

* **TripoSR (VAST AI Research):** El modelo de red neuronal principal para la inferencia de reconstrucción 3D.
* **Hugging Face Transformers:** Una biblioteca de vanguardia que proporciona arquitecturas de modelos pre-entrenados (como los utilizados en TripoSR) y utilidades para diversas tareas de procesamiento del lenguaje natural y visión por computadora.
* **Accelerate:** Una biblioteca de Hugging Face diseñada para simplificar el entrenamiento y la ejecución de modelos de PyTorch en diferentes configuraciones de hardware (CPU, GPU, TPU, y entornos distribuidos). En este caso, facilita el uso eficiente de la GPU en Colab.
* **huggingface_hub:** Una biblioteca que permite interactuar con el Hugging Face Hub, donde se almacenan y comparten miles de modelos pre-entrenados y datasets. Este proyecto descarga el modelo pre-entrenado de TripoSR desde el Hub.
* **Google Colaboratory (Colab):** Un entorno de cuaderno Jupyter gratuito que se ejecuta completamente en la nube y ofrece acceso a GPUs, lo que permite la ejecución de tareas de aprendizaje automático con requisitos computacionales significativos.
* **PyTorch:** El framework de aprendizaje profundo en el que se basa TripoSR y las bibliotecas de Hugging Face utilizadas.

## Flujo del Notebook

1.  **Configuración del Entorno:** Se habilita el uso de la GPU en Colab y se clona el repositorio de TripoSR.
2.  **Instalación de Dependencias:** Se instalan las bibliotecas necesarias, incluyendo PyTorch, Transformers, Accelerate y otras herramientas.
3.  **Descarga del Modelo Pre-entrenado:** Se descarga el modelo pre-entrenado de TripoSR desde Hugging Face Hub. **(Nota: Puede requerir autenticación con un token de Hugging Face si el modelo es privado o tiene restricciones de acceso. Ver sección de Consideraciones).**
4.  **Subida de la Imagen 2D:** El usuario puede subir una única imagen 2D a través de la interfaz de Colab.
5.  **Generación del Objeto 3D:** El script de TripoSR (`run.py`) procesa la imagen subida para generar un modelo 3D en formato `.obj`. El archivo de salida se guarda como `mesh.obj` dentro de una carpeta con el nombre de la imagen (sin la extensión) en el directorio `output_models`.
6.  **Descarga del Archivo .obj:** Se ofrece un botón para descargar el archivo `mesh.obj` generado.

## Cómo Utilizar

1.  Abre este notebook en Google Colaboratory.
2.  Sigue las instrucciones en cada celda, ejecutándolas secuencialmente.
3.  Cuando se te solicite, sube una imagen 2D de la que quieras generar un modelo 3D.
4.  Espera a que el proceso de generación se complete.
5.  Finalmente, descarga el archivo `.obj` generado.

## Consideraciones y Posibles Fallas

* **Reinicio de la Sesión:** Después de la instalación de las dependencias, Colab puede solicitar reiniciar la sesión. Es importante hacerlo y volver a ejecutar las celdas necesarias.
* **Autenticación de Hugging Face:** La descarga del modelo pre-entrenado puede requerir que tengas una cuenta en Hugging Face y que te autentiques con un token si el modelo tiene acceso restringido. Asegúrate de seguir las instrucciones si aparece un error de "Unauthorized".
* **Error al Crear Directorios:** Se ha corregido la lógica para la creación de directorios. Si aún experimentas problemas, revisa la salida de las celdas para identificar la causa.
* **Previsualización del Objeto 3D:** Actualmente, el notebook no incluye una previsualización interactiva del objeto 3D generado directamente en Colab. El archivo `.obj` debe descargarse y visualizarse con un software de modelado 3D externo (e.g., Blender, MeshLab).
* **Limitación a una Sola Imagen:** Este notebook está configurado para procesar una única imagen subida.
* **Rendimiento y Calidad:** El rendimiento y la calidad del modelo 3D generado pueden variar dependiendo de la imagen de entrada.

## Posibles Mejoras Futuras

* Implementar una visualización 3D interactiva del modelo generado directamente en el Colab (usando `pythreejs` u otras bibliotecas).
* Añadir una interfaz de usuario más amigable.
* Permitir la selección de diferentes modelos de TripoSR (si estuvieran disponibles públicamente).
* Incluir opciones para ajustar los parámetros de generación (si el script `run.py` lo permite).
* Implementar validación del tipo de archivo subido.

## Licencia

[Aquí puedes añadir la licencia bajo la que distribuyes este proyecto, por ejemplo, MIT License.]

## Agradecimientos

A VAST AI Research por desarrollar y compartir TripoSR, y a Hugging Face por sus excelentes bibliotecas y la plataforma Hugging Face Hub que facilitan el acceso a modelos y herramientas de aprendizaje automático.

---

Este README proporciona una descripción técnica completa de tu proyecto, resaltando su propósito académico, las tecnologías utilizadas y cómo funciona. Asegúrate de guardar este contenido en un archivo llamado `README.md` en la raíz de tu repositorio de GitHub. ¡Espero que esto te sea de gran ayuda para tu portafolio! ¿Hay algo más en lo que pueda ayudarte?

## Resultados

![ChatGPT Image 5 may 2025, 01_22_22 p m](https://github.com/user-attachments/assets/a062ee05-1851-427d-9f30-1668e5cd3e97)

![example](https://github.com/user-attachments/assets/b9306b17-a648-42b3-a7e4-e28fc9713618)



