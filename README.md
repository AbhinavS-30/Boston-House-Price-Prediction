# Boston House Price Prediction

A complete end-to-end Machine Learning project that predicts house prices in Boston based on various features. Built using Scikit-Learn, Flask, and standard ML pipeline practices, this project includes model training, evaluation, and deployment through a simple web interface.

## Table of Contents
- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Run the App](#run-the-app)
- [Model Training and Prediction](#model-training-and-prediction)
- [Future Improvements](#future-improvements)
- [License](#license)

## Overview
This project aims to predict the median value of owner-occupied homes in Boston using features such as crime rate, property tax, average number of rooms, and more. It includes the complete lifecycle of a machine learning workflow — from preprocessing, training, saving the model, and serving predictions via a Flask-based web application.

## Tech Stack
Language: Python 3.7+  
Libraries: Pandas, NumPy, Scikit-learn, Flask, Matplotlib  
Tools: VS Code, GitHub, Git, logging  
Model: Linear Regression (can be replaced with others)

## How It Works
1. The dataset is loaded and explored using Jupyter Notebook (`main.ipynb`).  
2. A regression model is trained using scikit-learn, and the scaler and model are saved as `scaler.pkl` and `model.pkl`.  
3. A Flask web app is developed to collect user input and generate house price predictions using the saved model artifacts.  
4. The app runs locally and takes real-time user input through a form served via HTML (`templates/home.html`).

## Installation
- Clone the repository  
- Create a virtual environment using conda or venv  
- Activate the environment  
- Install dependencies from `requirements.txt`  
- Ensure `model.pkl` and `scaler.pkl` are in the project root

## Run the App
- Activate the virtual environment  
- Run the Flask app using:  
  ```bash
  python app.py
  ```
- Open `http://127.0.0.1:5000` in your browser  
- Fill in the feature values to get a price prediction

## Model Training and Prediction
The pipeline includes the following steps:
- Data scaling using StandardScaler  
- Training with Linear Regression  
- Saving trained model and scaler as serialized `.pkl` files  
- Flask app loads these files and returns predictions based on user input

## Future Improvements
- Add logging and error handling  
- Include automated model evaluation scripts  
- Dockerize the app for portability  
- Deploy on cloud (Heroku, AWS, etc.)  
- Add input validation and range checks in the form
