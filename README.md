# Employee Attrition Analytics

An end-to-end machine learning project that analyzes employee attrition using a dataset of 20,000 employee records. The project covers exploratory data analysis, classification modeling to predict attrition, K-Means clustering to segment the workforce, and regression modeling to understand income drivers.

## Project Overview

Employee attrition is one of the costliest problems an HR team deals with — replacing an employee can cost anywhere from 50% to 200% of their annual salary once recruiting, onboarding, and lost productivity are accounted for. This project builds a complete analytics pipeline to help answer three questions:

- **Who is likely to leave?** — solved with classification models (Logistic Regression, Decision Tree, Random Forest)
- **What natural groups exist in the workforce, and which group is riskiest?** — solved with K-Means clustering
- **What drives an employee's income?** — solved with regression models (Linear Regression, Random Forest Regressor)

## Repository Structure

```
employee-attrition-analytics/
│
├── Datasets/
│   ├── capstone_employee_attrition_dataset.csv    # Raw dataset (20,000 records, 29 columns)
│   └── capstone_data_dictionary.csv               # Column definitions and data types
│
├── Docs/
│   ├── Capstone_Problem_Statement_and_Data_Dictionary.pdf   # Original problem statement
│   └── Project_Workflow_Report.pdf                          # Concept-level write-up of the full workflow
│
├── Output_Plots/
│   ├── attrition_overview.png          # Overall & department-wise attrition rate
│   ├── correlation_matrix.png          # Correlation heatmap of numeric features
│   ├── income_overtime_attrition.png   # Income & overtime vs attrition
│   ├── confusion_matrix_lr.png         # Confusion matrix — Logistic Regression
│   ├── roc_curves.png                  # ROC curves — all classification models
│   ├── feature_importance.png          # Top features driving attrition (Random Forest)
│   ├── elbow_curve.png                 # Elbow method for choosing k
│   ├── silhouette_scores.png           # Silhouette score vs k
│   └── cluster_attrition.png           # Attrition rate by cluster
│
├── employee-attrition-analytics.py     # Full project code (EDA → preprocessing → modeling)
└── README.md
```

## Dataset

- **Source file:** `capstone_employee_attrition_dataset.csv`
- **Size:** 20,000 employee records, 29 columns
- **Target variable:** `attrition` (Yes / No)
- **Data dictionary:** see `Datasets/capstone_data_dictionary.csv` for full column definitions

## Workflow

1. **Exploratory Data Analysis** — overall and department-wise attrition rate, correlation analysis, income/overtime vs attrition
2. **Preprocessing** — feature/target split, scaling (StandardScaler), encoding (OneHotEncoder), stratified train-test split
3. **Classification** — Logistic Regression, Decision Tree, and Random Forest, evaluated on precision, recall, F1-score, and ROC-AUC; hyperparameter tuning via GridSearchCV
4. **Model Interpretation** — confusion matrix, ROC curve comparison, Random Forest feature importance
5. **Clustering** — K-Means with elbow method and silhouette score to choose the optimal number of clusters, followed by attrition-rate-by-cluster analysis
6. **Regression** — Linear Regression and Random Forest Regressor to predict monthly income and identify its strongest drivers

A full concept-level explanation of each step and why it was done is available in `Docs/Project_Workflow_Report.pdf`.

## Tech Stack

- **Language:** Python
- **Libraries:** pandas, NumPy, scikit-learn, matplotlib, seaborn
- **Environment:** Google Colab

## How to Run

1. Clone the repository
   ```
   git clone https://github.com/<your-username>/employee-attrition-analytics.git
   ```
2. Open `employee-attrition-analytics.py` in Google Colab or your local Python environment
3. Make sure `capstone_employee_attrition_dataset.csv` (from the `Datasets/` folder) is available in the working directory
4. Run the script/notebook cells from top to bottom

## Key Outputs

All generated charts are available in the `Output_Plots/` folder, including attrition breakdowns, the correlation heatmap, confusion matrix, ROC curves, feature importance ranking, and clustering diagnostics (elbow curve, silhouette scores, cluster-wise attrition).

## Author

**Swaroop Kumar Vathada**
Data Analyst | BI Developer

🔗 [LinkedIn](https://www.linkedin.com/in/swaroopkumarvathada)
