
# Course Cancellation Prediction | Machine Learning

## Project Overview

This project was developed as part of the Introduction to Machine Learning course at Tel Aviv University.

The goal was to predict the probability of course registration cancellations using historical data and machine learning techniques.

The project follows the CRISP-DM framework, covering data exploration, preprocessing, feature engineering, model development, evaluation, and interpretation.

## Business Objective

Predicting course cancellations can help organizations:

- Identify high-risk registrations
- Improve resource planning
- Reduce operational uncertainty
- Support proactive customer engagement
- Make data-driven business decisions

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

- Analyzed historical course registration data
- Explored feature distributions and cancellation patterns
- Identified missing values and potential outliers
- Examined relationships between variables
- Created statistical visualizations

### 2. Data Preprocessing & Feature Engineering

- Handled missing values
- Cleaned categorical and numerical features
- Identified and treated implausible values
- Created business-oriented predictive features
- Applied feature encoding and selection
- Designed preprocessing pipelines to reduce data leakage

### 3. Machine Learning Models

Developed and compared four approaches:

- Logistic Regression
- Random Forest
- XGBoost
- Weighted Ensemble

Model tuning and evaluation incorporated temporal validation to better reflect real-world prediction scenarios.

### 4. Model Evaluation

Models were evaluated using:

- ROC-AUC
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

## Model Performance

| Metric | XGBoost |
|---|---|
| ROC-AUC | 0.8916 |
| Accuracy | 0.8003 |
| Precision | 0.7786 |
| Recall | 0.7338 |
| F1-Score | 0.7556 |

XGBoost achieved the highest ROC-AUC on the temporal validation set.

A weighted ensemble combining 85% XGBoost, 10% Random Forest, and 5% Logistic Regression also achieved competitive performance, with a ROC-AUC of 0.8915.

## Model Explainability

SHAP analysis was used to interpret model predictions and identify important features affecting cancellation risk.

The analysis highlighted factors including:

- Payment terms
- Registration lead time
- Previous course cancellations
- Customer characteristics
- Pre-course support activity

## Business Insights

The analysis grouped registrations into different predicted-risk categories.

Observed cancellation rates ranged from approximately:

- 5.6% in the low-risk group
- 93.9% in the high-risk group

These findings demonstrate how machine learning predictions can support operational prioritization.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost
- SHAP
- Jupyter Notebook

## How to Run

1. Open the Jupyter Notebook.

2. Install the required libraries:

   ```bash
   pip install numpy pandas matplotlib scipy scikit-learn xgboost shap
   ```

3. Place the required datasets in the same directory:

   - `Train_Data.csv`
   - `Test_Data_No_Target.csv`

4. Run the notebook cells in order.

## Final Output

The project generates cancellation probability predictions for course registrations.

The final prediction file contains:

- `Client_ID`
- `Drop_Probability`

## Authors

Gili Assour  
Yael Ben Dor

Tel Aviv University  
Introduction to Machine Learning
