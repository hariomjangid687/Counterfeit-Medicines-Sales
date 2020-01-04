# Counterfeit-Medicines-Sales Prediction

# Problem Statement-

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

We have two data files<br/>
1)Counterfeit_train.csv
2)Counterfeit_test.csv

# Steps
A)First I loaded both train and test data using python pandas library.<br/>
B)Then I concatenated both train and test data for data preprocessing and data cleaning.  
C)Then I removed  ID columns from the data because include ID columns in modeling process doesn't make sense.  
D)Then I made (n-1) dummies of all the categorical columns.  
E)Then I check Null values and imputed Null values by mean in train data only.  
F)Then I splitted train and test data after completing data preprocessing. 
G)Then I splitted train data into 80% and 20%,In which 80% data was used for training and 20% data was used for check the performance of the model.  
H)Then I build linear regression model on train data and made the predictions on 20% test data.  
I)Then I calculated Mean Absolute Error which is nothing but the difference between y_predicted and y_actual.  
J)Then I fit linear regression model on whole training data and made the predictions on whole test data.  
K)Linear regression was my base model,so for getting better performance I used Random Forest algorithm.  
L)I used RandomForestRegressor(Regression problem) and RandomizedSearchCv with 10 fold cross validation.  
M)Then I got the best estimator of randomized_search and by this best_estimator I fitted on my train data and made prediction on test data.  
N)Then I calculated Mean Absolute Error.  
O)From both the algorithms,Random Forest gave better performance and better results.

