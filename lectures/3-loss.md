# Loss Functions
Loss functions take in model parameters and returns how wrong an answer was.

By calculating the loss at various places, we can begin taking derivatives. Once we have a derivative, we can begin to shift weights around to get us to a local min or maxima.

## Basic ML Models
Linear Regression is used for predicting real-valued outputs. This means numbers.

Logistic Regression is used for predicting classes. This means labels.

Both use the same math under the hood, with a small difference at the end.

## Feature Engineering
One problem of ML is feature engineering. Arguably, it's the core problem of Machine Learning -- which subset of features do we use to create the best model?

One reason is that some data cannot be modeled accurately with a linear model. Imagine a donut.

Deep Learning can be thought of a solution to the problem: Allowing a computer to decide what features are important, on its own.

# Activation Functions
Because the layers of a network can be thought of as a bunch of matrix multiplication, we can think of any given layer as X_i and its weights as w. We can then feed X_i(w) into an activation function, A. A(X_i(w)).

The activation function is a key part of what makes feature extraction work. Without it, the math works out such that it's basically just the same as multiplying everything through, just like in Linear/Logistic regression.

Therefore, we need to use some non-linear activation function. This will allow for some features to "drop" out of the model (or in math terms, become 0).

# Back Propagation
First, run the model through and make a prediction. Calculate the loss, and find out which direction we want to go, up or down.

Next, go back one layer. Using the last node's partial derivative as a target, find out how much each node should change (make a derivative). Keep that in mind, and continue backwards.

The goal is to find out how each weight affects the output, and to adjust the weights depending on which final direction we want to move.

## The Math
1. Calculate final output
2. Calculate loss 
3. Calculate partial derivative of loss w.r.t. a weight at the end of the network
4. Continue calculating partial derivatives for weights leading up to that weight
5. Partially derive the activation functions at nodes
6. Calculate final derivative once you get back to the input layer
7. Once you have all the derivatives, you can solve for the deriviative of any weight w.r.t the output, aka the update.

