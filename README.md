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

![bin1](https://github.com/QQrex/Neural_Network_Charity_Analysis/blob/main/Image/bin1.PNG)
![bin2](https://github.com/QQrex/Neural_Network_Charity_Analysis/blob/main/Image/bin2.PNG)

Next, we will use OneHotEncoder from sklearn library to encode our categorical columns.

![encode](https://github.com/QQrex/Neural_Network_Charity_Analysis/blob/main/Image/encode.PNG)

Finally, our last step for data preprocessing is to split our training and testing data and then scale our features.

![sts](https://github.com/QQrex/Neural_Network_Charity_Analysis/blob/main/Image/sts.PNG)

### Compile, train and evaluate

Our data is fairly large with a lot of features. To compile our data efficiently, we will be using two hidden layers. The first layer will utilize 80 neurons and "relu" activation function. The second layer will use 30 neurons and "relu" activation function. 

![model](https://github.com/QQrex/Neural_Network_Charity_Analysis/blob/main/Image/model.PNG)

After compiling our model, we tested our model with our testing data and only saw a 0.73 accuracy score and 0.55 loss in data.

![score](https://github.com/QQrex/Neural_Network_Charity_Analysis/blob/main/Image/score.PNG)

### Scores of Optimization attempts

Attempt 1 - adding more neurons

![a1](https://github.com/QQrex/Neural_Network_Charity_Analysis/blob/main/Image/a1.PNG)

Attempt 2 - adding more hidden layers

![a2](https://github.com/QQrex/Neural_Network_Charity_Analysis/blob/main/Image/a2.PNG) 

Attempt 3 - Binning more features

![a3](https://github.com/QQrex/Neural_Network_Charity_Analysis/blob/main/Image/a3.PNG) 

Attempt 4 - changing activation and adding more epochs

![a4](https://github.com/QQrex/Neural_Network_Charity_Analysis/blob/main/Image/a4.PNG)
 
## Summary

With the data and features given to us in our data, our model had only an accuracy score of 0.73 with a 0.55 loss in data. We attempted to optimize our model by adding more neurons, hidden layers, binning features and/or changing activation function and increasing our epochs saw no significant change in our accuracy score or data loss. Further testing maybe needed to increase optimization for our model or more data may be needed to train our model. Another approach is to use a random forest model, as some of the features in our data maybe creating too much noise for our model. With random forest we wil be able to rank our important features and drop features that aren't really contributing to our model or even causing noise.
