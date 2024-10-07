# Customer Churn Prediction

This project predicts customer churn using a dataset from a bank. It involves data preprocessing, feature engineering, visualization, and training a machine learning model (XGBoost) to predict whether a customer will exit the bank or not.

## Dataset

The dataset used in this project is the **Churn Modelling Dataset** which contains the following key columns:
- CustomerId
- Gender
- Age
- Balance
- EstimatedSalary
- Exited (Target column)

## Project Structure

1. **Data Preprocessing**: 
   - Handling missing values and checking for duplicates.
   - Label encoding for categorical variables.
   - Feature scaling for numerical variables.

2. **Feature Engineering**:
   - Grouped customers by age into categories such as 'Young', 'Middle-Aged', and 'Senior'.
   - Segmented balance into low, medium, and high categories.
   - Created customer activity score based on the number of products, credit card ownership, and activity status.
   - Added a ratio feature comparing balance to estimated salary.

3. **Data Visualization**:
   - Distribution plots for `Balance` and `Age`.
   - Bar plot for gender distribution.

4. **Model Training**:
   - The model used is **XGBoost** (Extreme Gradient Boosting) Classifier.
   - Trained with the processed dataset.
   - Model evaluation using metrics like accuracy, precision, recall, and F1 score.

5. **Evaluation Metrics**:
   - Confusion Matrix
   - Precision-Recall Curve
   - AUC-ROC Curve

## Installation

### Prerequisites:
- Python 3.10.12

## Dependencies

Refer to `requirements.txt` for a complete list of required libraries.

## Results

The project evaluates the model using:
- Confusion Matrix
- Precision, Recall, F1-Score
- ROC-AUC Score

Graphs for Precision-Recall and ROC Curves are plotted to analyze the performance.

## Usage

1. Preprocess the dataset.
2. Train the model using XGBoost.
3. Visualize the evaluation metrics.
