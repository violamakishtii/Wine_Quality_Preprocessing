# Wine_Quality_Preprocessing
Machine Learning Course
# 🍷 Wine Quality Data Preprocessing Pipeline

This project focuses on building a complete **data preprocessing pipeline** for the Wine Quality dataset (`WineQT.csv`).  
It prepares the data for machine learning by handling missing values, outliers, encoding, feature engineering, scaling, and splitting.

---

## 📂 Dataset

- File: `WineQT.csv`
- Contains physicochemical properties of wine samples
- Target variable: `quality`

---

## ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 🚀 Pipeline Overview

### 1. Environment Setup
- Installs required libraries (for JupyterLite / Pyodide only)

---

### 2. Data Loading & Exploration
- Load dataset using Pandas
- Display:
  - Shape
  - First rows
  - Data types
  - Summary statistics

---

### 3. Data Cleaning

#### ✅ Missing Values
- Checked using `.isnull()`
- Handled using:
  - Median (numerical)
  - Mode (categorical)

#### ✅ Duplicates
- Removed duplicate rows if found

---

### 4. Outlier Handling
- Method: **IQR (Interquartile Range)**
- Outliers are **capped** (not removed) using `np.clip`

---

### 5. Feature Engineering

- Created new features:
  - `total_acidity = fixed acidity + volatile acidity`
- Binned alcohol levels:
  - `low`, `medium`, `high`
- Encoded binned values into numeric format

---

### 6. Encoding
- Label Encoding applied to categorical variables (if any)

---

### 7. Feature Selection

#### 📊 Correlation Analysis
- Correlation with target (`quality`) computed

#### 🧹 Low Variance Removal
- Removed features with variance < `0.01`

---

### 8. Data Visualization
- Correlation heatmap using Seaborn

---

### 9. Feature Scaling
- Standardization using `StandardScaler`
- Excluded:
  - `quality`
  - `Id`
  - non-numeric categorical features

---

### 10. Train-Test Split
- 80% Training / 20% Testing
- Stratified split based on `quality`

---

## 📈 Output

- Cleaned dataset
- Scaled feature matrix
- Train and test datasets ready for ML models

---

## 📊 Final Summary

- Dataset cleaned and preprocessed
- Features engineered and selected
- Ready for model training and evaluation

---

## ▶️ How to Run

1. Upload `WineQT.csv` into your working directory
2. Run all cells in order (Jupyter Notebook / JupyterLite)
3. Outputs will be displayed step-by-step

---

## 💡 Future Improvements

- Add machine learning models (e.g., Random Forest, XGBoost)
- Hyperparameter tuning
- Model evaluation metrics
- Deployment

---

## 👩‍💻 Author

Viola Makishti  
Business Informatics Student  

---

## ⭐ Notes

This project focuses on **data preprocessing**, which is a critical step before applying any machine learning model.
