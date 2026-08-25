# Activation Functions in Neural Networks

## Project Overview

This project demonstrates the importance of **activation functions in Artificial Neural Networks (ANNs)** and explains how they enable neural networks to learn complex, non-linear relationships.

Using the **make_moons** dataset, the notebook explores how different activation functions influence the learning behavior of a neural network and its ability to model non-linear decision boundaries.

The project focuses on building a strong conceptual understanding of why activation functions are essential in Deep Learning.

---

## Objective

The main objectives of this project are to:

* Understand why activation functions are required in neural networks
* Understand how activation functions introduce non-linearity
* Explore commonly used activation functions
* Visualize the behavior of different activation functions
* Understand the effect of activation functions on neural network learning
* Analyze how activation functions help solve non-linear classification problems

---

## Dataset

The project uses the **make_moons** dataset from Scikit-learn.

```python id="4x1xk2"
make_moons(
    100,
    noise=0.25,
    random_state=2
)
```

### Dataset Characteristics

* **Samples:** 100
* **Features:** 2
* **Problem Type:** Binary Classification
* **Noise:** 0.25
* **Random State:** 2
* **Dataset Type:** Synthetic

The `make_moons` dataset is useful for demonstrating neural networks because the classes form a **non-linear pattern** that cannot be effectively separated using a simple linear decision boundary.

---

## Why Do Neural Networks Need Activation Functions?

Without activation functions, multiple layers of a neural network would effectively behave like a single linear transformation.

Activation functions introduce **non-linearity**, allowing neural networks to learn complex relationships and decision boundaries.

```text id="v7x1m2"
Input
  ↓
Linear Transformation
  ↓
Activation Function
  ↓
Linear Transformation
  ↓
Activation Function
  ↓
Output
```

This non-linearity is one of the key reasons neural networks can solve complex problems.

---

## Activation Functions Covered

### 1. Sigmoid

The Sigmoid function maps values approximately between **0 and 1**.

It is commonly used for binary classification output layers.

**Advantages:**

* Output is easy to interpret as a probability
* Useful for binary classification

**Limitations:**

* Can suffer from vanishing gradients
* Saturates for very large or very small inputs

---

### 2. Tanh

Tanh maps values between **-1 and 1**.

Compared with Sigmoid, it is zero-centered and can sometimes provide better optimization behavior.

**Limitation:**

* Can still suffer from the vanishing gradient problem.

---

### 3. ReLU

ReLU stands for **Rectified Linear Unit**.

It outputs zero for negative values and keeps positive values unchanged.

ReLU is one of the most commonly used activation functions in hidden layers of neural networks.

**Advantages:**

* Simple and computationally efficient
* Helps reduce the vanishing gradient problem compared with Sigmoid/Tanh
* Works well in many Deep Learning architectures

**Limitation:**

* Can suffer from the **dying ReLU** problem.

---

### 4. Leaky ReLU

Leaky ReLU introduces a small negative slope instead of making all negative values zero.

This helps reduce the dying ReLU problem.

---

### 5. Softmax

Softmax converts multiple output values into a probability distribution whose values sum to 1.

It is commonly used in the output layer for **multi-class classification**.

---

## Visualization

The notebook visualizes different activation functions to understand:

* Their input-output relationship
* Linear vs non-linear behavior
* Saturation regions
* Gradient behavior
* Differences between activation functions

These visualizations make it easier to understand why different activation functions behave differently during neural network training.

---

## Project Workflow

The notebook follows a practical workflow:

1. Generate the `make_moons` dataset
2. Visualize the dataset
3. Understand the need for non-linearity
4. Explore different activation functions
5. Visualize activation function curves
6. Build a neural network
7. Apply activation functions
8. Train the model
9. Analyze model behavior
10. Compare activation functions

---

## Key Concepts Covered

* Artificial Neural Networks
* Activation Functions
* Linear Transformation
* Non-Linearity
* Sigmoid
* Tanh
* ReLU
* Leaky ReLU
* Softmax
* Binary Classification
* Decision Boundaries
* Vanishing Gradient Problem
* Dying ReLU Problem

---

## Key Learnings

### Activation Functions Introduce Non-Linearity

Without activation functions, a deep neural network would not be able to effectively learn complex non-linear relationships.

### ReLU is Widely Used

ReLU is commonly used in hidden layers because it is simple, efficient, and generally provides better gradient behavior than Sigmoid and Tanh.

### Different Layers Can Use Different Activations

The best activation function depends on the purpose of the layer and the type of problem.

### Output Activation Depends on the Task

For example:

* **Binary classification:** Sigmoid
* **Multi-class classification:** Softmax
* **Hidden layers:** ReLU or related variants

---

## Technologies Used

* **Python**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Scikit-learn**
* **TensorFlow / Keras**
* **Jupyter Notebook**

---

## Learning Outcomes

After completing this project, I gained a better understanding of:

* Why activation functions are fundamental to neural networks
* How non-linearity enables neural networks to learn complex patterns
* Differences between common activation functions
* Why ReLU is widely used in hidden layers
* Why Sigmoid and Softmax are commonly used for classification outputs
* How activation functions influence neural network training

---

## Future Improvements

Possible extensions include:

* Compare training performance using different activation functions
* Visualize decision boundaries for each activation function
* Compare convergence speed
* Experiment with different neural network architectures
* Analyze gradient behavior
* Demonstrate the dying ReLU problem
* Demonstrate the vanishing gradient problem
* Experiment with modern activation functions such as GELU and Swish

---

## Project Purpose

This project is part of my **Deep Learning learning journey**, focused on understanding the fundamental components of neural networks.

The goal is not only to learn how to use activation functions in frameworks such as TensorFlow/Keras, but also to understand **why they are necessary and how they affect the learning process**.

---

## Final Takeaway

**Activation functions are what allow neural networks to move beyond simple linear relationships.**

They introduce non-linearity, enabling neural networks to learn complex patterns and decision boundaries.

Understanding activation functions is therefore essential for developing a strong foundation in **Deep Learning and Neural Network architecture**.
