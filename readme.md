# 🎓 Student Exam Score Prediction  
### Machine Learning Regression Project

---

## 📌 Project Overview

This project focuses on predicting students’ **Exam Scores** using supervised Machine Learning techniques. The objective is to analyze academic, behavioral, and lifestyle factors affecting student performance and develop regression models to estimate final exam results.

The dataset used in this project was sourced from **Kaggle**.

---

## 🎯 Project Objectives

- Perform data cleaning and preprocessing  
- Conduct comprehensive Exploratory Data Analysis (EDA)  
- Develop Linear Regression models  
- Implement Polynomial Regression  
- Compare multiple feature combinations  
- Evaluate model performance using regression metrics  
- Interpret insights from model results  

---

## 📂 Dataset Information

**Dataset:** Student Performance Factors  
**Source:** Kaggle  
**Target Variable:** `Exam_Score`

---

## 🛠 Tools & Technologies

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  

---

## 🔎 Methodology

### 1️⃣ Data Cleaning
- Inspected dataset structure and summary statistics  
- Identified missing values  
- Imputed categorical missing values using mode  
- Verified data consistency  

---

### 2️⃣ Exploratory Data Analysis (EDA)
- Distribution analysis of categorical and numerical features  
- Bar plots comparing feature impact on exam score  
- Histogram & KDE visualization of score distribution  
- Regression plots for numerical variables  
- Correlation analysis using one-hot encoded dataset  

---

### 3️⃣ Model Development

Linear regression models were built with some changes and compared:

| Model | Features Used |
|-------|--------------|
| Model 1 | Hours_Studied |
| Polynomial Model 1 | Hours_Studied (Degree 2) |
| Model 2 | Hours_Studied, Attendance |
| Model 2 (Polynomial) | Degree 2 transformation |
| Model 3 | Hours_Studied, Attendance, Previous_Scores |
| Model 3 (Polynomial) | Degree 2 transformation |

---

## 📊 Model Performance Results

The models were evaluated using:

- **MAE** (Mean Absolute Error)  
- **MSE** (Mean Squared Error)  
- **RMSE** (Root Mean Squared Error)  
- **R² Score** (Coefficient of Determination)  

### 🔬 Final Comparison Table

| Model | MAE | MSE | RMSE | R² Score |
|-------|------|------|--------|----------|
| Model 3 | 1.359207 | 5.338274 | 2.310471 | 0.622338 |
| Model 3 (Polynomial) | 1.358279 | 5.341410 | 2.311149 | 0.622117 |
| Model 2 | 1.468964 | 5.809117 | 2.410211 | 0.589028 |
| Model 2 (Polynomial) | 1.467214 | 5.812159 | 2.410842 | 0.588813 |
| Polynomial Model 1 | 2.444780 | 10.844988 | 3.293173 | 0.232760 |
| Model 1 | 2.447569 | 10.855921 | 3.294833 | 0.231987 |

---

## 🏆 Best Performing Model

### ✅ Model 3 (Linear Regression)

- **Highest R² Score:** 0.622338  
- **Lowest error metrics overall**  
- Explains approximately **62% of the variance** in exam scores  

### Key Insight:
Polynomial transformations did **not** significantly improve performance, indicating that the relationship between selected features and exam score is predominantly **linear**.

Increasing feature relevance had a greater impact than increasing model complexity.

---

## 📈 Visualizations Included

- Feature distribution plots  
- Target variable distribution  
- Feature vs Target regression plots  
- Actual vs Predicted comparison graphs  
- Correlation analysis  
- Model performance comparison table  

---

## 🚀 Future Improvements

- Apply K-Fold Cross Validation  
- Implement Ridge and Lasso Regression  
- Try Tree-based models (Random Forest, Gradient Boosting)  
- Add clustering (K-Means) for student segmentation  
- Deploy as a Streamlit dashboard  

---

## 🧠 Skills Demonstrated

- Data Cleaning & Preprocessing  
- Exploratory Data Analysis  
- Regression Modeling  
- Polynomial Feature Engineering  
- Model Evaluation & Comparison  
- Analytical Interpretation of Results  

---

## 📦 How to Run the Project

```bash
# Clone the repository
git clone https://github.com/UFAQUE123/Student-Score-Prediction.git

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# Run the notebook or script
```

---
## Model Performance Insights

- Based on the comparative evaluation of all models using MAE, MSE, RMSE, and R² score, Model 3 (Linear Regression) demonstrates the best overall performance. It achieved the lowest error values (MAE = 1.359, RMSE ≈ 2.31) and the highest explanatory power (R² ≈ 0.622), indicating that it explains approximately 62% of the variance in exam scores.

- The polynomial version of Model 3 did not provide any meaningful improvement in predictive accuracy, as its performance metrics remained nearly identical and slightly lower in terms of R². A similar pattern is observed for Model 2 and its polynomial counterpart, where polynomial transformation does not enhance model performance.

- Model 1, both linear and polynomial, shows significantly weaker performance (R² ≈ 0.23), suggesting that it lacks sufficient predictive features to accurately model exam scores.

- Overall, the results indicate that the relationship between the selected features and the target variable is predominantly linear. Increasing model complexity through polynomial transformation does not improve performance and may introduce unnecessary complexity. Therefore, Model 3 (Linear Regression) is the most appropriate and efficient model for predicting exam scores in this analysis.
