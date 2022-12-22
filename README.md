# Neural_Network_Charity_Analysis
## Overview 
In this analysis, we used a neural network and deep learning model to predict best Organizations for funding from Alphabet Soup. As, some Organizations are not good they took the money and disappear so, we want to create a model that can easily predict that which Organizations are worth the funding, and which are high risk from a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.
## Results 
 ### Data Preprocessing
- We have one target variable which contains binary values is: IS_SUCCESSFUL.
- There are many feature variables that we used for our model: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT.
- We consider the ‘EIN’, ‘Name’ as neither target nor features because this information is not important for a model.
### Compiling, Training, and Evaluating the Model
-	This model contains 80 and 30 neurons respectively for two hidden layers, because data has 9 features and 34,000 samples that made it a large dataset. To speed up the training process, we are using the activation function ReLU as it gives value from 0 to infinity. For output layer we used the Sigmoid function because output column is a binary classification.
-	The original model’s performance fell short of the 75% target. The accuracy recorded was 72.5% with a loss of 55.9%. AS shown in picture.

![Screenshot_20221222_014232](https://user-images.githubusercontent.com/111101038/209231458-ee560e58-e7a2-4110-8744-2b46d4d8b551.png)


### Additional steps for model:
-	Attempt #1: An additional column is removed from the data set, "SPECIAL_CONSIDERATIONS" and more neurons are added to the hidden layers.
-	Attempt #2: Third hidden layer is added to increase the performance. 
-	Attempt #3: The activation function is changed from "relu" to "tanh"
## Summary 
The overall results, for this model is not satisfactory even after adding more layers, neurons and changing activation functions. After all the changes, we couldn’t reach the target accuracy 75%.  So, as we have a binary classification in our prediction column, I would suggest that we can use the machine learning model such as Random 
Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.
