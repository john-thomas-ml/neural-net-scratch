# neural-net-scratch: A From-Scratch Neural Network for MNIST Classification

**neural-net-scratch** is a minimalistic, educational implementation of a feedforward neural network designed to classify handwritten digits from the MNIST dataset. Built entirely from scratch using NumPy, this project demonstrates the core mechanics of neural networks—forward propagation, backpropagation, and gradient descent—without relying on high-level frameworks like TensorFlow or PyTorch. It’s a hands-on showcase of foundational machine learning principles, ideal for learning and portfolio building.

---

## Project Overview

This project implements a Multi-Layer Perceptron (MLP) with the following architecture:
- **Input Layer**: 784 units (flattened 28x28 MNIST images).
- **Hidden Layer**: 10 units with ReLU activation.
- **Output Layer**: 10 units with softmax activation (for 10 digit classes).
- **Loss Function**: Cross-entropy loss.

The network is trained on a batch of 1000 samples from the MNIST training set, emphasizing a deep understanding of neural network fundamentals.

---

## Key Features

- **Data Preprocessing**: Loaded, reshaped, and normalized MNIST data for efficient computation.
- **Forward Propagation**: Implemented using vectorized matrix operations for speed and clarity.
- **Backward Propagation**: Coded the gradient calculations from scratch, applying the chain rule.
- **Training**: Used gradient descent over 1000 iterations to optimize weights and biases.
- **Evaluation**: Computed accuracy on both training and test sets to assess performance.

---

## Latest Results

- **Training Accuracy**: 97% on a batch of 1000 samples.
- **Test Accuracy**: 81.19% on the full MNIST test set (10,000 samples).

The gap between training and test accuracy indicates overfitting, a common issue when training on a small, fixed batch. This project focuses on understanding core concepts rather than exhaustive optimization.

---

## What I Learned

This project sharpened my skills in:
- **Neural Network Fundamentals**: Gained a deep understanding of forward/backward propagation, activation functions, and loss computation.
- **Numerical Computing**: Mastered efficient, vectorized operations with NumPy.
- **Optimization**: Implemented and analyzed gradient descent for model training.
- **Critical Analysis**: Diagnosed overfitting and proposed solutions based on ML theory.

These skills are transferable to more complex deep learning tasks and frameworks.

---

## Technical Details

The implementation is grounded in core machine learning equations, all coded from scratch. Key components include:
- Forward propagation with ReLU and softmax activations.
- Backward propagation using the chain rule for gradient computation.
- Weight and bias updates via gradient descent.