# neural-net-scratch: A From-Scratch Neural Network for MNIST Classification

**neural-net-scratch** is a minimalistic, educational implementation of a feedforward neural network built to classify handwritten digits from the MNIST dataset. This project is coded entirely from scratch using NumPy, without relying on high-level frameworks like TensorFlow or PyTorch, to demonstrate the core mechanics of neural networks—forward propagation, backpropagation, and gradient descent. It’s a hands-on showcase of foundational machine learning principles, perfect for learning and portfolio building.

---

## Project Overview

This project implements a Multi-Layer Perceptron (MLP) with the following architecture:
- **Input Layer**: 784 units (flattened 28x28 MNIST images).
- **Hidden Layer**: 10 units with ReLU activation.
- **Output Layer**: 10 units with softmax activation (for 10 digit classes).
- **Loss Function**: Cross-entropy loss.

The network is trained on the full MNIST training set (60,000 samples), emphasizing a deep understanding of neural network fundamentals and practical implementation.

---

## Key Features

- **Data Preprocessing**: Loaded, reshaped, and normalized the entire MNIST dataset for efficient computation.
- **Forward Propagation**: Implemented using vectorized matrix operations for speed and scalability.
- **Backward Propagation**: Coded gradient calculations from scratch, applying the chain rule.
- **Training**: Used gradient descent over 1000 iterations to optimize weights and biases on the full training set.
- **Evaluation**: Assessed performance with accuracy metrics on both training and test sets.

---

## Latest Results

- **Training Accuracy**: 88.5% on the full MNIST training set (60,000 samples).
- **Test Accuracy**: 88.8% on the full MNIST test set (10,000 samples).

These results show a significant improvement in generalization compared to earlier iterations, as training on the full dataset reduced overfitting. The close alignment between training and test accuracy indicates that the model generalizes well, though there’s room for further optimization to reach modern MLP benchmarks (e.g., 98% test accuracy).

---

## What I Learned

This project enhanced my skills in:
- **Neural Network Fundamentals**: Mastered forward/backward propagation, activation functions (ReLU, softmax), and cross-entropy loss.
- **Numerical Computing**: Leveraged NumPy for efficient, vectorized operations on large datasets.
- **Optimization**: Implemented gradient descent and analyzed its behavior on a full dataset.
- **Critical Analysis**: Improved model generalization by scaling from a fixed batch to the full training set, reducing overfitting.

These skills lay a strong foundation for tackling advanced deep learning challenges and working with modern frameworks.

---

# Technical Details
The implementation is built on core machine learning equations, all coded from scratch:

## Forward Propagation
- **Hidden layer:** $Z_1 = W_1 \cdot X + b_1, \quad A_1 = \text{ReLU}(Z_1)$
- **Output layer:** $Z_2 = W_2 \cdot A_1 + b_2, \quad A_2 = \text{softmax}(Z_2)$

softmax(Z<sub>2</sub>)<sub>i</sub> = exp(Z<sub>2i</sub>) / &sum;<sub>j=1</sub><sup>n</sup> exp(Z<sub>2j</sub>)


## Backward Propagation
- **Output layer:** $\frac{\partial L}{\partial Z_2} = A_2 - Y, \quad dW_2 = \frac{1}{m} \sum (A_1 \cdot dZ_2^T)$
- **Hidden layer:** $\frac{\partial L}{\partial Z_1} = (W_2^T \cdot dZ_2) \odot \text{ReLU}'(Z_1), \quad dW_1 = \frac{1}{m} \sum (X \cdot dZ_1^T)$

## Parameter Updates
$W \gets W - \alpha \cdot dW, \quad b \gets b - \alpha \cdot db$