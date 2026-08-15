# Customer Analytics Using Machine Learning

## Overview

This repository contains my Data Science analysis for **Individual Task 1**. The project investigates customer purchasing behaviour using two publicly available datasets relevant to a **Data Scientist – Customer Analytics** role in the retail industry.

The analysis uses machine learning to identify purchasing patterns, predict customer behaviour, and compare model performance.

## Datasets

### 1. Online Shoppers Purchasing Intention

The dataset contains **12,330 online shopping sessions** with **18 attributes** describing browsing behaviour, page activity, visitor characteristics and purchase outcomes.

The target variable is `Revenue`, which indicates whether a shopping session resulted in a purchase.

**Source:**
https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset

### 2. Online Retail II

The dataset contains **1,067,371 transaction records** collected between December 2009 and December 2011 from a UK-based online retailer.

The attributes include invoice number, product code, product description, quantity, transaction date, unit price, customer ID and country.

**Source:**
https://archive.ics.uci.edu/dataset/502/online+retail+ii

## Machine Learning Methods

I applied two classification algorithms:

* **Random Forest**
* **Support Vector Machine (SVM)**

The datasets were analysed separately because they do not contain a common customer or session identifier.

For the Online Shoppers dataset, I predicted whether a browsing session resulted in a purchase.

For the Online Retail II dataset, I created customer-level behavioural features and used them to predict future repeat purchasing behaviour.

## Features Used

### Online Shoppers

The analysis considers behavioural and session-level variables such as:

* PageValues
* ProductRelated
* ProductRelated_Duration
* ExitRates
* Administrative activity
* Informational activity
* VisitorType
* TrafficType

### Online Retail II

Customer-level features were derived from transaction history, including:

* Recency
* Purchase frequency
* Monetary value
* Total items purchased
* Average order value
* Number of unique products
* Number of invoices
* Country

## Model Evaluation

I evaluated the models using:

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC
* PR-AUC

Accuracy was not considered sufficient on its own because the purchasing classes are imbalanced. Precision and recall were used to understand the model's ability to correctly identify purchasers, while F1-score provided a balance between the two. ROC-AUC and PR-AUC were used to compare overall classification performance.

## Results and Visualisations

The analysis produces:

* Model performance comparison tables
* Confusion matrices
* ROC curves
* Precision-recall curves
* Random Forest feature-importance plots

The results help identify which model performs better and which customer behaviours are most useful for predicting purchasing outcomes.

## Key Findings

The **Online Shoppers Purchasing Intention** dataset provides insights into immediate customer behaviour and purchase intention during an online shopping session.

The **Online Retail II** dataset provides insights into longer-term purchasing behaviour and repeat-purchase propensity based on historical transactions.

The two datasets therefore provide **complementary insights** rather than contradictory findings. Together, they demonstrate how current browsing behaviour and historical purchasing behaviour can support customer analytics and predictive decision-making.

## Technologies

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* OpenPyXL

## Repository Structure

```text
customer-analytics-machine-learning/
│
├── README.md
│
├── notebooks/
│   └── Part1_3_Data_Analysis.ipynb
│
└── results/
    ├── online_shoppers_model_results.csv
    ├── online_shoppers_feature_importance.csv
    ├── online_shoppers_confusion_matrices.png
    ├── online_shoppers_ROC_curve.png
    ├── online_shoppers_precision_recall_curve.png
    ├── online_shoppers_feature_importance.png
    └── ...
```

## How to Run

1. Clone or download this repository.
2. Install the required Python libraries.
3. Download the datasets from the UCI Machine Learning Repository using the links provided above.
4. Open the Jupyter Notebook.
5. Update the dataset file paths if required.
6. Run the notebook cells sequentially.
7. The analysis results and visualisations will be generated in the `results` folder.

## Author

**Desai Shubhakar**

Data Science Student
