# deep_learning
Module 21 challenge



**Overview of the analysis:** The purpose of this analysis was to create a nueral network that can help select which applicant's fundings which have the best chance of success. Using binary classifiers, this project looks thruogh 34000 records and is optimized to predict whether or not the funding will be successfull. 

Results: 

Data Preprocessing

What variable(s) are the target(s) for your model?

The targets of the model are the is_successful binary variable, indidcating whether or not the funding was successful for past applicants. 
**What variable(s) are the features for your model?:**

The features of the model is the is_successful variable which is a binary variable whether or the funding would be successful. 

The following variables were used in the model (excluding is successful):
<img width="798" alt="image" src="https://github.com/Samp-nik/deep_learning/assets/128440885/793b1a12-1755-42e7-baf3-7fbe95e53ab7">


What variable(s) should be removed from the input data because they are neither targets nor features?

- The variables that should be removed from the model are EIN and Name, since these are categorical variables that identify the individual assets, but do not provide useful information relating to their performance.

**Compiling, Training, and Evaluating the Model**

How many neurons, layers, and activation functions did you select for your neural network model, and why?

In the neural network model, three layers were used. The first hidden layer has 80 neurons with a ReLU activation function, the second hidden layer has 30 neurons with a ReLU activation function, and the output layer has 1 neuron with a sigmoid activation function. The choice of 80 neurons in the first layer and 30 neurons in the second layer is somewhat arbitrary and may be based on experimentation. The ReLU activation function is commonly used for hidden layers in neural networks, while the sigmoid activation function is appropriate for binary classification tasks like the one at hand.


**Were you able to achieve the target model performance?**

The model performance is indicated by the accuracy metric during training. After 100 epochs, the model achieved an accuracy of approximately 74.44% on the training data

**What steps did you take in your attempts to increase model performance?**

The steps taken to enhance model performance:

Standardizing the input data using StandardScaler.
Binning and replacing values in the 'APPLICATION_TYPE' and 'CLASSIFICATION' columns to reduce the number of unique values.
Training the model with 100 epochs.

**Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.**

Overall, the model did a satisfactory job of predicting the whether or not an applicant would be successful with an accuracy of 74%. Ways to improve the classification problem would be continuing to adjust the number of layers and nuerons or running another method like a Random Forest. 
