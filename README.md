# Predicting Blood Pressure: A Machine Learning Approach

## Overview
This project explores the use of machine learning models to predict systolic and diastolic blood pressure using health indicators and lifestyle factors. By identifying key features such as BMI, occupation, and physical activity levels, the goal is to provide actionable insights for healthcare and early intervention strategies.

---

## Hypothesis
The hypothesis is that personal, health, and lifestyle factors, such as age, BMI, stress levels, physical activity, and sleep quality, significantly influence blood pressure. The project investigates these relationships and evaluates their predictive power in machine learning models.

---

## Dataset and Preprocessing

### Dataset Summary
- **Size**: 374 entries
- **Features**:
  - **Personal Information**: `Age`, `Gender`
  - **Health Indicators**: `Blood Pressure`, `Heart Rate`, `BMI Category`, `Stress Level`
  - **Lifestyle Factors**: `Daily Steps`, `Sleep Duration`, `Quality of Sleep`, `Physical Activity Level`
  - **Occupational Data**: Professions such as `Accountant`, `Lawyer`, `Nurse`

### Preprocessing Steps
1. **Feature Engineering**:
   - Created `BP_Difference` (Difference between systolic and diastolic blood pressure).
   - Added `Steps_per_Age` (Ratio of daily steps to age).
2. **Correlation Analysis**:
   - Removed redundant features (`Stress Level`, `Quality of Sleep`, and `Diastolic_BP`) based on high correlations with other variables.
3. **Encoding**:
   - Label Encoding for `Gender` and `BMI Category`.
   - One-Hot Encoding for `Occupation` and `Sleep Disorder`.

---

## Methodology

### Model Selection
The following models were chosen to handle different aspects of the data:
1. **Ridge Regression**:
   - Effective for multicollinear data due to regularization.
   - Tuned using Grid Search for optimal `alpha` values.
2. **Random Forest Regressor**:
   - Captures complex, non-linear relationships.
   - Optimized with Grid Search for `n_estimators`, `max_depth`, and `min_samples_split`.

### Model Development Process
1. **Baseline Model**:
   - A simple linear regression model was used as the baseline for comparison.
2. **Grid Search Optimization**:
   - Parameters for Ridge Regression (`alpha`) and Random Forest (`n_estimators`, `max_depth`, `min_samples_split`) were optimized using 5-fold cross-validation.
3. **Re-Evaluation Without `BP_Difference`**:
   - Due to its dominance in the feature importance analysis, the model was retrained without `BP_Difference` to test the predictive strength of other variables.

### Feature Importance Analysis
The Random Forest model revealed the following key insights:
1. **BMI_Category_encoded**:
   - Most influential predictor, emphasizing the role of body weight in blood pressure control.
2. **Occupation_Accountant**:
   - Highlighted the potential impact of occupational stress on blood pressure.
3. **Physical Activity Level**:
   - Consistently linked to healthier blood pressure levels.

---

## Results

### Model Performance
1. **Ridge Regression**:
   - RMSE: 2.21
   - Best `alpha`: 1
2. **Random Forest**:
   - RMSE: 0.6685
   - Best Parameters:
     - `n_estimators`: 100
     - `max_depth`: 10
     - `min_samples_split`: 5

### Re-Evaluation Insights
- Excluding `BP_Difference` improved the model's robustness by emphasizing other influential features.
- **Adjusted Random Forest**:
  - Test RMSE: 0.6685
  - Key predictors included BMI, physical activity, and occupation.

---

## Conclusion
The Random Forest model emerged as the most effective for predicting blood pressure, achieving a Test RMSE of 0.6685. Key findings include:
- **BMI** as the most significant predictor, reaffirming its critical role in blood pressure control.
- **Occupational stress**, particularly in professions like accounting and nursing, is strongly associated with elevated blood pressure.
- **Physical activity** and age-adjusted metrics provide additional predictive power.

These insights pave the way for personalized healthcare solutions, emphasizing weight management, stress reduction, and regular physical activity as vital interventions.

---

## Future Directions
1. **Expand Dataset**:
   - Collect larger, diverse samples to improve generalizability.
2. **Add Features**:
   - Include dietary habits and genetic factors for deeper analysis.
3. **Real-World Applications**:
   - Integrate findings into wearable health monitoring devices.
