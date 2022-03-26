# financial analysis - Machine Learning - Classification

Logistic Regression - Credit Risk Problem - Imbalanced Sample


In this assigmnment, financial Python programming skills will be used with logistic regression analysis to tackle a credit classification problem. Credit risk poses a classification problem that’s inherently imbalanced. This is because healthy loans easily outnumber risky loans. In this assignment, used various techniques to train and evaluate models with imbalanced classes. For this purpose I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

Data source: CSV file

The steps followed are:

1. Split the Data into Training and Testing Sets

2. Create a Logistic Regression Model with the Original Data

3. Predict a Logistic Regression Model with Resampled Training Data

4. Write a Credit Risk Analysis Report

Packages Used This project leverages python 3.7

Installation Guide: The application requires the below programs to be installed 

1. Python 
2. Pandas 
3. Numpy
4. SKlearn
5. Imblear
6. Pathlib 


**Credit Risk Analysis Report

The purpose of this analysis is to determine if logistic regression for loan classification performs better imbalanced data or with balanced data, alebit generated automatically using resampler tool provided by imblearn.

For the purpiose of this analysis, I will leverage a set of past loan data obtained in a csv file to predict if the loan ultimately turns out to be good / bad using logistic regression. However, the data source contains data that is imbalanced where in the number of bad loans in the data is just around 3.2% of the total loan population as revealed by the value counts  obtained from the data. I performed the following analysis to reach my objective:

1. Performed LogisticRegression with the data as contained in the csv file (original data) and calculated the effectiveness of the predicted classification as measured by precision, accuracy and recall ratios.
2. Resampled the data inorder to balance the data in terms of the population of bad and good loans (50% each), and repeated the prediction of bad and good laons using LogisticRegression on the resampled data. The revised result, as measured by precision, accuracy and recall ratios is compared with the original results.

## Results

The results of the analysis are provided below:
* **Machine Learning Model 1 based on original data:**
<img width="915" alt="Screen Shot 2022-03-26 at 4 12 16 PM" src="https://user-images.githubusercontent.com/96159292/160260091-72c4c657-b3c7-4ddc-b100-8efec235bb71.png">


    * Accuracy score ((True Positive + True Negative)/ Total Population)) - 99.2% 
    * Precision Score - Overall 0.99 (For good loans is 100% but for bad loans is 90%)
    * Recal1 Score -  Overall - 0.99 (For good loans is 100% but for bad loans is 86%)

* **Machine Learning Model 2 based on resampled data:**
<img width="908" alt="Screen Shot 2022-03-26 at 4 12 29 PM" src="https://user-images.githubusercontent.com/96159292/160260094-87f4bb84-3437-4486-9727-00613d580ce8.png">

    * Accuracy score ((True Positive + True Negative)/ Total Population)) - 99.2% 
    * Precision Score -  Overall - 1 (Breakup - For good loans is 99% but for bad loans is 99%)
    * Recal1 Score -  Overall - .99 (Breakup - For good loans is 100% but for bad loans is 86%)

## Summary

In the case of credit classification, precision ratio which  measures true positive as a measure of total positive (in other words, the number of good loans predicted as a percetnage of total good loans preicted - i.e. fasle positive are minimized) is the best indicator, as one nnegative loan can erode the entire porfitability of interest earned on good loans. 

The precision ratio for bad loans improved considerably with the resampled data and hence the model with the revised sample data is preferred to run LogistcRegression in this case.


Contributors Brought to you by Ram Atmakuri (ram.atmakuri@outlook.com)

License [MIT] (https://choosealicense.com/licenses/mit/)

