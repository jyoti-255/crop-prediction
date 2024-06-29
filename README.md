# Crop Recommendation System using Flask 🌾🚀

## Project Overview

This project implements a crop recommendation system using Flask, predicting the best crop to cultivate based on environmental factors such as Nitrogen, Phosphorus, Potassium, Temperature, Humidity, pH, and Rainfall. The prediction model is deployed as a Flask web application.

## Project Components 📦

### Flask App (`app.py`)

The Flask application serves as the backend for the crop recommendation system. It handles HTTP requests, processes input data, and returns predictions to the user.

#### Endpoints

- **Home Page (`'/'`):** Renders the `home.html` template where users can input environmental data.
  
- **Prediction Endpoint (`'/predict'`):** Handles POST requests containing environmental data, preprocesses the data (standardization using a scaler), and predicts the best crop using a pre-trained machine learning model (`model.pkl`).

#### Dependencies

- Flask: Used for creating the web application and handling HTTP requests. 🌐
- NumPy: Required for numerical operations in data processing. 🧮
- Pandas: Used for data manipulation and handling. 🐼
- Scikit-learn: Provides machine learning utilities, including model loading (`pickle` for serialization) and data preprocessing (StandardScaler). 🤖

### Model (`model.pkl`)

The prediction model is serialized using pickle (`pickle.load(open('model.pkl', 'rb'))`) and deployed within the Flask application. It predicts the crop based on the input environmental factors after standardizing the input data (`sc.transform(single_pred)`).

### Templates (`templates/home.html`)

The `home.html` template is rendered on the home page of the application (`'/'`). It contains a form where users can input environmental data to receive crop recommendations.

### Static Files

- **CSS and JavaScript:** Any static files required for styling and client-side functionality can be stored in appropriate directories. 🎨📜

## Usage 🌱

1. Ensure all dependencies are installed using `pip install -r requirements.txt`.
2. Run `python app.py` to start the Flask application.
3. Access the application in your web browser at `http://localhost:5000`.

---


