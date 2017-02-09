---
title: Chapter 1 - Introduction
layout: default
---

### Machine Learning: What and Why?

> We are drowning in information and starving for knowledge. John Naisbitt. (p. 1)

Loose definition of **machine learning**: "automated methods of data analysis" or "a set of methods that can automatically detect patterns in data, and then use the uncovered patterns to predict future data, or to perform other kinds of decision making under uncertainty." (p. 1)

The book assumes probability theory is the best framework to study machine learning. (p. 1)

**Long tail**: "Few things are very common, but most things are quite rare." (p. 2) Implication? We are still learning from only a small set of data "even if the total amount of data is large" (p. 2)

### Types of Machine Learning

1. Supervised learning

Given labeled or known input-output pairs: $D = \{\textbf{x_i}, y_i\}_{i=1}^{N}$

- Classification: when the data is categorical
- Regression: when the data is continuous

2. Unsupervised learning

Given unlabeled data: $D = \{\textbf{x_i}\}_{i=1}^{N}$

Less well-defined problem.

3. Reinforcement learning (p.)

Not covered.

### Supervised learning

"To handle ambiguous cases... it is desirable to return a probability." Given an input vector $\textbf{x}$ and a training set $D$, we can write:

$$
\hat{y} = \hat{f}(\textbf{x}) = \arg\max_{c \in C} p(y=c|\textbf{x}, D)
$$

In words, this is the most probable class label $c$ for the data and training set. Notice that we are explicitly conditioning on the training data and input vector. To be explicit, we could also condition on the family of models. $\hat{y}$ is also knon as a **MAP estimate** for **maximum a posteriori**. (p. 4)

> Essentially the document classification problem has been reduced to one that looks for subtle changes in the patterns of bits. (p. 5)

### Unsuperived learning

#### Latent factors

> When dealing with high dimensional data, it is often useful to reduce the dimensionality by projecting the data to a lower dimensional subspace which captures the "essence" of the data. This is called **dimensionality reduction**... The motivation behind this technique is that although the data may appear high dimensional, there may only be a small number of degrees of variability, corresponding to **latent factors**. (p. 11-12)

#### Matrix completion

> This is typical of the difference between data mining and machine learning: in data mining, there is more emphasis on interpretable models, whereas in machine learning, there is more emphasis on accurate models. (p. 16)

### Basic concepts

- **Parametric model**: The model has a fixed number of parameters. Advantages: faster to use. Disadvantages: makes stronger assumptions. (p. 16)

- **Non-parametric model**: The number of parameters grows with the amount of training data. Advantages: more flexible. Disadvantages: intractable for large datasets. (p. 16)

### Overfitting

**Overfitting** is when our model captures noise as well as the signal in the data. (p. 22)

### Model selection

How do we pick the best model from a number of models? For example, how do we select $K$ in K-nearest neighbor? One approach is to compute the **misclassification rate** (p. 22-23):

$$
err(f, D) = \frac{1}{N} \sum_{i=1}^{N} \identity(f(\textbf{x_i}) \neq y_i)
$$

### No free lunch

> All models are wrong, but some models are useful. George Box (p. 24)
