# Emotion Detection Web Application

This repository contains the solution to the final project for the **IBM** course, which consists of an interactive web application that analyzes the emotional tone of text. The system connects to the **IBM Watson** Natural Language Processing (NLP) API to classify text into five basic emotions and determine the predominant one.

## 🎯 Project Features and Objectives

* **AI API Consumption:** Asynchronous connection using HTTP POST requests to the *Watson NLP Service* microservice.
* **Predictive Analysis:** Calculation of scores for the emotions *anger*, *disgust*, *fear*, *joy*, and *sadness*, dynamically identifying the dominant emotion using native Python functions (`max()`).
* **Robust Error Handling (Task 7):** Handling blank or invalid inputs by capturing the HTTP 400 status code and validating `None` values, preventing server crashes and improving user experience.
* **Code Standards Compliance:** The entire backend strictly complies with traditional style regulations (includes full docstrings in modules and functions to facilitate maintenance).

## 📁 Key Code Components

* **EmotionDetection/emotion_detection.py**: Contains the `emotion_detector()` function, responsible for structuring the JSON object, sending the required gRPC headers, consuming the Watson API, and processing the structured response.
* **server.py**: The core of the web application built with **Flask**. Configures routing for the user interface (`/`) and the API endpoint (`/emotionDetector`) that processes query parameters and formats the final response for the client.

## 🛠 Technologies Used

* **Backend:** Python 3.x, Flask
* **Network Libraries:** Requests, JSON
* **AI Service:** IBM Watson NLP Runtime (`emotion_aggregated-workflow`)
* **Frontend:** HTML5, CSS3, JavaScript (AJAX)

## 🚀 Local Installation and Execution

### 1. Clone the repository

```bash
git clone https://github.com
cd oaqjp-final-project-emb-ai
```

### 2. Install required dependencies

Make sure you have Flask and the HTTP requests library installed in your local or virtual environment:

```bash
pip install Flask requests
```

### 3. Start the web application

Run the backend server:

```bash
python server.py
```

The server will deploy locally on port 5000. You can open your browser and go to: http://localhost:5000/.

## 📈 Technical Skills Demonstrated (For Recruiters)

* **Backend Microservices Development:** Creation and configuration of web servers with Flask in local production environments.
* **AI Model Integration:** Effective consumption of cloud services (Cloud AI integration), abstracting the complexity of the NLP model.
* **Programming Logic and Data Handling:** Filtering of complex JSON dictionaries, key-value data sorting, and user input sanitization.
