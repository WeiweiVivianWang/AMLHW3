# homework-iii-starter
the starter repository for hw3

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

Test Set R<sup>2</sup>: 0.538


#### Overview

A banking institution ran a direct marketing campaign based on phone calls. Often, more than one contact to the same client was required, in order to assess if the product (bank term deposit) would be subscribed or not. The task is to predict whether someone will subscribe to the term deposit or not based on the given information.

#### Data Cleaning

	- load the data
	- Split Data into X and y
	- Define Parameters
	- Split Data into Random Training and Test Subsets
	- Recode Missing Values 
	- Feature selection(remove duration varaible)	
	- Get Dummy variables for categorical variables

	 	
	
The data was filtered to remove all observations where the response variable (`UF17`) is missing. Then, the data was randomly split into a training and test subset. Missing values in the data were then recoded as `NaN`s. Next, all features that were specific to the tenant—or were leaking information about the response variable—were removed. This reduced the number of features from 196 to 73. Missing values were then imputed based on the median for continuous values and the mode for categorical values. Finally, the categorical features were encoded as one-hot.

#### Model Set1 

The model of choice for this assignment is the Ridge Regression because the inclusion of a penalty term `alpha` is able to reduce overfitting. Grid search was performed to determine the ideal value for `alpha`, which turns out to be `0.01` in this implementation. The model was also cross-validated using 10 iterations of shuffle-split cross-validation on the training set. Shuffle-split was chosen because it randomly shuffles the data before splitting it into the training and validation subsets. This led to an accuracy of 53.8% on the test set. The script `test_rent.py` ensures that the model is at least 50% accurate.


#### Model Set2

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
	
