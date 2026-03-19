# Health Insurance Cost Predictor

This is a **Streamlit-based web app** that predicts health insurance costs using machine learning. The app considers personal, lifestyle, and medical factors to estimate the cost of health insurance for an individual.  

The project uses pre-trained models (`model_young` and `model_rest`) and scalers for feature preprocessing to provide accurate predictions.

---

## Features
- Predict health insurance costs in real-time
- Interactive web interface with Streamlit
- Supports categorical and numerical features:
  - Age, Number of Dependants, Income, Genetical Risk  
  - Gender, Marital Status, BMI Category, Smoking Status, Employment Status, Region, Medical History, Insurance Plan
- Calculates a **normalized risk score** based on medical history
- Uses different models/scalers for young adults (≤25) and others

---

## Project Structure
ml-project-premium-prediction/
│
├── artifacts/ # Saved ML models and scalers
│ ├── model_young.joblib
│ ├── model_rest.joblib
│ ├── scaler_young.joblib
│ └── scaler_rest.joblib
├── src/ # ML code
│ ├── prediction_helper.py # Preprocessing and prediction logic
│ └── train_model.py # Optional: script to train models
├── app.py # Streamlit app
├── data/ # Optional datasets for training
├── requirements.txt # Python dependencies
└── README.md



## 🚀 Live Demo

👉 **Try the app here:**  
https://ml-project-premium-prediction-mb.streamlit.app/

---

## Installation

1. **Clone the repository**
```bash
git clone https://github.com/mbarapatre/ml-project-premium-prediction.git
cd "C:\Users\mbarapatre\ml-project-premium-prediction"

Create a virtual environment
python -m venv venv
venv\Scripts\activate

Install dependencies
pip install -r requirements.txt

Usage
Run the Streamlit app
streamlit run app.py

Use the interface
Enter your personal and health information in the input fields
Click the Predict button to see the estimated insurance cost

## How It Works
Input Handling
Inputs from the Streamlit form are collected as a dictionary
Numerical inputs: Age, Income, Number of Dependants, Genetical Risk
Categorical inputs: Gender, Marital Status, BMI, Smoking Status, Employment Status, Region, Medical History, Insurance Plan

Preprocessing
The preprocess_input function converts categorical inputs into one-hot encoded columns
A normalized risk score is calculated from the medical history
Features are scaled using pre-loaded scalers (scaler_young or scaler_rest) depending on age

Prediction
Two separate models are used:
model_young → for age ≤ 25
model_rest → for age > 25
The predict function returns the predicted insurance cost
