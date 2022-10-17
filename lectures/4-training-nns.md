# Neural Networks in Practice
In the real world, neural networks look like a bunch of connected sets of layers.

Backpropagation allows us to take a derivative of an output with respect to its input, indefinitely.

In practice, Activation Layers are usually split into their own layer.

# What Goes Wrong
Sometimes model is bad, for many reasons.

1. Getting things wrong
2. Training too long
3. Training is unstable

## Bias vs. Variance
High bias (low noise) can't fit legitimate patterns. High variance (high noise) doesn't generalize well.

We want a happy middle, so we can encourage the model to make "smooth" moves. We can do this by limiting the magnitude of weights. This is called regularization.

We basically just penalize the model for using weights that are too big by adding the magnitude of the weights to loss.

## Momentum
SGD is a slow process. We often move in the same direction over multiple training steps. We can make the model move faster if it moves in the same direction multiple times by adding a momentum multiplier to the weight update.

## Choosing Activation Functions
Activation Functions can cause a network to get stuck. Some older ones were popular. Just use ReLU or Leaky ReLU.
