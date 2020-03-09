# Project 2 - Ames Housing Data and Kaggle Challenge

*Author: Julie Vovchenko*

## Problem Statement
By using Ames Housing Train Dataset, I want to create the best model that identifies best predictions of sale price of all houses in Test Dataset, including my friends (Mary and Ira) house, and send those predictions to Kaggle competition.  
In addition I want to identify best features that effect the home sale price the most of all houses in Ames Iowa, that can be used for potential remodeling by Mary and Ira.  


### Table of Content:
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
    -  [Import Packages and Data](#Import-Packages-and-Data)  
    -  [Renaming Columns (train/test)](#Renaming-Columns-(train/test)) 
    -  [Data Cleaning](#Data-Cleaning)
        -  [Imputing Missing Data (train)](#Imputing-Missing-data-(train))
        -  [Imputing Missing Data (test)](#Imputing-Missing-data-(test))    
        - [High Level Checks](#High-Level-Checks)
- [Feature Engineering](#Feature-Engineering)  
    - [Interactions (Synergies) Creation](#Interactions-(Synergies)-Creation)
    - [Dummie Variable Creation](#Dummie-Variable-Creation)
- [Preprocessing](#Preprocessing)
- [Modeling](#Modeling)
    - [Linear Regression](#Linear-Regression)
    - [Ridge Regression](#Linear-Regression)
    - [Lasso Regression](#Lasso-Regression)
    - [Friends House Sale Price Prediction](#Friends-House-Sale-Price-Prediction)
    - [Kaggle Competition Test Predictions](#Kaggle-Competition-Test-Predictions)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)  



### Datasets and Dictionary

- [Ames Housing Data (train dataset)](../data/train.csv)
- [Ames Housing Data (test dataset)](../data/test.csv)
- [Data Dictionary](../data/data_dictionary.txt)


## Executive Summary

In order to solve the problem, I used the Ames Housing Train and Test Datasets, that holds the data of all houses sold on Ames Iowa in 2006-2010. The train dataset consists of 2051 of rows and 81 columns, and test dataset consists of 878 rows and 80 columns. They both have the same format, for the exception of 'sale_price' column missing in test dataframe.  
1. Using the data dictionary, I imputed missing values of those columns for houses that dont have certain features, like a basement, garage or a pool, in both dataframes(train and test. 
2. Cleaned both datasets for instances of other missing vallues, by performing high level checks.
3. Checked linearity for those house features with numeric variables and with highest correlation to house sale price.
4. Performed Feature Engeniering by creating Interations(synergies) with numeric features that have heighest correlation to house sale price, and also created dummie columns for 'object' features. 
5. Created three models: Linear Regression Model, Ridge and Lasso Models. 
6. Sent predicted price to Kaggle competition.
7. Predicted the sale price of Mary and Ira house, including my remodeling recommendation by using highest ceefitients from Linear Regression Model.



---

## Conclusions and Recommendations  
By using Ames Housing Train Dataset, I created three models (Linear Regression, Ridge and Lasso) that identifies predictions of sale price of all houses in Test Dataset.  All three models performed similarly well in predicting housing sale price based on all house features in Ames Train Dataset. I used Linear Regression model in predicting house sale price in Test dataframe, in which Mary and Ira houses details as well. This predictions were submitted to Kaggle Competition, scorring 42nd among 121 total.


**The metrics of the Lenear Regression Model used for predictions are:**
1. R^2 train = 0.94
2. R^2 test = 0.91
3. RMSE train = 19,508
4. RMSE test = 22,728  

**Conclusion on a model performance:**  
The model is low bias. The metrics on train dataset is a bit higher than on a test dataframe, meaning that the model is a little bit overfit. 

Based on Lenear Regression model the predicted price of the house of Mary and Ira is 170,224 dollars. 

The following recommendations were given to Mary and Ira:

    "Consider upgrading the following features with highest effect on sale price:
      - Exterior: Asphalt Shingles / Cinder Block / Brick Common
      - Roof Material:  Membrane 
      - Heating: Hot water or steam heat"

  


---
### Source Documentation  
The following sourse was used to implement a house image into a presentation (page 2).  
http://www.iconarchive.com/show/noto-emoji-travel-places-icons-by-google/42486-house-icon.html
