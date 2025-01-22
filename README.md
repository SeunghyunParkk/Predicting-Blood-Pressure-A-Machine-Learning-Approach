# Predicting Blood Pressure: A Machine Learning Approach

## Overview
This project leverages machine learning techniques to predict an individual's blood pressure based on health indicators and lifestyle factors. By identifying key contributors to high blood pressure, this project aims to support early intervention strategies and reduce the risk of cardiovascular diseases.

---

## Objective
The main objective is to develop machine learning models that predict blood pressure using a combination of personal, health, and lifestyle factors. This project hypothesizes that features such as age, BMI, stress level, physical activity, and sleep quality significantly influence blood pressure levels.

---

## Dataset and Features

### Data Description
- **Dataset Size**: 374 entries
- **Key Features**:
  - **Personal Information**:
    - `Person ID`: Unique identifier for individuals
    - `Age`: Individual's age
    - `Gender`: Binary variable representing gender
  - **Health Indicators**:
    - `Blood Pressure`: Systolic and diastolic readings
    - `Heart Rate`: Resting heart rate
    - `BMI Category`: Categorized Body Mass Index
    - `Stress Level`: Scale from 1 to 10
  - **Lifestyle and Occupational Data**:
    - `Physical Activity Level`: Daily or regular physical activity level
    - `Daily Steps`: Average daily steps
    - `Occupation`: Profession categories such as Nurse, Teacher, etc.
    - `Sleep Duration`: Average hours of sleep per day
    - `Quality of Sleep`: Rated sleep quality
    - `Sleep Disorder`: Binary indicator for sleep disorders

---

## Methodology

### Preprocessing
1. **Data Cleaning**:
   - Handled missing values using imputation.
   - Encoded categorical features for model compatibility.
2. **Feature Scaling**:
   - Standardized numerical variables for consistent model inputs.
3. **Exploratory Data Analysis**:
   - Visualized relationships between variables using pairplots and heatmaps.
   - Identified key predictors of blood pressure through feature correlation.

### Machine Learning Models
1. **Random Forest**:
   - Utilized for its ability to capture complex interactions.
2. **Ridge Regression**:
   - Tested for linear relationships with regularization.
3. **Model Evaluation**:
   - Metrics: Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R-squared (R²)

---

## Results

### Model Performance
- **Random Forest**:
  - R²: [value]
  - RMSE: [value]
- **Ridge Regression**:
  - R²: [value]
  - RMSE: [value]

### Key Insights
- Features like `Stress Level`, `Age`, and `BMI Category` were identified as strong predictors of blood pressure.
- Lifestyle factors such as `Physical Activity` and `Quality of Sleep` also contributed significantly.

---

## Future Work
- Incorporate additional data to improve generalizability.
- Experiment with advanced models such as Gradient Boosting or Neural Networks.
- Conduct real-world testing to validate predictions.


