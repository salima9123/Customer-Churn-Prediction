# Customer Churn Prediction Using K-Nearest Neighbors (KNN)

## Project Overview

This project uses Machine Learning to predict whether a customer is likely to leave a service. The K-Nearest Neighbors (KNN) algorithm is used to classify customers based on the information available in the dataset.

The project includes data cleaning, exploratory data analysis, model training, performance evaluation, and predictions for new customer data.

## Problem Statement

Customer churn occurs when customers stop using a company's products or services. Losing customers can affect business growth and revenue.

This project aims to predict customer churn using Machine Learning so that businesses can better understand customer behaviour and identify customers who may need additional attention.

## Objectives

- Clean and prepare customer data for analysis.
- Understand customer data through visualisations.
- Build a customer churn prediction model using KNN.
- Select a suitable K value for the model.
- Evaluate the model using classification metrics.
- Save and reload the trained model for future predictions.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Pickle
- Google Colab

## Machine Learning Algorithm

**K-Nearest Neighbors (KNN)**

KNN is a supervised Machine Learning algorithm used for classification. It predicts the class of a new data point by examining the classes of its nearest neighbours.

In this project, KNN is used to classify customers into churn and non-churn categories based on the dataset's target labels.

## Project Workflow

1. Loaded and inspected the customer dataset.
2. Checked for missing values, duplicate records, and data inconsistencies.
3. Cleaned and prepared the data.
4. Performed Exploratory Data Analysis (EDA).
5. Created histograms, boxplots, and pairplots using Matplotlib and Seaborn.
6. Prepared the input features and target labels.
7. Converted categorical features into numerical values where required.
8. Split the dataset into training and testing sets.
9. Evaluated different K values to select the best-performing value.
10. Selected K = 15 for the final model.
11. Evaluated the model using accuracy, precision, recall, F1-score, and a confusion matrix.
12. Saved the trained model for future use.
13. Reloaded the saved model to make predictions on new customer data.

## Key Features

- Customer data cleaning and preprocessing.
- Exploratory Data Analysis using visualisations.
- KNN-based customer churn classification.
- Selection of the best K value through model evaluation.
- Performance analysis using classification metrics.
- Saved model for reuse without retraining.
- Prediction for new customer input.

## Model Evaluation

The model was evaluated on 1,405 test samples. The best K value selected during model tuning was 15.

### Performance Metrics

| Evaluation Metric | Score |
|---|---:|
| Best K Value | 15 |
| Accuracy | 78% |
| Weighted Precision | 77% |
| Weighted Recall | 78% |
| Weighted F1-score | 78% |
| Class 1 Precision | 61% |
| Class 1 Recall | 52% |
| Class 1 F1-score | 56% |

### Classification Report

| Class | Precision | Recall | F1-score | Support |
|---|---:|---:|---:|---:|
| 0 | 84% | 88% | 86% | 1,033 |
| 1 | 61% | 52% | 56% | 372 |

### Confusion Matrix

| | Predicted Class 0 | Predicted Class 1 |
|---|---:|---:|
| Actual Class 0 | 908 | 125 |
| Actual Class 1 | 179 | 193 |

### Results and Analysis

The KNN model achieved 78% accuracy on the test dataset with K = 15.

The model correctly classified 908 samples from Class 0 and 193 samples from Class 1. However, the recall for Class 1 was 52%, indicating that the model missed some actual cases belonging to that class.

The results show that the model identifies Class 0 more effectively than Class 1. Further tuning and experimentation could help improve its performance on the weaker class.

*Note: Confirm that Class 1 represents customers who churned before interpreting these metrics as churn-specific results.*

## Saved Model

The trained KNN model was saved using Pickle for future use.

Saving the model makes it possible to load the trained model and make predictions without training it again.

The preprocessing steps used during training, including encoding and scaling where applicable, must also be applied consistently to new customer data.

## Sample Prediction

**Input:** Customer information matching the features expected by the trained model.

**Output:** Predicted customer class.

The output indicates whether the customer belongs to the churn or non-churn category according to the target labels in the dataset.

*Note: Actual predictions depend on the input values and the trained model.*

## Dataset

Add the Kaggle dataset link used in this project:

[Customer Churn Prediction Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn?utm_source=chatgpt.com)

## How to Run the Project

1. Open the project notebook in Google Colab.
2. Upload the required customer dataset.
3. Run the notebook cells in order.
4. Review the data analysis and model evaluation results.
5. Enter new customer details to generate a prediction.
6. Load the saved model to make further predictions without retraining, if the notebook supports this workflow.

## Future Improvements

- Improve recall for the churn class.
- Experiment with different K values and model parameters.
- Compare KNN with other classification algorithms.
- Explore the relationship between customer features and churn.
- Develop a simple user interface for customer churn predictions.

## Disclaimer

This project is developed for educational purposes and demonstrates the application of Machine Learning to customer churn prediction. Its predictions should be evaluated alongside other business information before making customer retention decisions.

## Author

Machine Learning project developed using Python and Scikit-learn.
