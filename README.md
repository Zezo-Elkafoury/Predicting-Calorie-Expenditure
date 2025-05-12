# 🏋️‍♂️ Calories Burned Prediction (Regression Project)

This project predicts the number of calories burned based on features like age, weight, height, heart rate, and body temperature using machine learning models for a kaggle competition.

---

## 📊 Dataset Columns
- **Sex**
- **Age**
- **Height**
- **Weight**
- **Duration**
- **Heart_Rate**
- **Body_Temp**
- **Calories** (Target)

---

## 🚀 Workflow Steps

### 1. 📚 Data Preprocessing
- Checked missing values (none ✅)
- Created new features like:
  - **BMI** (Body Mass Index)
  - **Effort** (Heart Rate * Body Temp * Duration)
  - And other interaction features!

### 2. 🔥 Models Used
- **CatBoost Regressor**
- **XGBoost Regressor**

### 3. 🎯 Cross-Validation
- Used **K-Fold Cross Validation** (no data leakage)
- Target was transformed using `log1p()` for better RMSLE performance

### 4. ⚡ Ensembling
- Optimized the blend of CatBoost and XGBoost predictions
- Used **scipy minimize** to find best weights minimizing RMSLE

### 5. 📈 Final Submission
- Predictions blended and transformed back using `expm1()`
- Ready for submission!

---

## 📦 Key Techniques Used
- ✅ Feature Engineering
- ✅ K-Fold Cross-Validation
- ✅ Log-transform Target
- ✅ Model Ensembling (weight optimization)

---

## 🏅 Goal
Maximize Kaggle leaderboard score (minimize **RMSLE**) by blending multiple models and smart feature engineering.
