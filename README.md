# Neural_Network_Charity_Analysis
Challenge 19 for Butler Data Science

## Analysis 
The purpose of this challenge is to take deep-learning neural networks and analyze the success of donations to charity. To perform this analysis we preprocessed the data, we compiled, trained and evaluated the model, and finally optimized the model.

## Results

### Data Preprocessing
- The `EIN` and `NAME` columns were used as identification information and were removed from the working dataset.
- The columns `APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT` are the features chosen for the model.
- The column `IS_SUCCESSFUL` contains binary data referring to whether or not the donation was used effectively and this is the target for our model.

### Compiling, Training, and Evaluating the Model
- The model is made up of two hidden layers with 80 and 30 neurons both of these layers were given the activation function "ReLU"
The activation function `Sigmoid` is used on the output layer.
- The model accuracy is under 75%. This is not a satisfying performance to help predict the outcome of the charity donations.

![OGmodelaccuary](https://github.com/coxjack/Neural_Network_Charity_Analysis/blob/main/Additional%20Supporting%20Images/OriginalModel.png)

- To increase the performance of the model, bucketing to the feature `ASK_AMT` was applied and organized the different values by intervals.

![ASKAMT](https://github.com/coxjack/Neural_Network_Charity_Analysis/blob/main/Additional%20Supporting%20Images/AskAMt.png)

- Additionally the number of neurons on both of the hidden layers was increased and another model with three hidden layers was used.

Change in Number of Neurons per layer

![neuronmodelacc](https://github.com/coxjack/Neural_Network_Charity_Analysis/blob/main/Additional%20Supporting%20Images/Neurons.png)

Change in Number of Layers

![layermodelacc](https://github.com/coxjack/Neural_Network_Charity_Analysis/blob/main/Additional%20Supporting%20Images/Layers.png)

- A different activation function (`tanh`) was used also instead of "ReLU" but none of these steps helped improve the model's performance.

![tanhmodelacc](https://github.com/coxjack/Neural_Network_Charity_Analysis/blob/main/Additional%20Supporting%20Images/ActFunc.png)

## Summary
The deep learning model as designed reach the target of 75% accuracy. Even with the alterations done to the neurons, layers, and activation functions the model did not perform any better.
My suggestion would be to try a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against the deep learning model.

