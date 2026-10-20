# Dimensionality Reduction for Breast Imaging

This project explores different ways to reduce the dimensionality of data, using **BreastMNIST**, a MedMNIST dataset of breast ultrasound images, as a case study.

The goal is to understand what different methods preserve or lose, visualize the resulting representations, and explore how dimensionality reduction can support a classification task. The project is still at an early stage: PCA is the first method being explored, and the other methods below are planned directions.

## Current progress

So far, the work is in the [`dim_reduc_PCA.ipynb`](./dim_reduc_PCA.ipynb) notebook. It covers:

- loading the BreastMNIST training, validation, and test splits at a resolution of 224 × 224;
- displaying a few images and their labels;
- flattening the images so PCA can be applied;
- examining explained variance and the number of components needed to retain different proportions of variance;
- preparing the reduced data as PyTorch tensors.

The notebook currently stops at this preparation stage. Training an MLP and comparing it with a CNN are planned, but have not been implemented yet, so there are no classification results to report at this point.

## Methods and directions to explore

- **PCA**: establish a baseline and study how much variance is retained as the number of components changes.
- **Kernel PCA and LDA**: explore alternative approaches to representing the data, including a method that takes class labels into account.
- **t-SNE**: visualize the data in a low-dimensional space.
- **Autoencoders and VAEs**: learn compact representations of the ultrasound images.
- **CNN feature extraction and latent-space visualization**: investigate representations learned by neural networks and visualize them.
- **Classification comparisons**: train an MLP on reduced representations and compare its results with a CNN trained on the original images.

The methods will be compared in terms of their representations, the information they retain, and—where classification is evaluated—their results on the task.
