# deep-learning-challenge
Module 21 Challenge, Data visualization Bootcamp U of T.
Student Name: Jesus Hernandez

# AlphabetSoupCharity Deep Learning Model Analysis

## Overview of the Analysis:

The purpose of this analysis is to develop a deep learning model using TensorFlow and Keras to predict the success of charitable organizations based on various input features. The dataset used for training and testing contains information about different charitable organizations, and the goal is to create a model that can effectively classify whether a charity will be successful or not.

## Data Preprocessing:
* Target and Features:
    Target Variable(s): 'IS_SUCCESSFUL'
    Feature Variable(s): All columns except 'IS_SUCCESSFUL' after dropping non-beneficial columns ('EIN', 'NAME').
    Removed Variables: 'EIN', 'NAME' were removed as they are neither targets nor features.

## Compiling, Training, and Evaluating the Model:
 * Neurons, Layers, and Activation Functions: In this step the first model   had the next characteristics: 
    * First Hidden Layer: 8 neurons, activation function = [relu]
    * Additional Hidden Layer 1: 5 neurons, activation function = [relu]
    * Output Layer: Activation function = 'sigmoid' (for binary classification)
    * Achieving Target Model Performance: The assessment of the model yielded 
    Loss: 0.5499852299690247, Accuracy: 0.7392128109931946. This model may be improved. 
    * Steps to Increase Model Performance: To enhance the model I ran an auto-tune "AlphabetSoupCharity_Tune.ipynb" with an output of Best val_accuracy So Far: 0.7395043969154358 in a total elapsed time: 00h 31m 23s. The values for the neural an optimized neural network yielded are: 
    'activation': 'relu',
    'first_units': 9,
    'num_layers': 5,
    'units_0': 3,
    'units_1': 5,
    'units_2': 3,
    'units_3': 5,
    'units_4': 9,
    'units_5': 5,
    
    I tested this paremeters in "AlphabetSoupCharity_Optimization.ipynb", also changing the bin size. However the accuracy did not improve. 

    After tutor feedback I tested different number of layers including 30 neurons for the first layer as approximately the half of the number of input features you have. It ran with for layers during 100 epochs. The results yielded Loss: 0.5506576299667358, Accuracy: 0.7384839653968811.

    Then I ran a model with 6 layers and the following number of neuron in each layer: 35, 25, 10, 15, 10, 10. Ran for 100 epochs. The outcome was Loss: 0.5589349865913391, Accuracy: 0.7396501302719116. This improved the previous test.





## Summary:
The deep learning model was constructed and trained to predict the success of charitable organizations. The best results are 0.739504396915435 as overall performance. Based on the analysis, a recommendation for improving classification accuracy could involve trying a different model architecture, cleaning outlayers in the data, and fine-tuning hyperparameters. 

