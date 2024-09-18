# deep-learning-challenge
Module 21 Challenge

## Overview 
The purpose of this analysis is to develop and optimize a neural network model that predicts the success of charity applications funded by Alphabet Soup. The dataset contains various features related to the applicants, and the goal is to use these features to create a binary classifier. This classifier will assist Alphabet Soup in making informed decisions about which applicants are most likely to utilize the funding effectively.

### Data Preprocessing
Target Variable: 
This binary outcome indicates whether the funding application was successful (1) or not (0).

```
IS_SUCCESSFUL
```
Feature Variables:
```
APPLICATION_TYPE: Type of application submitted.
AFFILIATION: The sector or affiliation of the applicant.
CLASSIFICATION: Government classification of the organization.
USE_CASE: Intended use of the funding.
ORGANIZATION: Type of organization.
STATUS: Current status of the application.
INCOME_AMT: Income classification of the applicant.
SPECIAL_CONSIDERATIONS: Any special considerations noted for the application.
```
Additionally, we have the EIN and NAME variables, which were dropped as they are identifiers and do not provide predictive value for the success of funding. To simplify the model, rare categories in APPLICATION_TYPE and CLASSIFICATION were combined into an "Other" category. We also applied one-hot encoding to convert categorical variables into a format suitable for machine learning.

### Compiling, Training, and Evaluating the Model
Before compiling, training, and evaluating our model, the first step was to split the data into training and testing sets. This was followed by scaling the features to ensure all variables contribute equally to the model's performance, especially since we had categorical columns.

The data was then prepared for the neural network. We initially set the input layer to match the number of features in our dataset, used two hidden layers with 80 and 40 neurons respectively, and applied the ReLU activation function for both. The output layer consisted of one neuron with a sigmoid activation function to predict the probability of success, which is our objective.

Diving deeper into the structure of this model, I used binary cross-entropy as the loss function, the Adam optimizer, and accuracy as the evaluation metric, as suggested in the starter code.

Initially, our model achieved an accuracy of 72.63%. After a series of optimization attempts, I was unable to reach the 75% threshold, but the accuracy slightly improved to 72.73% by adding five hidden layers with 150, 80, 50, 50, and 10 neurons respectively, while keeping the same ReLU activation function and reducing the number of epochs to 20.

##### Other attempts included:

- Adding the tanh activation method.
- Decreasing epochs to various options like 90, 52, etc.
- Simplifying the model further by filtering with higher thresholds in different categories.
  
### Summary
Our final model achieved a solid accuracy of 72.73%, indicating that it correctly predicted the success of applicants approximately 72.73% of the time. While we made some improvements, there remains significant room for enhancement. To surpass this accuracy threshold, several strategies could be explored. One approach is to delve deeper into feature engineering, make adjustments to the network's architecture, and continue experimenting with the number of neurons in the hidden layers. Also, incorporating advanced techniques such as regularization, hyperparameter tuning, and exploring alternative algorithms could further refine the model's performance and lead to more accurate predictions.

### Help
- Xpert Learning Assistant
- Tutoring 
