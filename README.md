# MNIST Handwritten Digit Classification using MLP

This project implements a Multilayer Perceptron (MLP), a type of feedforward neural network, using TensorFlow and Keras to classify handwritten digits (0-9) from the MNIST dataset.

## Project Overview

This notebook provides a basic example of image classification using a fully connected neural network:
* **Data Loading:** Loads the MNIST dataset from `tensorflow.keras.datasets`.
* **Preprocessing:**
    * **Flattens** the 28x28 pixel images into 1D vectors of 784 features.
    * Normalizes pixel values to the range [0, 1].
    * **One-hot encodes** the integer labels (0-9) into a categorical format.
* **Model Building:** Defines a `Sequential` MLP model consisting only of `Dense` layers.
* **Training:** Trains the model on the MNIST training data.
* **Evaluation:** Evaluates the trained model's performance on the test dataset.
* **Prediction:** Demonstrates how to predict the class of a single test image and visualize the result.

---

## Dataset: MNIST Handwritten Digits

* **Source:** `tensorflow.keras.datasets.mnist`
* **Content:** Grayscale images of handwritten digits (0-9).
* **Size:** 60,000 training images, 10,000 testing images.
* **Dimensions:** Each image is 28x28 pixels.
* **Classes:** 10 (digits 0 through 9).


---

## Model Architecture

The model is a simple `Sequential` MLP with three layers:

1.  **Input/First Hidden Layer:**
    * `Dense` layer with 128 units.
    * Activation function: `relu` (Rectified Linear Unit).
    * `input_shape=(784,)` - Expects a flattened vector of 784 features.

2.  **Second Hidden Layer:**
    * `Dense` layer with 128 units.
    * Activation function: `relu`.

3.  **Output Layer:**
    * `Dense` layer with 10 units (one for each digit class).
    * Activation function: `softmax` - Outputs a probability distribution across the 10 classes.

**Compilation:**
* **Optimizer:** `adam`
* **Loss Function:** `categorical_crossentropy` (standard for multi-class classification with one-hot labels)
* **Metrics:** `accuracy`

---

## Requirements

You'll need these Python libraries:

* `tensorflow`
* `numpy`
* `matplotlib`

Install them using pip:
```bash
pip install tensorflow numpy matplotlib
