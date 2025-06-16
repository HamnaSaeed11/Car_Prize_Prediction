# 🚗 Car Price Classification

A machine learning project designed to predict whether a car's price is **above** or **below** the median value based on its features. This project explores various preprocessing techniques, visualization methods, and classification algorithms to build an accurate price prediction model.

---

## 📁 Dataset

- **Source**: `CarPricesPrediction.csv`
- **Rows**: 1000
- **Features**:
  - `Make` (e.g., Toyota, Ford)
  - `Model` (e.g., Civic, Altima)
  - `Year` (e.g., 2016)
  - `Mileage` (miles driven)
  - `Condition` (e.g., Excellent, Good)
  - `Price` (in USD)

---

## 📊 Workflow

### 1. Data Preprocessing
- Removed outliers using **IQR** method on `Mileage` and `Price`
- Normalized numeric columns using **MinMaxScaler**
- Encoded categorical columns using **LabelEncoder**
- Created binary target variable `Price_Class`:
  - `0` = Price below median
  - `1` = Price above median
- Handled class imbalance using **SMOTE**

### 2. Visualizations
- Correlation heatmap
- Pairplot colored by `Condition`
- Boxplots (before & after outlier removal)
- Count plots of class distributions
- Confusion matrices & ROC curves

### 3. Model Training
Trained and evaluated 3 classification algorithms:
- **Logistic Regression**
- **Support Vector Machine (SVM)**
- **K-Nearest Neighbors (KNN)**

---

## 🏆 Results

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC | MCC  |
|--------------------|----------|-----------|--------|----------|---------|------|
| Logistic Regression| 100%     | 1.00      | 1.00   | 1.00     | 1.00    | 1.00 |
| KNN                | 93%      | 0.93      | 0.93   | 0.93     | 0.97    | 0.86 |
| SVM                | 90%      | 0.90      | 0.90   | 0.90     | 0.50    | 0.80 |

✅ **Best Model**: Logistic Regression with perfect evaluation metrics.

---

## 🛠️ Tools & Libraries

- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib
- imbalanced-learn (SMOTE)

---



