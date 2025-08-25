# HR-Analytics-Attrition-Prediction
Retain or Resign: Decoding the 'Why' Behind Employee Turnover with Data

## Overview

This project analyzes employee attrition data to understand the key factors driving employee turnover and builds a predictive model to identify employees at high risk of leaving. The goal is to provide insights that can help organizations develop targeted retention strategies.

## Project Structure

1.  **Data Loading and Exploration:** Load the dataset and perform initial exploration to understand data types, missing values, and basic statistics.
2.  **Data Visualization:** Visualize key features and their relationship with attrition to uncover patterns and insights.
3.  **Feature Engineering:** Create new features based on existing ones to potentially improve model performance.
4.  **Data Preprocessing:** Handle categorical variables (using One-Hot Encoding and potentially Target Encoding) and scale numerical features.
5.  **Handling Imbalanced Dataset:** Address the class imbalance in the target variable (attrition) using techniques like SMOTETomek.
6.  **Modeling:** Train and evaluate multiple classification models (Logistic Regression, Random Forest, Artificial Neural Network) to predict employee attrition.
7.  **Model Evaluation and Tuning:** Assess model performance using relevant metrics (Precision, Recall, F1-score, ROC AUC, PR AUC) and tune hyperparameters and decision thresholds to optimize for specific business goals (e.g., maximizing recall to identify at-risk employees).
8.  **Conclusion:** Summarize the key findings from the analysis and the performance of the final model.

## Key Findings

*   Analysis revealed significant differences between employees who left and those who stayed, including age, daily rate, distance from home, satisfaction levels, stock option level, job role, marital status, job involvement, and job level.
*   Correlations were observed between features like JobLevel, MonthlyIncome, and TotalWorkingYears.
*   Specific groups identified with higher attrition risk include younger employees (28-31), single employees, Sales Representatives, those with low job involvement and job level, employees with long commutes, and those with short tenure with their current manager.

## Modeling Results

Multiple models were trained and evaluated. Logistic Regression, after hyperparameter tuning and threshold adjustment, was selected as the preferred model due to its strong performance in identifying employees at risk of attrition (high recall).

The final tuned Logistic Regression model achieved the following performance on the test set:

*   **Precision (Attrition Class):** 0.3529
*   **Recall (Attrition Class):** 0.7660
*   **F1-score (Attrition Class):** 0.4832
*   **Overall Accuracy:** 0.7381
*   **ROC AUC:** 0.7840
*   **Average Precision (PR-AUC):** 0.6302

The high recall indicates the model's effectiveness in identifying a large proportion of employees who are likely to leave, which is valuable for proactive retention efforts.

## How to Run the Project

1.  Clone this repository: `git clone [repository URL]`
2.  Navigate to the project directory: `cd [project directory]`
3.  Install the required libraries: `pip install -r requirements.txt` (You will need to create a `requirements.txt` file listing all dependencies used, e.g., pandas, numpy, matplotlib, seaborn, sklearn, imbalanced-learn, xgboost, tensorflow, category-encoders, shap, joblib).
4.  Place your dataset (`Human_Resources.csv`) in the correct path as specified in the notebook (`/content/drive/MyDrive/Data Portofolio/Human_Resources.csv`) or update the notebook code to point to your dataset location.
5.  Open and run the Jupyter Notebook (`[your_notebook_name].ipynb`) in a compatible environment (like Google Colab or a local Jupyter installation).

## Dependencies

*   pandas
*   numpy
*   matplotlib
*   seaborn
*   scikit-learn
*   imbalanced-learn
*   xgboost
*   tensorflow
*   category-encoders
*   joblib
