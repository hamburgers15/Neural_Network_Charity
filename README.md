# Neural_Network_Charity

## Overview
The purpose of this analysis is to use neural networks to help predict where to make investments by analyzing a data set containing information on companies that were invested in perviiously.  

## Results
### Data Preprocessing
-The target variable is IS_SUCCESSFUL
-The variables that are features in this model are; APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS
-EIN and NAME are neither target nor feature variables and so they were removed.
### Compiling, Training, and Evaluating the Model
-The original model contained two hidden layers, with 80 neurons in the first layer and 30 in the second layer.  A relu activation was selected for both.  
-The original model did not reach the 75% accuracy goal.  The accuracy score was 73.25%.

![original](https://user-images.githubusercontent.com/117960721/235949862-4b384e63-f8ef-4002-8b74-2b6b1a6a05c8.png)

-In order to try and get a better accuracy outcome I preformed 3 optimizations.
  - First I added a third hidden layer with 20 neurons and a relu activation.  In this case the accuracy decreased to 72.88%

![Attempt 1](https://user-images.githubusercontent.com/117960721/235951470-9377a21d-c975-4ac4-964a-65b124b29e95.png)

  - Then I increased the number of neurons in each layer.  THey changed from 80, 30 and 20 to 100, 85 and 50. Unfortunetly the acuraccy fell even more, to 72.85%
  
![Attempt 2](https://user-images.githubusercontent.com/117960721/235951590-b5157fc6-9516-49bb-85a9-0d2206928a7a.png)

  - The final optimization I prefomed was to change the activation functions for all three hidden nodes, from relu to sigmoid.  This change did give us an increase in the accuracy score to 73.03%

![Attempt 3](https://user-images.githubusercontent.com/117960721/235951750-41c8faf7-fb33-4a6b-a727-e22bc0d010d2.png)


## Summary
Ultimately, my attempts at optimization did not increase the accuracy of the original model.  In the future using the Balanced Random Forest Classifier model may provide us with a more accurate model for this dataset.  The Random Forest model uses multiple dicision trees to train the model witch can lead to a better model with less chance for overfitting.
