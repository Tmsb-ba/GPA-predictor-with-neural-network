# GPA Prediction Project

This repository contains a machine learning project aimed at predicting students' GPA over time using deep learning frameworks, specifically TensorFlow/Keras and PyTorch. The project explores two different approaches to predicting GPA, demonstrating how different frameworks can be applied to the same problem.

## Overview

The project is divided into two main parts:

1. **Prediction of GPA using TensorFlow/Keras**

2. **Prediction of GPA using PyTorch**

The goal is to compare the performance of these implementations and analyze their suitability for the given dataset and task.

## Dataset

The dataset contains multiple features such as:

* GPA: The target variable to be predicted.

* StudyTimeWeekly: The weekly hours spent studying.

* Attendance: Class attendance rate.

* Extracurricular Activities: Participation rate in extracurriculars.

* Demographic Information: Age, gender, and ethnicity.


## Approaches

### TensorFlow/Keras Implementation
*  All features were normalized using standard scaling to ensure all features have comparable ranges.
*  The dataset was split into training (70%) and testing (30%) subsets for model evaluation.
#### Model Architecture
A fully connected deep neural network (DNN) was designed.
The network consists of:

* 5 hidden layers with decreasing units (256 → 16) and ReLU activations.
* A final dense layer for regression output (GPA prediction).
#### Training
* Mean Squared Error (MSE) was used as the loss function.

* The Adam optimizer was chosen for efficient training.

* The model was trained over 30 epochs with a batch size of 32.
  
### PyTorch Implementation
#### Preprocessing
* The raw numerical data was directly used without any normalization or encoding.

* The dataset was divided into training and testing sets (70/30 split).

No additional preprocessing steps, such as handling missing values or feature selection, were applied.

#### Model Architecture

A fully connected neural network (3 layers) was implemented using PyTorch:

* Input layer with 64 neurons.

* Hidden layers with 64 and 32 neurons, activated by ReLU.

* Output layer with 1 neuron for regression (GPA prediction).

#### Training

* The Mean Squared Error (MSE) loss function was used.

* The Adam optimizer was employed with a learning rate of 0.01.

* The model was trained for 250 epochs.



