# MOOCs NLP Data Analytics

An end-to-end Natural Language Processing and machine learning project that analyzes MOOCs (Massive Open Online Courses) forum data to classify student opinions and segment students based on their behavior.

## Overview

This project applies a full NLP pipeline to unstructured forum text — from raw data cleaning all the way through model comparison and clustering. It combines **supervised learning** (opinion classification) and **unsupervised learning** (student segmentation) in a single workflow.

## Pipeline

**1. Data Cleaning & Preprocessing**
- Dropped irrelevant columns (IDs, metadata)
- Handled missing values (median for numeric, most-frequent for categorical)
- Removed duplicates and processed datetime fields

**2. Text Processing (NLP)**
- Lowercasing, removal of links, emails, numbers, and punctuation
- Stopword removal using NLTK
- Term Frequency (TF) and TF-IDF vectorization

**3. Feature Engineering & Reduction**
- Binning continuous features into categories
- Log transformation to reduce skewness
- PCA for dimensionality reduction
- Chi-square (SelectKBest) feature selection

**4. Modeling & Evaluation**
- Compared six classifiers: Naive Bayes, SVM (linear & RBF), Random Forest, AdaBoost, and Logistic Regression
- Handled class imbalance with over-sampling and under-sampling
- Hyperparameter tuning with GridSearchCV
- Evaluated with accuracy, confusion matrix, and classification reports

**5. Clustering**
- K-Means with the Elbow Method to determine the optimal number of clusters
- Cluster visualization on PCA components

## Key Findings

- SVM and Random Forest delivered the strongest classification performance.
- Feature importance analysis surfaced the most influential words in predicting student opinion.
- The Elbow Method identified meaningful student segments within the forum data.

## Tools & Libraries

Python, Pandas, NumPy, Matplotlib, Seaborn, scikit-learn, NLTK, imbalanced-learn

## How to Run

1. Clone the repository:
   ```
   git clone https://github.com/Malakkserag/moocs_NLP_Data_Analytics.git
   ```
2. Install the dependencies:
   ```
   pip install pandas numpy matplotlib seaborn scikit-learn nltk imbalanced-learn openpyxl
   ```
3. Place the dataset (`moocs.xlsx`) in the project folder and run the script.

## Authors
-Malak Serag
-Omar Ahmed

Malak Serag and Omar Ahmed
