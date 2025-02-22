# Support Vector Machines (SVM) – A Theoretical Overview

Support Vector Machines (SVM) are one of the most powerful supervised learning algorithms for classification. At their core, SVMs aim to find the optimal decision boundary that maximizes the margin between data points of different classes. This margin is defined by a subset of training points called **support vectors**, which directly influence the boundary’s position.

## Core Idea

SVM operates by constructing a hyperplane in a high-dimensional space that best separates the data points of different classes. The key principle is maximizing the margin, which makes the model generalize well to unseen data. The optimization problem involves minimizing a quadratic function subject to linear constraints, making it a convex problem with a unique global solution.

## Handling Nonlinear Data

Real-world datasets are often not linearly separable. SVMs tackle this challenge using the kernel trick, which makes the necessary dot product calculations as if the data is mapped into a higher-dimensional space where a linear boundary can be found. Common kernels include:

- **Polynomial Kernel:** Captures curved decision boundaries.
- **Radial Basis Function (RBF) Kernel:** Maps points into an infinite-dimensional space, making it highly effective for complex data distributions.

## Soft-Margin SVM

In practical applications, datasets may contain outliers or overlapping classes. The soft-margin SVM introduces a trade-off between maximizing the margin and minimizing classification errors by allowing some misclassification through slack variables.

## Computational Considerations

While the standard SVM formulation requires solving a quadratic programming problem, real-world implementations often rely on more efficient optimization techniques such as **Sequential Minimal Optimization (SMO)**, which decomposes the problem into smaller, manageable subproblems. An implementation of SMO is made in this repository and also for the interested reader, its theoretical overview is given as an optional section.

## Why SVM?

- Works well in high-dimensional spaces.
- Robust to overfitting, especially with proper kernel selection. This is because SVM problem formulation is based on minimizing the weight norm $\|| \mathbf{w} \||^2$ which inherently applies regularization.
- Interpretable decision boundaries based on support vectors.
- Efficient use of training data – Only a subset of data points (support vectors) determine the model, making it effective even with limited training samples.

## What’s in This Repository?

This repository provides a structured theoretical and practical overview of SVMs, covering:

- Mathematical foundations and optimization concepts.
- Explanation of linear and nonlinear SVMs.
- Exploration of real-world challenges, including handling outliers.
- Implementation of an SVM classifier from scratch.
- A discussion on efficient training techniques like Sequential Minimal Optimization (SMO) and its implementation. 
