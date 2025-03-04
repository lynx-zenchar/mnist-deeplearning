# Keras MNIST CNN

This notebook shows my attempt at building, training, and evaluating a Convolutional Neural Network (CNN) using Keras on the MNIST dataset.

## Overview

The notebook includes the following steps:
- **Data Loading & Exploration:**  
  Loads the MNIST dataset and displays sample images to familiarize users with the data.

- **Data Preprocessing:**  
  Normalizes the image data and reshapes it to add a channel dimension. It also converts the labels to categorical format for multi-class classification.

- **Model Building:**  
  Constructs a sequential CNN model with:
  - A convolutional layer (32 filters with a 4x4 kernel and ReLU activation)
  - A max pooling layer to reduce spatial dimensions
  - A flattening layer to transform 2D data to 1D
  - A fully connected (dense) layer with 128 neurons (ReLU activation)
  - An output layer with 10 neurons (softmax activation) for class probabilities

- **Model Compilation & Training:**  
  The model is compiled with the `categorical_crossentropy` loss function and `rmsprop` optimizer, then trained for 2 epochs.

- **Model Evaluation:**  
  Evaluates the trained model on the test set and uses scikit-learn’s classification report to present detailed performance metrics.

## Requirements

To run this notebook, you need to have the following Python packages installed:
- Python 3.x
- [Keras](https://keras.io/) (and a backend such as TensorFlow)
- [NumPy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)
- [scikit-learn](https://scikit-learn.org/)

You can install these using pip, for example:

```bash
pip install keras tensorflow numpy matplotlib scikit-learn
