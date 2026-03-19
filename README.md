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
