# Heart Disease Prediction Using Machine Learning

## Project Overview

This project applies machine learning techniques to predict the presence of heart disease based on clinical patient data.

The project follows a complete machine learning workflow:

- Data Understanding
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Model Training
- Model Evaluation

## Dataset

**Source:** [Heart Failure Prediction Dataset (Kaggle)](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction/data)

The dataset contains clinical features related to heart health, including:

- Age
- Sex
- Chest Pain Type
- Resting Blood Pressure
- Cholesterol
- Fasting Blood Sugar
- Resting ECG
- Maximum Heart Rate
- Exercise Angina
- ST Slope

## Data Cleaning

- Invalid zero values in `Cholesterol` and `RestingBP` were identified and replaced with the median value of each column.

## Data Preprocessing

The following preprocessing steps were applied:

- Handling categorical variables using One-Hot Encoding
- Splitting data into training and testing sets (80/20, stratified by target)
- Feature scaling using StandardScaler for Logistic Regression
- Tree-based models (Decision Tree and Random Forest) were trained without scaling since they do not require feature scaling

## Machine Learning Models

Three classification models were trained and evaluated:

1. Logistic Regression
2. Decision Tree
3. Random Forest

## Model Performance

| Model | Accuracy | Recall | F1-score |
|------|----------|--------|----------|
| Logistic Regression | 87% | 89% | 88% |
| Random Forest | 85% | 86% | 87% |
| Decision Tree | 79% | 76% | 80% |

Recall was given particular attention in this comparison, since in medical prediction tasks it reflects the model's ability to correctly identify patients who actually have heart disease.

## Feature Importance

The Random Forest model was used to identify important features.

The most influential features included:

- ST_Slope
- MaxHR
- Age
- Cholesterol
- ExerciseAngina

## Tools & Libraries

Python libraries used:

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

## Project Structure
heart-disease-prediction-ml/

├── heart-disease-prediction-ml.ipynb
├── logistic_regression_heart_model.pkl
├── data/
│   └── heart.csv
├── requirements.txt
└── README.md

## How to Run

1. Install the required dependencies:
​```
pip install -r requirements.txt
​```
2. Open the notebook:
​```
heart-disease-prediction-ml.ipynb
​```
3. Run the cells in order.