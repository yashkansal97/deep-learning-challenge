# DEEP LEARNING CHALLENGE

## OVERVIEW

In this assignment, we focused on building a neural network. This machine learning neural network is trained to predict the best chance of funding for a venture.

## RESULTS

### Preprocessing

1. What variable(s) are the target(s) for your model?
    The target variable is the "IS_SUCCESSFUL" column which stores the information regarding whether the fundraising for the venture was successful or not.
2. What variable(s) are the features for your model?
    All other variables provided, except the name and id columns, are the features for the model.
3. What variable(s) should be removed from the input data because they are neither targets nor features?
    name and id colums needed to be removed from the input.
    
### Compiling, Training, and Evaluating the Model

1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
    For the initial model, we chose 2 hidden layers, both with 'relu' activation function. The first layer had 7 neurons, while the second had 5. There was an output layer with single output and 'sigmoid' activation function because this is a classification problem.
2. Were you able to achieve the target model performance?
    No, the target performance was 75% accuracy, however, with the initial model we only reached 72.53% accuracy on the test set.
3. What steps did you take in your attempts to increase model performance?
    We tried to optimize the model in three ways listed below:
    1. In the preprocessing, we replaced more "application types" and "classifications" with the other category to reduce the number of dummies. We also changed the number of nodes to 9 for the first hidden layer and 4 for the second hidden layer. The accuracy achieved turned out to be lower at 72.22% accuracy.
    2. Keeping the preprocessing from before, we added another hidden layer while also changing the number of neurons in the previous layers. Now hidden layer 1 had 7 nodes, hidden layer 2 had 4 nodes and hidden layer 3 also had 4 nodes. This marginally improved the performance to 72.59% accuracy.
    3. Finally for the last attempt, we looked at the correlation values of features with our target columns. We found that "STATUS" column was very poorly correlated to the target. Upon further analysis, we noted that STATUS had two unique values but the second value ("0") occured only 5 times compared to 34394 for "1". This column was dropped. Keeping the same architecture as the previous optimization attempt, a new model was fitted. This time the accuracy was higher than before but still below target, at 72.79%.
    
## SUMMARY

In summary, the target accuracy value of 75% was not achieved, however our last optimization got close to it at 72.79%. To further improve the accuracy, more EDA is potentially required for the input and target data.

