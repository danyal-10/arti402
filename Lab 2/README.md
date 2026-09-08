# ARTI 402 — Deep Learning

## Lab 2: Activations, Loss, and How a Network Learns

This folder contains the completed notebook for Lab 2 in the ARTI 402 Deep Learning course.
The lab explains how activation functions, loss functions, gradients, and backpropagation allow a neural network to learn.

## Student Information

- Student ID: 2240002713
- Course: ARTI 402 — Deep Learning
- Lab: Lab 2

## Lab Objectives

The main objectives of this lab are:

- Demonstrate that multiple linear layers can be represented by one equivalent linear layer when no activation function is used.
- Implement ReLU and Sigmoid activation functions using NumPy.
- Build a reusable dense layer for a feedforward neural network.
- Implement the Softmax activation function for multiclass classification.
- Calculate categorical cross-entropy loss.
- Estimate derivatives numerically.
- Apply gradient descent to minimize a function.
- Calculate gradients through a neuron using the chain rule.
- Build and train a complete neural network using NumPy.

## Notebook Content

### 1. Linear Layer Collapse

The notebook combines two linear layers into one equivalent layer and verifies that both produce the same output.

### 2. Activation Functions

ReLU and Sigmoid are implemented without Python loops so they can operate efficiently on complete NumPy arrays.

### 3. Dense Layer

A `Layer_Dense` class is created with randomly initialized weights, zero biases, and a forward-pass method.

### 4. Softmax

The Softmax function converts the output scores into class probabilities. Numerical stability is improved by subtracting the maximum value in each row before exponentiation.

### 5. Categorical Cross-Entropy Loss

Categorical cross-entropy measures the error between the predicted probabilities and the correct class labels. Prediction values are clipped to prevent calculating `log(0)`.

### 6. Numerical Derivatives

The derivative of a function is estimated using the centered difference method.

### 7. Gradient Descent

Gradient descent is used to minimize a quadratic function by repeatedly updating the input in the direction that reduces the function value.

### 8. Backpropagation

The backward pass of a single neuron is calculated using the chain rule. The analytical gradients are compared with numerical derivatives to verify their correctness.

### 9. Final Assessment

The final assessment builds and trains the following neural network:

```text
Input (2 features)
→ Dense Layer (8 neurons)
→ ReLU
→ Dense Layer (3 outputs)
→ Softmax
→ Categorical Cross-Entropy Loss
```

The network is trained for 150 epochs using numerical gradients.

## Results

- Starting loss: 1.0971
- Starting accuracy: 47.00%
- Final loss: 0.1846
- Final accuracy: 92.67%

All exercises and assessment checks pass successfully.

## Requirements

- Python 3
- NumPy
- Matplotlib
- Jupyter Notebook or Google Colab

No additional machine-learning frameworks such as TensorFlow, PyTorch, or scikit-learn are used.

## Dataset

The dataset is generated directly inside the notebook using the provided `vertical_data` function. No external dataset, download, API, or internet connection is required.

## File

- `arti402_Lab2_2240002713.ipynb` — completed notebook with code and visible outputs

## How to Run

1. Open `arti402_Lab2_2240002713.ipynb` in Jupyter Notebook or Google Colab.
2. Restart the runtime or kernel.
3. Run all cells from top to bottom in order.
4. Confirm that every exercise and assessment check displays a passed message.

## Submission Notes

- Keep the notebook inside the Lab 2 folder in the course repository.
- Make sure the notebook filename includes the student ID.
- Keep all generated outputs visible before uploading the notebook to GitHub.
