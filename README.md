# ICE CREAM SALES PREDICTOR — LINEAR AND POLYNOMIAL REGRESSION MODELS

---

## 1. INTRODUCTION

The **Ice Cream Sales Predictor** is a machine learning-based web application designed to forecast ice cream sales using temperature data.  
This project utilizes **Linear Regression** and **Polynomial Regression** to analyze how temperature impacts sales trends.  
It integrates data preprocessing, model training, evaluation, and visualization into an interactive web interface powered by **Streamlit**.

The goal is to demonstrate how regression models can be implemented to solve real-world prediction problems effectively.

---

## 2. OBJECTIVE

The main objectives of this project are:

- To predict ice cream sales based on temperature input using regression techniques.  
- To evaluate model accuracy and performance using statistical measures.  
- To compare Linear and Polynomial Regression models for better understanding.  
- To visualize regression trends and predictions interactively.  
- To deploy a fully functional predictive web application using Streamlit.

---

## 3. DATASET INFORMATION

The dataset **`Ice Cream Sales and Temperature.csv`** is used for training and testing.  
It contains temperature (°C) values and corresponding sales values (in units).

| Temperature (°C) | Sales |
|------------------|-------|
| 20 | 150 |
| 22 | 200 |
| 25 | 350 |
| 27 | 500 |
| 30 | 700 |
| 32 | 1000 |
| 35 | 1350 |

This dataset demonstrates a **non-linear relationship**, making Polynomial Regression suitable.

---

## 4. METHODOLOGY

### 4.1 Data Preprocessing
- The dataset is imported using **Pandas**.
- Missing or non-numeric values are handled.
- Data is split into input (`X`) and output (`y`) variables.

### 4.2 Model Development
Two models are implemented:
1. **Linear Regression:** Fits a straight line (y = mx + c).
2. **Polynomial Regression:** Fits a curved line (y = a₀ + a₁x + a₂x² + ...).

The best polynomial degree (1–12) is automatically determined based on the **R² score**.

### 4.3 Evaluation Metrics
Models are evaluated using:
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score (Coefficient of Determination)**
- **Cross-Validation R²**

### 4.4 Prediction
Users can input temperature values to predict sales in real-time.  
Predicted results are displayed with “sales” labels and stored in session history.

### 4.5 Visualization
Graphical plots generated using **Plotly** include:
- Actual data points  
- Linear regression line  
- Polynomial regression curve  
- Highlighted prediction point  

### 4.6 Model Persistence
- Trained polynomial model can be saved (`best_model.pkl`).
- The saved model can be reloaded for future predictions.

---

## 5. SYSTEM REQUIREMENTS

| Component | Specification |
|------------|----------------|
| Programming Language | Python 3.8 or higher |
| Framework | Streamlit |
| Libraries | Pandas, NumPy, Scikit-learn, Plotly, Joblib |
| Browser | Chrome / Edge / Firefox |
| OS | Windows / macOS / Linux |

---

## 6. PROJECT STRUCTURE
IceCream-Sales-Predictor/
│
├── app.py # Main Streamlit application
├── run_app.py # Auto-launcher script
├── run.bat # Windows launcher
├── requirements.txt # Python dependencies
├── Ice Cream Sales and Temperature.csv # Dataset file
├── best_model.pkl # Saved trained model
└── README.md # Project documentation


