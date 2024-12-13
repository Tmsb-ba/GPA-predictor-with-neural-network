# GPA Prediction Project
## Introduction

This repository presents a machine learning project aimed at predicting students' Grade Point Average (GPA) using deep learning. The project explores two distinct approaches using TensorFlow/Keras and PyTorch frameworks. By applying these models to the same dataset, the project aims to highlight their differences and compare their performance for GPA prediction.

## Dataset

The dataset contains multiple features such as:

* GPA: The target variable to be predicted.

* StudyTimeWeekly: The weekly hours spent studying.

* Attendance: Class attendance rate.

* Extracurricular Activities: Participation rate in extracurriculars.

* Demographic Information: Age, gender, and ethnicity.


## Models

The project is divided into two main parts:

1. **Prediction of GPA using TensorFlow/Keras**

2. **Prediction of GPA using PyTorch**

For the TensorFlow/Keras implementation, all numerical features were normalized using standard scaling to ensure consistent ranges. The dataset was split into training (70%) and testing (30%) subsets. The model was a fully connected deep neural network (DNN) with five hidden layers, each with progressively decreasing units (256 → 16) and ReLU activations. The final output layer contained one neuron for GPA regression. Training was conducted over 30 epochs with a batch size of 32 using the Mean Squared Error (MSE) loss function and the Adam optimizer.

For the PyTorch implementation, the raw numerical data was used directly without normalization or encoding. The dataset was split into training (70%) and testing (30%) subsets. The model consisted of a fully connected neural network with two hidden layers (64 and 32 neurons) using ReLU activations, and a final output layer with one neuron for GPA regression. Training was performed over 250 epochs using the Mean Squared Error (MSE) loss function and the Adam optimizer with a learning rate of 0.01.

## Results

For TensorFlow/Keras model

* Test Loss (MSE): 0.0561

* Test Mean Absolute Error (MAE): 0.1549

For PyTorch model

* Test R-Squared (R² Score): 0.8901

The TensorFlow/Keras model showed strong performance with low test loss and MAE, while the PyTorch model achieved a high R² score, indicating that it effectively explained the variance in the GPA values.

