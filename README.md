# Neural_Network_Charity_Analysis

## Purpose

We have been tasked to build a neural network model to predict whether applicants funded by Alphabet Soup will be successful.

## Overview

With the dataset provided to us we will:

- Preprocess our data

- Compile, train and evaluate our model

- Optimize the model

## Results

### Data Preprocessing

Looking at our data, we can remove the columns 'EIN' and 'NAME' as these two columns are identifiers and would not be needed for our deep learning model. Next, we have identified 'IS_SUCCESSFUL' as our target value and all other columns will considered as features for our model.

For our features, we would need to we will bin our 'APPLICATION_TYPE' and 'CLASSIFICATION' column as they have imbalanced unique value based on our density graphs.

![bin1]()
![bin2]()

Next, we will use OneHotEncoder from sklearn library to encode our categorical columns.

![encode]()

Finally, our last step for data preprocessing is to split our training and testing data and then scale our features.

![sts]()

### Compile, train and evaluate

Our data is fairly large with a lot of features. To compile our data efficiently, we will be using two hidden layers. The first layer will utilize 80 neurons and "relu" activation function. The second layer will use 30 neurons and "relu" activation function. 

![model]()

After compiling our model, we tested our model with our testing data and only saw a 0.73 accuracy score and 0.55 loss in data.

![score]()

### Scores of Optimization attempts

Attempt 1 - adding more neurons

![a1]()

Attempt 2 - adding more hidden layers

![a2]() 

Attempt 3 - Binning more features

![a3]() 

Attempt 4 - changing activation and adding more epochs

![a4]()
 
## Summary

With the data and features given to us in our data, our model had only an accuracy score of 0.73 with a 0.55 loss in data. We attempted to optimize our model by adding more neurons, hidden layers, binning features and/or changing activation function and increasing our epochs saw no significant change in our accuracy score or data loss. Further testing maybe needed to increase optimization for our model or more data may be needed to train our model. Another approach maybe to use a random forest model, as some of the features in our data maybe creating too much noise for our model.
