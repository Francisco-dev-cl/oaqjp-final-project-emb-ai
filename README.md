# Emotion Detection Web Application

Este repositorio contiene la solución al proyecto final del curso de **IBM**, que consiste en una aplicación web interactiva que analiza el tono emocional de un texto. El sistema se conecta con la API de procesamiento de lenguaje natural (NLP) de **IBM Watson** para clasificar el texto en cinco emociones básicas y determinar la predominante.

## 🎯 Características y Objetivos del Proyecto
*   **Consumo de APIs de IA:** Conexión asíncrona mediante peticiones HTTP `POST` al microservicio de *Watson NLP Service*.
*   **Análisis Predictivo:** Cálculo de puntuaciones para las emociones *anger* (ira), *disgust* (disgusto), *fear* (miedo), *joy* (alegría) y *sadness* (tristeza), identificando dinámicamente la emoción dominante utilizando funciones nativas de Python (`max()`).
*   **Control de Errores Robusto (Task 7):** Manejo de entradas en blanco o inválidas mediante la captura del código de estado HTTP 400 y validación de valores `None`, evitando caídas del servidor y mejorando la experiencia de usuario.
*   **Cumplimiento de Estándares de Código:** Todo el backend cumple rigurosamente con las normativas de estilo tradicionales (incluye docstrings completos en módulos y funciones para facilitar el mantenimiento).

## 📁 Componentes Clave del Código
*   **`EmotionDetection/emotion_detection.py`**: Contiene la función `emotion_detector()`, encargada de estructurar el objeto JSON, enviar los encabezados gRPC requeridos, consumir la API de Watson y procesar la respuesta estructurada.
*   **`server.py`**: El núcleo de la aplicación web en **Flask**. Configura el enrutamiento para la interfaz de usuario (`/`) y el endpoint de la API (`/emotionDetector`) que procesa los parámetros de consulta y formatea la respuesta final para el cliente.

## 🛠️ Tecnologías Utilizadas
*   **Backend:** Python 3.x, Flask
*   **Librerías de Red:** Requests, JSON
*   **Servicio de IA:** IBM Watson NLP Runtime (`emotion_aggregated-workflow`)
*   **Frontend:** HTML5, CSS3, JavaScript (AJAX)

## 🚀 Instalación y Ejecución Local

### 1. Clonar el repositorio
```bash
git clone https://github.com
cd oaqjp-final-project-emb-ai
```

### 2. Instalar dependencias requeridas
Asegúrate de contar con Flask y la librería de peticiones HTTP instaladas en tu entorno local o virtual:
```bash
pip install Flask requests
```

### 3. Iniciar la aplicación web
Ejecuta el servidor backend:
```bash
python server.py
```
El servidor se desplegará localmente en el puerto `5000`. Puedes abrir tu navegador e ingresar a: `http://localhost:5000/`.

## 📈 Habilidades Técnicas Demostradas (Para Reclutadores)
*   **Desarrollo de Microservicios Backend:** Creación y configuración de servidores web con Flask en producción local.
*   **Integración de Modelos de IA:** Consumo efectivo de servicios en la nube (Cloud AI integration) abstrayendo la complejidad del modelo NLP.
*   **Lógica de Programación y Manejo de Datos:** Filtrado de diccionarios complejos de tipo JSON, ordenamiento de datos clave-valor y sanitización de entradas de usuario.
