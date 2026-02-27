# 🎓 Student Exam Score Prediction

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Scikit--Learn-ML-orange?style=for-the-badge&logo=scikitlearn" />
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Type-Regression-informational?style=for-the-badge" />
</p>

---

## 📌 Project Overview

This project predicts **Student Exam Scores** using supervised machine learning. It analyzes academic, behavioral, socioeconomic, and lifestyle factors to build accurate regression models.

📊 Dataset: *Student Performance Factors (Kaggle)*
🎯 Target Variable: `Exam_Score`

---

## 🚀 Project Workflow

### 🔹 Data Processing

* Missing value imputation (mode)
* One-Hot Encoding for categorical features
* StandardScaler for numerical features
* Preprocessing pipelines using `ColumnTransformer`

### 🔹 Exploratory Data Analysis

* Feature distributions & count plots
* Feature vs target visualizations
* Correlation analysis
* Regression plots

### 🔹 Modeling

Models evaluated:

* Linear Regression
* Ridge Regression
* Lasso Regression
* Random Forest
* Gradient Boosting

Evaluation Metrics:

* R² Score
* MAE
* RMSE
* 5-Fold Cross Validation

---

## 📊 Final Model Performance

| Model             | R²         | MAE       | RMSE      |
| ----------------- | ---------- | --------- | --------- |
| 🏆 **Ridge**      | **0.7697** | **0.452** | **1.804** |
| Linear            | 0.7696     | 0.452     | 1.804     |
| Gradient Boosting | 0.7309     | 0.819     | 1.950     |
| Lasso             | 0.7043     | 0.994     | 2.045     |
| Random Forest     | 0.6526     | 1.165     | 2.216     |

---

## 🏆 Best Model: Ridge Regression

✔ Explains ~77% of variance
✔ Lowest prediction error
✔ Handles multicollinearity
✔ Highly interpretable

---

## 💡 Key Insights

* The problem is predominantly **linear**.
* Adding relevant features improves performance more than increasing model complexity.
* Polynomial expansion did not significantly improve results.
* Tree-based models did not outperform linear models.

---

## 💾 Model Artifacts

All trained pipelines (preprocessing + model) are saved using `joblib`.

```
models/
    linear.pkl
    ridge.pkl
    lasso.pkl
    random_forest.pkl
    gradient_boosting.pkl
    fitted_pipelines.pkl
```

Load a saved model:

```python
import joblib
model = joblib.load("models/ridge.pkl")
predictions = model.predict(X_new)
```

---

## 🛠 Tech Stack

* Python
* Pandas & NumPy
* Matplotlib & Seaborn
* Scikit-learn
* Joblib

---

## 🧠 Skills Demonstrated

`Regression` • `Feature Engineering` • `Model Evaluation` • `Cross-Validation` • `Pipelines` • `Regularization`

---

## 📌 Conclusion

This project demonstrates a complete end-to-end regression workflow — from data exploration to deployment-ready model serialization. Ridge Regression proved to be the most stable and accurate approach for predicting student exam performance.

---

