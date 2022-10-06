# Lecture 2 - Machine Learning Review
## The Machine Learning Process vs. Deep Learning Process
A typical ML pipeline consists of feature extraction, model optimizaiton, and inference. In a Deep Learning model, the pipeline only consists of the optimization and inference stages.

Feature extraction is typically a hard problem. Which features of a dataset are significant to solving a given problem is often left to the creator of the model, or is a lengthy part of the design process. Oftentimes feature extraction is the sole differentiator of a good vs. great model.


Deep Learning extracts features throughout the model, with deeper layers having more semantic meaning than earlier layers.

Deep Learning is typically supervised learning, aka data with known labels and whose goal is to predict a label given an input. These can include classification or regression tasks.
## Optimization
Models are trained to optimize a certain function, usually, the maximum or minimum error extrema, hopefully global or close to it. In Deep Learning, the optimization process usually creates optimizations that are close enough to global min or max.  


Convex Optimization: Global min or max exists

Non-convex Optimization: Global min or max does not exist, several local min or max possible
We optimize models by deriving and finding when it crosses 0. That is, when a function's derivative goes from decreasing to increasing or vice versa.

>

## Gradient Descent
We use the derivative of a f(x) to find out what number of guess next.
```
given some f(x)

initialize some x to something

if f'(x) > 0: x--
else if f'(x) < 0: x++
else: x is optimized
```

Size of increment is a hyperparameter and should depend on the magnitude of f'(x).


## Tensors
Tensors are a generalization of a collection of numbers.

``` 
0D: 1
1D: [1, 2]
2D: [[1, 2], [3, 4]]
```

The dimension of a tensor is shown above, and the size of a tensor is defined as the number of elements it contains. The goal is to represent any dataset, with any number of dimensions and elements.

Practically, we can represent an RGB image of 128 x 128 size as a tensor of 3 channels, 128x128 pixels.

```
[3 x 128 x 128]
```

