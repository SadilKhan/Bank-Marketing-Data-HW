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
- Variance of Recall: ![equation](https://latex.codecogs.com/png.latex?\inline&space;7.59&space;\times&space;10^{-5})

## Decision Tree(Max Depth 12):
*After 10-fold Cross Validation*
- Mean Recall: 93.6%
- Variance of Recall: <img src="http://www.sciweavers.org/tex2img.php?eq=%202.15%20%20%5Ctimes%2010%5E%7B-5%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0" align="center" border="0" alt=" 2.15  \times 10^{-5}" width="101" height="19" />

## SVC
*After 10-fold Cross Validation*
- Mean Recall: 95.7%
- Variance of Recall: <img src="http://www.sciweavers.org/tex2img.php?eq=%204.05%20%20%5Ctimes%2010%5E%7B-5%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0" align="center" border="0" alt=" 4.05  \times 10^{-5}" width="101" height="19" />
