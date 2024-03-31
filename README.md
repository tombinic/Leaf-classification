# ANN&DL Project Report 🌿

This repository contains the work for the ANN&DL project by the ANN Group, focusing on the classification of leaves as healthy or unhealthy using deep learning techniques. 🍃

## Dataset Inspection 📊

The project dataset comprises 5,200 RGB images of leaves, each with a resolution of 96x96 pixels. The images are labeled as either healthy or unhealthy, making it a binary classification task. The dataset features a class imbalance, with 3,199 (61.52%) healthy leaves and 2,001 (38.48%) unhealthy leaves.

## Preprocessing 🛠️

### Dealing with Outliers and Duplicates

Initial data inspection involved identifying outliers and duplicates. After cleansing, the dataset consisted of 4,850 samples, including 3,060 healthy and 1,790 unhealthy leaves.

### Addressing Data Imbalance

Various strategies were considered to tackle the inherent data imbalance, including data augmentation and adjusting class weights in the loss function. The final approach involved maintaining sample-level imbalance but adjusting class weights to improve model sensitivity towards diseased leaves classification.

## Model Selection and Tuning 🔍

### Feature Extraction Model (FEM) Selection

After evaluating several pretrained models for feature extraction, ConvNeXtXLarge was selected for its superior performance.

### Hyperparameter Tuning and Architecture

Hyperparameter tuning focused on the fully connected neural network (FFNN) layers added to ConvNeXtXLarge, using grid search to optimize the number of layers, neurons, and other parameters like learning rate and batch size.

## Data Augmentation 🔄

To combat overfitting, data augmentation techniques such as random flips, rotations, and translations were applied, enhancing model robustness and performance.

## Fine-Tuning 🎛️

The model underwent fine-tuning with partial unfreezing of the backbone and adjustments in learning rate and data augmentation parameters to further enhance performance and generalization.

## Results 📈

The final model, with a ConvNeXtXL backbone and a FFNN with two hidden layers, achieved the following performance metrics on the hidden test set:

- Accuracy: 0.892
- Precision: 0.890
- Recall: 0.815
- F1-Score: 0.851

You can find all the details in the colab notebook. Clearly, there could be some errors due to missing file or path.
