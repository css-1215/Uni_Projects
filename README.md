ANN2122890: Handwritten Digit Recognition with Customizable Neural Networks
This project implements an artificial neural network (ANN) in MATLAB for recognizing handwritten digits from the MNIST dataset. The function, ann2122890.m, supports both a three-layer (one hidden layer) and a five-layer (three hidden layers) network architecture. It provides options for different learning rates, backpropagation methods, and error functions, allowing you to experiment with various training configurations.

Table of Contents:

Overview

Project Structure

Usage

Parameters

Dataset

Results

Requirements

License

Overview
The ann2122890 function is designed to train a neural network on a subset of the MNIST dataset. It normalizes the input data, sets up a one-hot encoding for the target outputs, and performs forward and backward propagation based on your configuration parameters. The function is particularly tailored by validating a specific student ID (2122890) and custom network architecture parameters.

Key features include:

Customizable Architecture: Choose between one hidden layer with Nh neurons or three hidden layers with u, v, and w neurons.

Flexible Backpropagation: Two backpropagation options are available (heuristic unscaled or calculus-based).

Error Metrics: Use either total squared error or cross-entropy as your performance index.

Visualization: Optionally display training progress and sample predictions with graphics.

Project Structure

ann2122890.m             (Main MATLAB function file)

mnist_train_1000.csv       (Training data file (first 1000 MNIST samples))

mnist_test_100.csv          (Testing data file (first 100 MNIST samples))

README.md                 (This README file)

Usage

Prepare the Workspace:
Ensure that the MNIST CSV files (mnist_train_1000.csv and mnist_test_100.csv) are in the same directory as ann2122890.m.

Run the Function:

In MATLAB, call the function with your desired parameters. For example:

[Yn, On, Yt, Ot, pc, tc] = ann2122890(2122890, 50, 0.01, 2, 25, 33, 34, 37, 1, 1, 1);
This example runs the network for 50 epochs with a learning rate of 0.01, using calculus-based backpropagation, a single hidden layer of 25 neurons, and squared error as the performance metric.

Interpret the Output:

Yn and Yt contain the true one-hot encoded labels for the training and testing sets.

On and Ot are the network's output predictions.

pc and tc represent the predicted and true classification vectors, respectively.

Parameters
ID: Your student ID (must be 2122890 for this implementation).

N_ep: Number of training epochs.

lr: Learning rate for weight updates.

bp: Backpropagation method (1 for heuristic unscaled, 2 for calculus-based).

Nh: Number of neurons in the hidden layer (if using one hidden layer).

u, v, w: Number of neurons in the three hidden layers (if using three hidden layers; must be 33, 34, and 37, respectively).

cf: Cost function choice (1 for total squared error, 2 for cross-entropy).

gfx: Flag to enable/disable graphics (0 for no graphics, nonzero to show graphics).

HL: Hidden layer configuration (1 for one hidden layer, 3 for three hidden layers).

Dataset
The project uses a subset of the MNIST dataset:

Training Set: 1000 samples from mnist_train_1000.csv

Testing Set: 100 samples from mnist_test_100.csv

Make sure these files are present in your project directory.

Results
The function prints the accuracy of the network on both the training and testing sets. Additionally, when graphics are enabled, it displays:

The performance index (error) per epoch.

A bar plot of the predicted output for each digit.

The corresponding MNIST image.

A dynamic plot tracking wins and losses during classification.

Requirements
MATLAB R2016b or later (for the use of readmatrix and modern graphics functions).

Basic MATLAB toolboxes for matrix operations and visualization.

License
This project is provided for educational purposes. Feel free to modify and improve the code as needed.














