# Neural Network Charity Analysis

## Overview of Project 

1. Compare the differences between the traditional machine learning classification and regression models and the neural network models.
2. Describe the perceptron model and its components.
3. Implement neural network models using TensorFlow.
4. Explain how different neural network structures change algorithm performance.
5. Preprocess and construct datasets for neural network models.
6. Compare the differences between neural network models and deep neural networks.
7. Implement deep neural network models using TensorFlow.
8. Save trained TensorFlow models for later use.

## Purpose

Alphabet Soup, a charitable foundation, is looking to parse out smart places to make investments. Using machine learning and neural networks, the data that was given will be processed, compiled, and trained, and then it will be evaluated and optomized  to help make accurate and informed decisions. The data given is a large file of more than 34,000 organizations that have already received funding from Alphabet Soup. This is the data that will be parsed to see who has previously been successful from the funding, (it should be noted that success is defined by if the money given by Alphabet Soup was used effectively). This will help predict whether current applicants are more likely to be successful or not in the future. 

## Results

### Preprocessing Data for a Neural Network Model

![Deliverable_1_Dropped_Columns](https://user-images.githubusercontent.com/88064181/144948251-2297823a-8daa-414e-918e-efc2202cb197.png)
![Deliverable_1_Features_Targets_StandardScaler](https://user-images.githubusercontent.com/88064181/144948255-c64ac6fc-1af0-4bd7-8f14-4c25901e4712.png)
![Deliverable_1_Layers_Neurons_Activation](https://user-images.githubusercontent.com/88064181/144948261-b856d68a-b3cc-4473-b28d-18f144d2ca34.png)

### Compile, Train, and Evaluate the Model

![Deliverable_2_Non-Optomized_Model_Accuracy](https://user-images.githubusercontent.com/88064181/144948279-4827e25c-a2b2-4e24-9828-0978af960444.png)

### Optimize the Model to Over 75% Accuracy 

![Deliverable_3_Final_Optimized_Accuracy ](https://user-images.githubusercontent.com/88064181/144948303-869de662-6230-43e1-aa36-18c164572a17.png)

The model added a significant margin of accuracy after 4 attempts of optimization, but never achieved 75% accuracy. The model could have been overfitted which would have a negative impact on the overall accuracy. 


## Summary 

### Data Preprocessing 

When preproccessing the data, it is important to consider the targets for the model. For this data set, it is important to see if the target is marked as successful or not in the Dataframe, indicating that the funds from Alphabet Soup have been used effectively. The "IS_SUCCESSFUL" column is the feature of this model. The "EIN" and "NAME" columns are neither targets nor features. They will not increase the accuracy of the model and should therefore be dropped from the dataframe to improve the efficiency of the model. 

### Compiling, Training, and Evaluating the Model

For the original model, 2 layers and an output layer were used. The first layer had 80 neurons and a relu activation, the second layer had 40 neurons and a sigmoid activation, and the output layer had 1 neuron and a linear activation. Relu activation was used for the first layer because it directly outputs inputs of positivity. The sigmoid function was choosen for the deeper layer because it uses exponetial operations. 

In the optimized model, an increase in accuracy was achieved, but the goal of 75% accuracy was not met. The first step to trying to increase accuracy was dropping the "STATUS" and "SPECIAL_CONSIDERATIONS" columns because they did not impact the data being analyzed, and they would increase efficiency. The next attempt saw a lowering in application count when binning. The third attempt saw more hidden layers and neurons added to the model. Instead of 2 layers and an output layer, two layers were added. The first two layers had relu activation and held 120 and 90 neurons respectively. The third and fourth layers had sigmoid activation and held 50 and 30 neurons respectively. The best attempt of the model with the highest accuracy had all of the above changes with the addition of a fifth and final hidden layer. The fifth layer also had sigmoid activation and only ten neurons. It was with this final model that an accuracy of 0.72548 was achieved.

### Recommendation

Overall, the goal of 75% accuracy was not achieved from this model. The model was originally run at an accuracy of 46.68%, so the final model's accuracy of 72.55% was a significant increase, but not the target predictive accuracy set by Alphabet Soup. The model may not have been able to reach total efficiency or the desired accuracy because it may have been overfitted. Removing columns and re-binning the data may help increase the efficiency of the model. Likewise, an increase of data may also help increase the accuracy. The random forest classifiers may have been a better option of model for this data. The random forest classifiers has more estimators and a better depth of data due to all of the branches. It will also help avoid an overfitting of data. 

