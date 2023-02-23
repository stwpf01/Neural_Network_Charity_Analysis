# Neural_Network_Charity_Analysis

## Overview

The purpose of this analysis was to find out if applicants will succeed if funded through the use of machine learning and neural networks. This involved compiling, training, and evaluating the neural network model for its accuracy and loss of data. The code for this can be found in the [AlphabetSoupCharity.ipynb]() file. Attempts were then made to optimize this model further through various means, as can be found in the [AlphabetSoupCharity_Optimization]() file. Results will be described below.

## Results

### Data Preprocessing

- The target (`y`) for the model was the `IS_SUCCESSFUL` column.
- The features (`X`) for the model was every other column besides the `IS_SUCCESSFUL` column.
- The identification columns `NAME` and `EIN` were dropped due to them having no bearing on the data. 


### Compiling, Training, and Evaluating the Model

During the optimization it was desired for the model to have an accuracy of at least 75%. Four attempts were made (NOTE: Images display the accuracy of each optimization attempt):


![Optimization1]()

1. Increasing the number of neurons from the original `80`,`30` to `100`,`50`.


![Optimization2]()

2. Adding an extra hidden layer to the model (while still keeping the increased number of neurons but having the added hidden layer have `20` neurons).


![Optimization3]()

3. Changing the activation function for the hidden layers from `relu` to `tanh` (while still keeping the extra hidden layer as well as the increased number of neurons).


![Optimization4]()

4. Lowering the number of neurons to `80`,`30`,`10`, keeping the extra hidden layer, but switching the activation funtions back to `relu`.

Unfortunately, none of the ways tried to optimize the model succeeded in obtaining at least 75% accuracy. Optimization attempt #3 was the closest with 60%. This is actually less than the original attempt, which had a 66% accuracy score. 

## Summary

Overall, this model needs further optimization. One of the possible recommendations would be to bin other columns, such as the `ASK_AMT` column. Perhaps it would improve the model if the `ASK_AMT` values were made similar to the `INCOME_AMT`, in that it would be generalized into ranges rather than specific amounts. Removing the third hidden layer and changing the activation from `relu` to `tanh` may also improve the model; the model fared better without the added layer and `tanh` improved the worse running model. 

