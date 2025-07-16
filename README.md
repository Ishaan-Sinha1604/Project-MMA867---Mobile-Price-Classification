# Project-MMA867---Mobile-Price-Classification
This project tackles a multi-class classification problem to predict the **price range of mobile phones** using technical specifications. We applied a combination of **Logistic Regression**, **Principal Component Analysis (PCA)**, and **StandardScaler** for dimensionality reduction and optimization.

---

## 🧠 Project Overview

- **Objective**: Predict one of four price categories (0–3) for mobile phones based on 20+ features such as RAM, battery power, internal memory, and camera specs.
- **Approach**: Build a classification pipeline using preprocessing, dimensionality reduction (PCA), and penalized logistic regression with `l1` regularization.
- **Outcome**: Achieved **~98% accuracy** on the test set using an 18-component PCA model and L1-penalized logistic regression.

---

## 📁 Repository Structure

.
├── Mobile_Price_Classification.ipynb # Main notebook with code
├── train.csv # Training dataset
├── test.csv (optional) # Test dataset for deployment
├── README.md # Project summary and usage guide

markdown
Copy
Edit

---

## 🔬 Features & Methods

### 📊 Data Exploration & Cleaning
- Checked for missing values and duplicate columns
- Visualized distribution using histograms
- Computed Pearson correlation matrix with heatmaps

### ⚙️ Preprocessing & Transformation
- **StandardScaler** applied to features before PCA
- **Variance Inflation Factor (VIF)** used to inspect multicollinearity
- Dimensionality reduced using **Principal Component Analysis (PCA)**
  - Chose **18 principal components** to retain >96% variance
  - Visualized explained variance using line plots

### 📈 Modeling
- **Baseline Model**: Logistic Regression without scaling → ~65% accuracy
- **Improved Model**: 
  - Scaled + PCA-transformed data
  - Logistic Regression with L1 regularization (`C=100`)
  - Achieved:
    - **Train Accuracy**: 98.7%
    - **Test Accuracy**: 97.8%

### 📊 Evaluation Metrics
- **Confusion Matrix**: 150 samples in each of 4 classes (0–3)
- **Classification Report**:
  - Precision, Recall, F1-Score: **~0.98 for all classes**
- Visualized top PCA component weights and indicator coefficients

---

## 🛠️ Technologies Used

- **Language**: Python
- **Libraries**:
  - `pandas`, `numpy` – Data manipulation
  - `matplotlib`, `seaborn` – Data visualization
  - `sklearn` – Logistic Regression, PCA, preprocessing, metrics
  - `statsmodels` – VIF calculation

---

## 📊 Final Classification Report

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
|   0   |   0.97    |  0.98  |   0.98   |   150   |
|   1   |   0.97    |  0.96  |   0.97   |   150   |
|   2   |   0.97    |  0.99  |   0.98   |   150   |
|   3   |   0.99    |  0.99  |   0.99   |   150   |
| **Overall** |       |        | **0.98** | **600** |

---

## 📌 Conclusion

- Logistic Regression performs exceptionally well on PCA-reduced feature space.
- Feature scaling and dimensionality reduction significantly improved model performance.
- The model is efficient, interpretable, and highly accurate for this classification task.

---
