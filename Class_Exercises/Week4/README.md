# Week 4 Perceptron Learning

This exercise implements a single-layer perceptron and trains it to reproduce the OR logic gate. The OR dataset is linearly separable, making it suitable for demonstrating perceptron learning, weight updates, predictions, and a two-dimensional decision boundary.

## Files

- [Open the Week 4 notebook](perceptron_or_gate.ipynb)
- [Return to the module repository](../../README.md)

## Learning objectives

The completed exercise will demonstrate how to:

- represent a Boolean logic gate as a machine-learning dataset;
- calculate a weighted sum using inputs, weights, and a bias;
- apply a binary step activation function;
- update perceptron parameters from prediction errors;
- train over repeated epochs until the samples are classified correctly;
- evaluate predictions against the OR truth table; and
- visualise the learned linear decision boundary.

## OR-gate dataset

| Input A | Input B | Expected output |
| ---: | ---: | ---: |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

The only negative example is `(0, 0)`. The other three combinations belong to the positive class.

## Environment

The notebook uses Python with:

- [NumPy](https://numpy.org/) for numerical operations; and
- [Matplotlib](https://matplotlib.org/) for visualisation.

Open the notebook in JupyterLab, select **Python [conda env:University]**, and run the cells in order.

## Exercise status

The dataset setup is complete. The perceptron activation function, training process, evaluation, visualisation, and final findings will be added as the exercise progresses.

