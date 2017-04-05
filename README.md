
[![Build Status](https://travis-ci.com/AppliedMachineLearning/homework-iii-WeiweiVivianWang.svg?token=FY3cqhRLkpqpLqmFhgu9&branch=master)](https://travis-ci.com/AppliedMachineLearning/homework-iii-WeiweiVivianWang)


# GitHub Repository for Homework 3

### COMS 4995: Applied Machine Learning, Spring 2017



##### Group Members:

- [Weiwei Wang](https://github.com/WeiweiVivianWang) (ww2439)
- [Zhengyuan Shi](https://github.com/KennethAY) (zs2319)

##### Files:

- [homework2_rent.py](./homework2_rent.py)
- [preprocessing_rent.py](./preprocessing_rent.py)
- [test_rent.py](./test_rent.py)

*****

#### Model Performance

Best model with largest roc_auc score, 0.81806 is Neural Network classifier.


#### Overview

A banking institution ran a direct marketing campaign based on phone calls. Often, more than one contact to the same client was required, in order to assess if the product (bank term deposit) would be subscribed or not. The task is to predict whether someone will subscribe to the term deposit or not based on the given information.

#### Data Cleaning

	- load data  
	- Split Data into X and y
	- Define Parameters
	- Split Data into Random Training and Test Subsets
	- Recode Missing Values 
	- Feature selection(remove duration varaible)	
	- Get Dummy variables for categorical variables

	 	

#### Model Set1 

	- Logistic Regression CV roc_auc score:0.78362	
	- SVM roc_auc score: 0.71146
	- QDA roc_auc score: 0.74557
	- Nerual Network roc_auc score: 0.81806
	- LDA roc_auc score: 0.78698


#### Model Set2

	- Random Forest roc_auc score:0.74607	
	- XGBoost roc_auc score: 0.7897
	- AdaBoost roc_auc score: 0.76681
	- Extra Trees roc_auc score: 0.76682
	- Gradient Boosting roc_auc score: 0.79391

#### Model Ensemble

#### Resampling Techniques






There are two main files and one folder for data
1) .travis.yml: To configure the Travis and set the environment for test
2) hw3_starter_notebook.ipynb: The file containing the codes

The steps in the code:
1) Data Cleaning
	- load the data
	- Pre-processing (Convert categorical/non-numeric data to numeric data)
	- Feature selection (Select the related features and excluded features which have less impact on the classification)
	- Extract Testing data and Target (The column of "subscribed")
	- Split data into Training and Testing
2) Model Set1: Using 5 models to test, the Feature Engineering and Selection have been done in the above step
	- NearestCentroid
	- KNeighborsClassifier
	- SVC
	- SGDClassifier
	- LogisticRegression
3) Model Set2: Using 3 models to test, the Feature Engineering and Selection have been done in the above step
	- DecisionTreeClassifier
	- RandomForestClassifier
	- GradientBoostingClassifier
4) Model Ensemble: Uising averaging and “poor man’s stacking” method and models created before
5) Resampling
	
