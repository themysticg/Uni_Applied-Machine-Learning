# Week 3 - OR Gate: Perceptron, TensorFlow and PyTorch

This exercise implements the OR logic gate in three ways: a perceptron built from scratch, a TensorFlow neural network and a PyTorch neural network. It follows the examples in *Week 3 day 2.pptx*. The OR dataset is linearly separable, making it suitable for learning about weights, bias, activation functions and training.

## Files

- [From-scratch perceptron](perceptron_or_gate.ipynb) - manual updates, training errors and decision boundary plots.
- [TensorFlow implementation](tensorflow_or_gate.ipynb) - a sigmoid neuron trained through the Keras API.
- [PyTorch implementation](pytorch_or_gate.ipynb) - a sigmoid neuron with an explicit training loop.
- [Return to the module repository](../../README.md)

## Learning objectives

The completed notebooks demonstrate how to:

- represent a Boolean logic gate as a machine-learning dataset;
- calculate a weighted sum using inputs, weights, and a bias;
- apply a binary step activation function;
- update perceptron parameters from prediction errors;
- train over repeated epochs until the samples are classified correctly;
- evaluate predictions against the OR truth table; and
- visualise the learned linear decision boundary;
- train a sigmoid neuron using binary cross-entropy and SGD; and
- compare manual perceptron updates with TensorFlow and PyTorch training.

## OR-gate dataset

| Input A | Input B | Expected output |
| ---: | ---: | ---: |
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

The only negative example is `(0, 0)`. The other three combinations belong to the positive class.

## Environment

The notebooks use the `University` Python environment with:

- [NumPy](https://numpy.org/) for numerical operations;
- [Matplotlib](https://matplotlib.org/) for visualisation;
- [TensorFlow](https://www.tensorflow.org/) for the Keras implementation; and
- [PyTorch](https://pytorch.org/) for the explicit training loop.

TensorFlow and PyTorch were installed and checked on 6 October 2026. Open a notebook in JupyterLab or VS Code, select **Python (University)** (also displayed as **Python [conda env:University]**), and run the cells in order. Executed outputs are saved in each notebook.

## Completed work - 6 October 2026

- Confirmed the from-scratch perceptron implementation, including its training errors, decision boundary and predictions.
- Completed the TensorFlow implementation with commented code, probability predictions, learned parameters and a comparison with the manual perceptron.
- Completed and ran the PyTorch implementation from slides 16-19, explaining the forward pass, loss calculation, `zero_grad()`, `backward()` and `step()`.
- Checked that all three implementations reproduce the OR truth table.
- Corrected the exercise folder, notebook heading and repository links from Week 4 to Week 3.

## Results

| Implementation | Epochs | Binary predictions | Correct truth-table outputs | Final loss |
| --- | ---: | --- | ---: | ---: |
| From-scratch perceptron | 20 | `[0, 1, 1, 1]` | 4/4 (100%) | Not applicable |
| TensorFlow | 500 | `[0, 1, 1, 1]` | 4/4 (100%) | 0.1515 |
| PyTorch | 1,000 | `[0, 1, 1, 1]` | 4/4 (100%) | 0.0855 |

These results use the same four examples for training and evaluation. They confirm that each model learned the complete OR truth table, rather than measuring performance on unseen data. The TensorFlow and PyTorch losses are from runs with different initialization and epoch counts, so they do not establish that one framework is better.

The manual perceptron uses a step activation and corrections based on classification mistakes. TensorFlow and PyTorch use sigmoid probabilities and gradient-based optimization of binary cross-entropy. TensorFlow handles training through `model.fit()`; PyTorch makes each stage visible in the training loop.

