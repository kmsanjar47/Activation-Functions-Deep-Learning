# Activation Functions

## What is an activation function?

While building a Neural Network, we mostly have three layers: the input layer, the hidden layer, and the output layer. The neural network has neurons that work in correspondence with weight, bias, and their respective activation function. Activation functions make back-propagation possible, allowing for the update of weights and biases based on the error at the output.

The activation function decides whether a neuron should be activated by calculating the weighted sum and adding bias to it. Its purpose is to introduce non-linearity into the output of a neuron.

## Types of Activation Function:

### Sigmoid Function:

It is a function plotted as an 'S' shaped graph.
**Equation:** A = 1/(1 + e^(-x))
**Graph:**

#### Pros:

- **Smoothness:** The sigmoid function is smooth and differentiable across its entire range, aiding optimization algorithms like gradient descent.
- **Output Range:** Outputs values in the range (0, 1), suitable for binary classification problems.
- **Logistic Interpretation:** Closely related to logistic regression, making it convenient for binary outcomes.

#### Cons:

- **Vanishing Gradient Problem:** Significant issue, especially in deep neural networks.
- **Output Not Centered Around Zero:** Output is not centered around zero.
- **Output Saturation:** Can saturate for extreme input values.
- **Not Zero-Centered:** Not zero-centered, leading to biased weight updates.

### Tanh Function:

The tanh function is a mathematically shifted version of the sigmoid function.
**Equation:** tanh(x) = (e^(2x) - 1) / (e^(2x) + 1)
**Graph:**

#### Pros:

- **Zero-Centered:** Outputs range from -1 to 1, beneficial for optimization algorithms.
- **Smooth and Differentiable:** Similar to the sigmoid function.
- **Output Range:** Outputs values in the range (-1, 1).
- **Less Likely to Saturate:** Tends to saturate less quickly than the sigmoid function.

#### Cons:

- **Vanishing Gradient Problem:** Still prone to the vanishing gradient problem.
- **Non-Zero-Centered in Practice:** Mean of activations may shift away from zero during training.
- **Computational Cost:** Involves exponentiation, computationally more expensive.
- **Not Always Preferable for All Layers:** Might not be the best choice for all layers.

### ReLU Function:

Stands for Rectified Linear Unit, widely used in hidden layers.
**Equation:** A(x) = max(0, x)
**Graph:**

#### Pros:

- **Simple and Efficient:** Computationally efficient with a simple threshold operation.
- **Promotes Sparsity:** Tends to sparsely activate neurons, reducing overfitting.
- **Mitigates Vanishing Gradient Problem:** Does not suffer from the vanishing gradient problem to the same extent.
- **Accelerates Training:** Faster training of deep neural networks.
- **Zero-Centered for Positive Values:** Zero-centered for positive values.

#### Cons:

- **Dead Neurons:** Common issue, leading to inactive neurons.
- **Not Suitable for All Data:** May not be suitable for all types of data.
- **Not Smooth Everywhere:** Not differentiable at zero.
- **Not Always Zero-Centered:** Lack of zero-centeredness for negative values.

## References:
Geeks-for-geeks & Google
Picture collected from Geeks-for-geeks
