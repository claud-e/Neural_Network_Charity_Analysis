# Neural_Network_Charity_Analysis

## Overview

This analysis is meant to create a deep learning model to predict which organizations are effective when given donations.  

## Results


- Data Preprocessing
  - What variable(s) are considered the target(s) for your model?
The target variable is found as "IS_SUCCESSFUL", since it is what we are trying to predict.

  - What variable(s) are considered to be the features for your model?
Almost every other variable is a feature, except for the ones specified in the next question.


  - What variable(s) are neither targets nor features, and should be removed from the input data?
"EIN" and "NAME" are only identifying variables which do not add value to the model. Also, after the preprocessing stage, "SPECIAL_CONSIDERATIONS" is split into two columns, but since it is a binary variable one of the two columns can be dropped because the information is redundant.

- Compiling, Training, and Evaluating the Model
  - How many neurons, layers, and activation functions did you select for your neural network model, and why?

3 hidden layers are used, 80 neurons used in the first layers, 30 in the second layer and 1 in the final (output) layer. The activation functions are Rectified Linear Unit (ReLU) for the first two layers, Sigmoid for the final layer. Using ReLU as the activation function has become standard in the world of neural networks because in comparison to other functions it allows for more sensitivity to the activation sum and is more robust while keeping the computational requirements at a low point. The sigmoid function in the final layer is cited as a "best practice" when dealing with non-linearly separable datasets.
  
  - Were you able to achieve the target model performance?

No, altough the accuracy came very close at 0.7268 when adding 20 (for a total of 100) neurons to the model.
  
  - What steps did you take to try and increase model performance?

The first attempt was to change the first activation function to a sigmoid function.
The second one added one hidden layer with 10 neurons and ReLU as the activation function.
The third attempt added the aforementioned 20 neurons to the first layer.

## Summary

This model came very close to the desired accuracy, therefore I recommend spending a bit more time processing the data to get a better and less noisy dataset. Another option is to experiment with the content of the layers, mainly adding more neurons to already existing layers, but changing activation functions would be worthwile as well.
