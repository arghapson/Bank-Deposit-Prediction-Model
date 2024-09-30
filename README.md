# Predictive Modelling for Bank Deposit Subscriptions - Data Analysis

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning/Preparation](#data-cleaning-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Predictive Modelling](#predictive-modelling)
- [Results/Findings](#results-findings)

### Project Overview
---
This project focuses on building and evaluating a predictive machine learning model to solve a classification problem using a bank deposit dataset. The main objective is to predict whether a customer will subscribe to a term deposit based on various features such as demographic and financial data. The analysis aims to uncover key insights and trends that can guide marketing campaigns, with a specific focus on customer characteristics that influence subscription rates.

### Data Sources
---
- **Dataset**: Bank Term Deposit Dataset  
  The dataset used for this project was obtained from Kaggle, a repository of open datasets. It includes customer demographic information, financial data, and details about marketing interactions.
  - **Key Features**:
    - **age**: Age of the customer (numerical)
    - **job**: Type of job (categorical)
    - **balance**: Average yearly balance in euros (numerical)
    - **education**: Level of education (categorical)
    - **y**: Target variable representing whether the client subscribed (binary: 'yes' or 'no')

### Tools
---
- **Python** — Used for data manipulation, visualisation, and modelling.
- **Pandas** — Data loading and preparation.
- **Matplotlib & Seaborn** — For data visualisation.
- **Scikit-learn** — Used for building and evaluating the logistic regression model.
- **Jupyter Notebook** — For developing and documenting the analysis and modelling process.

### Data Cleaning/Preparation
---
1. **Handling Missing Values**: There were no missing values in the dataset.
2. **Categorical and Numerical Handling**: Categorical variables were one-hot encoded, and numerical variables were scaled using `StandardScaler`.
3. **Splitting the Dataset**: The data was split into training and testing sets (80/20) to prevent data leakage and evaluate the model on unseen data.

### Exploratory Data Analysis
---
The exploratory data analysis (EDA) helped identify key trends and relationships within the dataset:
- **Age Group Analysis**: Younger (<30) and older (>60) customers exhibited higher subscription rates.
- **Financial Attributes**: Customers with higher balances and without loans showed a greater tendency to subscribe.
- **Communication Channels**: The method of communication and timing (e.g., month of contact) played a significant role in determining the likelihood of subscription.

Key Questions Explored:
- Which age groups are more likely to subscribe?
- Does having a personal loan affect subscription rates?
- How does the number of contacts impact the outcome of a campaign?

### Predictive Modelling
---
The project employed **Logistic Regression** for the predictive task of classifying whether a customer would subscribe to a term deposit. This model was chosen for its simplicity and effectiveness in binary classification tasks. Key steps in the modelling process:
1. **Preprocessing**: Scaling of numerical features and one-hot encoding for categorical variables.
2. **Training**: The model was trained on 80% of the dataset.
3. **Evaluation**: Key metrics such as accuracy, precision, recall, F1-score, and the area under the ROC curve were used to evaluate model performance.

### Results/Findings
---
- **Accuracy**: 89.88% on the test set, indicating a reasonably good performance.
- **ROC AUC**: 0.92, reflecting strong model performance in distinguishing between subscribers and non-subscribers.
- **Class Imbalance**: The model showed better performance in predicting non-subscribers, a common issue with imbalanced datasets.
