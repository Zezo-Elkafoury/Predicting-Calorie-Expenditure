# 🏋️‍♂️ Predicting Calorie Expenditure using Machine Learning

This notebook builds a machine learning model to predict **calorie expenditure** based on physiological and workout data, as part of the Kaggle competition **"Predict Calorie Expenditure"**.

---

## 📊 Dataset
- **Train CSV:** Contains features like Age, Sex, Height, Weight, Duration, Heart Rate, Body Temperature and the target variable (*Calories*).
- **Test CSV:** Contains similar features without the target (*Calories*) — your model must predict these.
- **Sample Submission CSV:** Shows the expected submission format.

---

## ✅ Workflow Overview
1. **Data Loading & Inspection**
   - Read datasets
   - Check shapes, info, and distributions (especially the target `Calories`).

2. **Data Cleaning & Preprocessing**
   - Handle missing values.
   - Encode categorical column `Sex`.
   - Feature Engineering:
     - Created new features like BMI, HR per minute, Temperature per minute, Effort score, Age-Weight interaction, etc.
   - Scaled numerical features using `StandardScaler`.

3. **Target Transformation**
   - Applied log transformation (`np.log1p`) to `Calories` to handle right skewness and improve model performance.

4. **Model Training with K-Fold Cross Validation**
   - Used **5-Fold Cross Validation** to train and evaluate the model for more reliable performance estimation.
   - Model: **XGBoost Regressor** with tuned hyperparameters.
   - Evaluation Metric: **Root Mean Squared Log Error (RMSLE)**.

5. **Test Predictions and Submission**
   - Averaged predictions from all folds (blending) for test set.
   - Applied inverse log transformation (`np.expm1`).
   - Saved the submission file in the correct format.

---

## 🚀 Model Highlights
- **Algorithm:** XGBoost Regressor
- **Metric:** RMSLE (Root Mean Squared Log Error)
- **Features Used:** Original features + engineered features (BMI, Effort, HR per min, etc.)

---

## 📂 Submission
- Submission file `submission.csv` includes:
  - **ID** column from the sample submission
  - Predicted **Calories**


