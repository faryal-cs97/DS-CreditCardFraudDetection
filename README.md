# DS-CreditCardFraudDetection
# Credit Card Fraud Detection - Exploratory Data Analysis (EDA)

## Project Overview
This repository contains a detailed Exploratory Data Analysis (EDA) on the Credit Card Fraud Detection dataset. The aim is to uncover patterns, anomalies, and key insights into fraudulent transactions to lay a strong foundation for building fraud detection models. 

### Dataset Information
- **Dataset Name:** Credit Card Fraud Detection Dataset
- **Source:** [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Dataset Summary:**
  - Total Rows: 284,807
  - Total Columns: 31
  - Features: Anonymized (V1 to V28), `Time`, `Amount`, and `Class` (indicating fraud or legitimate transaction).

---

## Objectives
1. Explore and understand the dataset structure and quality.
2. Identify patterns and correlations distinguishing fraudulent from legitimate transactions.
3. Detect and handle outliers to improve data quality.
4. Generate actionable insights and visualizations to guide further modeling.

---

## Key Insights
### Before Outlier Removal
1. **Dataset Dimensions:** Rows: 284,807 | Columns: 31
2. **Data Types:**
   - Numerical: All features (`float64`), except `Class` (binary).
3. **Missing Values:** None detected.
4. **Class Distribution:**
   - Legitimate: 284,315 (~99.83%)
   - Fraudulent: 492 (~0.17%)
5. **Transaction Amount (Statistical Summary):**
   - Min: 0 | Max: 25,691.16 | Mean: 88.35 | Median: 22.00
6. **Maximum Transaction:**
   - 25,691.16 (Legitimate transaction).
7. **Visualizations:**
   - Bar Chart: Class imbalance visualized.
   - Histogram: Right-skewed transaction amounts.
   - Heatmap: Correlations inflated due to outliers.

### After Outlier Removal
1. **Improved Data Representation:**
   - Reduced the influence of extreme values on statistical summaries.
   - Clearer patterns in mid-range transaction amounts.
2. **Visualizations:**
   - Histogram: Less skewed distribution.
   - Heatmap: Stabilized correlations reveal genuine feature relationships.
3. **Fraud Insights:**
   - Fraudulent transactions correlate more with anonymized features rather than extreme transaction amounts.

---

## Repository Structure
```plaintext
.
├── data
│   ├── creditcard.csv            # Dataset file
├── notebooks
│   ├── eda_credit_card_fraud.ipynb  # Jupyter Notebook with EDA
├── visuals
│   ├── bar_chart.png             # Bar chart for class distribution
│   ├── histogram_amount.png      # Histogram of transaction amounts
│   ├── heatmap_correlation.png   # Heatmap of feature correlations
├── README.md
```

---

## Requirements
### Dependencies
Install the necessary packages using:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## Project Workflow
1. **Data Loading:**
   - Import the dataset and perform initial exploration.
2. **Data Cleaning:**
   - Detect and remove outliers using the Interquartile Range (IQR) method.
3. **Exploratory Data Analysis:**
   - Generate descriptive statistics.
   - Visualize patterns using bar charts, histograms, and heatmaps.
4. **Insights and Recommendations:**
   - Summarize findings for feature engineering and preprocessing.

---

## Results and Recommendations
- **Fraud Patterns:** Fraudulent transactions are influenced by specific anonymized features rather than transaction amounts.
- **Class Imbalance:** Use techniques like SMOTE or undersampling to balance the dataset before modeling.
- **Preprocessing:** Remove outliers and standardize features for better model performance.

---


### References
- Dataset: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- Scikit-learn Documentation: [https://scikit-learn.org](https://scikit-learn.org)

