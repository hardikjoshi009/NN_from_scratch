# NumPy Neural Network Implementation

This project implements a flexible neural network using NumPy from scratch, incorporating L1, L2, and combined regularization techniques to improve model generalization. The network is trained on the K-MNIST dataset, which consists of Japanese character images. 

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Model Architecture](#model-architecture)
- [Regularization Techniques](#regularization-techniques)
- [Results](#results)

## Overview

The primary goal of this project is to provide a fully customizable neural network built entirely using NumPy. Users can modify the number of hidden layers, neurons, activation functions, and regularization methods (L1, L2, or combined). This project emphasizes understanding the underlying mechanics of neural networks, including forward and backward propagation, weight initialization, and optimization methods.

## Features

- **Customizable architecture**: Modify hidden layers, neurons, and activations.
- **Regularization support**: L1, L2, and combined (Elastic Net) regularization.
- **Forward/Backward Propagation**: Handcrafted implementation for full transparency into neural network computations.
- **Gradient Descent Optimizer**: Integrated with regularization for weight updates.
- **Trained on K-MNIST Dataset**: Image classification on 10 Japanese characters.

## Model Architecture

- **Input Layer**: 784 neurons (representing 28x28 pixel images)
- **Hidden Layers**: Fully connected, customizable number of layers and neurons, with ReLU activation by default.
- **Output Layer**: 10 units (corresponding to 10 character classes) with softmax activation.
- **Loss Function**: Cross-Entropy Loss.
- **Optimizer**: Gradient Descent with integrated regularization.

The flexibility of the architecture allows users to experiment with different configurations, enabling exploration of deeper networks or varied activation functions.

## Regularization Techniques

- **L1 Regularization**: Encourages sparsity in weights, reducing overfitting by adding a penalty proportional to the sum of absolute values of the weights.
  
  $$ L_{L1} = \lambda \sum |W| $$

- **L2 Regularization**: Prevents overfitting by adding a penalty proportional to the sum of the squared values of the weights.
  
  $$ L_{L2} = \lambda \sum W^2 $$

- **Combined Regularization**: A mix of both L1 and L2 regularization (Elastic Net), combining their benefits.
  
  $$ L_{combined} = \lambda_1 \sum |W| + \lambda_2 \sum W^2 $$

## Results

The neural network was trained on the K-MNIST dataset, achieving the following accuracies with different regularization methods:

- **L1 Regularization**: 78.04% accuracy
- **L2 Regularization**: 79.01% accuracy
- **Combined Regularization**: 79.78% accuracy

