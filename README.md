# Group Members: 
- Md.Sadil Khan(MDS201927)

- Prince Kumar(MDS2019)

# Data: [Bank Marketing Data](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing) 

# Problem Description:
 The "Bank Marketing Data Set" from the UCI Machine Learning Repository is related with direct marketing campaigns (phone calls) of a Portuguese banking institution.

The classification goal is to predict if the client will subscribe a term deposit (variable y). In this assignment we have to build three classifiers for this data set: a decision tree, a naive Bayesian classifier, and a support vector machine and we have to do 10-fold cross validation to evaluate our classifier.

# Soultion:

## Dataset Description:
- The dataset has no missing values.

- The class distribution is skewed heavilly.

## Data Preprocessing:
- We deleted "contact" and "day of week" column, since this are not useful for classification.

- There are many similar values in "education","loan","default","job" and "housing" columns, so we replaced similar categories with same name.

- The column "pdays" has all values under 27 except one value,999 ,which is significantly greater than rest of the value. So we replaced it with 0.

- We used One Hot Encoder for categorical variables and then scaled the dataset along the columns.

- Since the class distribution is skewed, we used [SMOTE](https://machinelearningmastery.com/smote-oversampling-for-imbalanced-classification/) for over-sampling.

# Models

## Naive Bayes:
*After 10-fold Cross Validation*
- Mean Recall: 89.3%
- Variance of Recall: $7.59 \mul 10^{-5}$
