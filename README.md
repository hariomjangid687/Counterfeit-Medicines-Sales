# Counterfeit-Medicines-Sales Prediction

# Problem Statement

Counterfeit medicines are fake medicines which are either contaminated or contain wrong or no active
ingredient. They could have the right active ingredient but at the wrong dose. Counterfeit drugs are illegal and
are harmful to health. 10% of the world's medicine is counterfeit and the problem is even worse in developing
countries. Up to 30% of medicines in developing countries are counterfeit.
Millions of pills, bottles and sachets of counterfeit and illegal medicines are being traded across the world. The
World Health Organization (WHO) is working with International Criminal Police Organization (Interpol) to dislodge
the criminal networks raking in billions of dollars from this cynical trade.
Despite all these efforts, counterfeit medicine selling rackets don’t seem to stop popping here and there. It has
become a challenge to deploy resources to counter these; without spreading them too thin and eventually
rendering them ineffective. Government has decided that they should focus on illegal operations of high net
worth first instead of trying to control all of them. In order to do that they have collected data which will help them
to predict sales figures given an illegal operation's characteristics.

# Solution-

We have two data sets<br/>
1)Counterfeit_train.csv  
2)Counterfeit_test.csv

# Steps
1)First load both train and test data using python pandas library.<br/>
2)Concatenate both train and test data for data preprocessing and data cleaning.    
3)Drop all ID columns from the data because including ID columns in modeling process doesn't make sense.    
4)Make (n-1) dummies of all the categorical columns.    
5)Check Null values and impute Null values by mean in train data only.    
6)Data preprocessing is complete,now split train and test data.  
7)Again split train data into 80% and 20%,in which 80% data will be used for training and 20% data was used for testing,check the performance of the model.    
8)Build linear regression model on train data and make  predictions on 20% test data.    
9)Calculate Mean Absolute Error which is nothing but the difference between y_predicted and y_actual.    
10)Fit linear regression model on whole training data and make predictions on whole test data.    
11)Linear regression is base model,so for getting better performance use another ML models like Random Forest algorithm.    
12)Use RandomForestRegressor(Regression problem) and RandomizedSearchCv of sklearn library with 10 fold cross validation.    
13)Find the best estimator of randomized_search and by this best_estimator  fit on 80% train data and make prediction on 20% test data.    
14)Calculate Mean Absolute Error(Y_predicted-Y_actual).    
15)Fit on whole training data and make prediction on whole test data.  
16)Save our predictions in an csv file.  
17)From both the algorithms,Random Forest give better performance and better predictions.

