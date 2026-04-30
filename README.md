# 🚕 Taxi Price Prediction (Regression Project)

## 📌 Overview
This project focuses on predicting taxi trip prices using regression techniques. The goal is to build a machine learning model that can accurately estimate the fare of a trip based on features like distance, duration, and pricing rates.

---

## 📂 Dataset
The dataset contains the following features:

- Trip_Distance_km  
- Time_of_Day  
- Day_of_Week  
- Passenger_Count  
- Traffic_Conditions  
- Weather  
- Base_Fare  
- Per_Km_Rate  
- Per_Minute_Rate  
- Trip_Duration_Minutes  
- Trip_Price (Target Variable)

---

## 🎯 Objective
To build a regression model that predicts taxi fare (`Trip_Price`) based on trip-related features.

---

## 🧱 Project Workflow

### 🔹 Task 1: Exploratory Data Analysis (EDA)
- Analyzed dataset structure and data types  
- Checked missing values  
- Visualized distributions using Plotly  
- Explored relationships between features and target  
- Identified trends and anomalies  

---

### 🔹 Task 2: Data Preparation
- Handled missing values:
  - Numerical → filled with median  
  - Categorical → filled with mode  
- Dropped rows with missing target values  
- Applied One-Hot Encoding for categorical features  
- Prepared clean dataset for modeling  

---

### 🔹 Task 3: Feature Engineering
- Created new features:
  - Distance_Cost = Trip_Distance_km × Per_Km_Rate  
  - Time_Cost = Trip_Duration_Minutes × Per_Minute_Rate  
  - Estimated_Total = Base_Fare + Distance_Cost + Time_Cost  
  - Speed_kmph  
- Removed data leakage feature: Price_per_Person  
- Performed correlation analysis  
- Selected important features  
- Removed low-importance features  

---

### 🔹 Task 4: Model Building & Comparison
Trained multiple regression models:

- Linear Regression  
- Decision Tree Regressor  
- Random Forest Regressor  
- Gradient Boosting Regressor  

Evaluation metrics used:
- MAE (Mean Absolute Error)  
- RMSE (Root Mean Squared Error)  
- R² Score  

Result:
- Gradient Boosting performed best with highest R² and lowest error  

---

### 🔹 Task 5: Model Improvement
- Performed residual analysis to understand model errors  
- Applied hyperparameter tuning using GridSearchCV  
- Used feature importance to remove weak features  
- Retrained model with optimized feature set  

---

### 🔹 Task 6: Results & Insights
- Trip distance is the most influential feature  
- Pricing is mainly driven by:
  - Distance  
  - Duration  
  - Rate components  
- Features like weather, time of day, and passenger count had minimal impact  
- Model achieved high accuracy (R² ≈ 0.94)  

---

## 📊 Final Model Performance (Example)

| Model              | R² Score | RMSE |
|-------------------|----------|------|
| Random Forest     | ~0.94    | Low  |
| Gradient Boosting | ~0.94+   | Lower |

---

## 🧠 Key Learnings
- Feature engineering significantly improves model performance  
- Ensemble models outperform basic models  
- Removing low-impact features simplifies the model without reducing accuracy  
- Real-world pricing logic can be effectively captured using ML  

---

## 🚀 Future Improvements
- Try advanced models like XGBoost or LightGBM  
- Add more real-world features (location, surge pricing, traffic index)  
- Use cross-validation for better generalization  
- Deploy model using Flask or Streamlit  

---

## 🛠️ Technologies Used
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Plotly  

---

## 📌 Conclusion
This project demonstrates how machine learning can be used to accurately predict taxi fares. The model aligns well with real-world pricing logic and can be extended for practical applications like ride-sharing platforms and fare estimation systems.
