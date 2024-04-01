# Leaf-classification Project 🌿

🧑‍🤝‍🧑Thanks to [Andrea Bertogalli](https://github.com/andberto) and [Niccolò Balestrieri](https://github.com/NiccoloBalestrieri)


This repository contains the work for the ANN&DL project by the ANN Group for the Artificial Neural Network and Deep Learning course, focusing on the classification of leaves as healthy or unhealthy using deep learning techniques. 🍃

## Dataset Inspection 📊

The project dataset comprises 5,200 RGB images of leaves, each with a resolution of 96x96 pixels. The images are labeled as either healthy or unhealthy, making it a binary classification task. The dataset features a class imbalance, with 3,199 (61.52%) healthy leaves and 2,001 (38.48%) unhealthy leaves.

## Preprocessing 🛠️

### Dealing with Outliers and Duplicates

Initial data inspection involved identifying outliers and duplicates. After cleansing, the dataset consisted of 4,850 samples, including 3,060 healthy and 1,790 unhealthy leaves.



![Screenshot 2024-04-01 at 23-45-26 reportv1 0 pdf](https://github.com/tombinic/Leaf-classification/assets/91635053/2fdf1507-a8bc-427e-8d14-eb2979e50e19)

![Screenshot 2024-04-01 at 23-45-51 reportv1 0 pdf](https://github.com/tombinic/Leaf-classification/assets/91635053/83efeb41-b0b5-4b0c-87ba-9dc52c5cef6b)

### Addressing Data Imbalance

Various strategies were considered to tackle the inherent data imbalance, including data augmentation and adjusting class weights in the loss function. The final approach involved maintaining sample-level imbalance but adjusting class weights to improve model sensitivity towards diseased leaves classification.

## Model Selection and Tuning 🔍

### Feature Extraction Model (FEM) Selection

After evaluating several pretrained models for feature extraction, ConvNeXtXLarge was selected for its superior performance.


![Screenshot 2024-04-01 at 23-46-26 reportv1 0 pdf](https://github.com/tombinic/Leaf-classification/assets/91635053/1116e7c1-9612-49d2-9757-8d76e68582ef)

### Hyperparameter Tuning and Architecture

Hyperparameter tuning focused on the fully connected neural network (FFNN) layers added to ConvNeXtXLarge, using grid search to optimize the number of layers, neurons, and other parameters like learning rate and batch size.

![Screenshot 2024-04-01 at 23-51-09 reportv1 0 pdf](https://github.com/tombinic/Leaf-classification/assets/91635053/f4e3284c-106d-4b4b-8822-7f17d9d3ce0c)


## Data Augmentation 🔄

To combat overfitting, data augmentation techniques such as random flips, rotations, and translations were applied, enhancing model robustness and performance.

![Screenshot 2024-04-01 at 23-52-20 reportv1 0 pdf](https://github.com/tombinic/Leaf-classification/assets/91635053/256aff0e-70c8-45a4-8b31-0b09bf65ff35)


## Fine-Tuning 🎛️

The model underwent fine-tuning with partial unfreezing of the backbone and adjustments in learning rate and data augmentation parameters to further enhance performance and generalization.

## Results 📈

The final model, with a ConvNeXtXL backbone and a FFNN with two hidden layers, achieved the following performance metrics on the hidden test set:


![Screenshot 2024-04-01 at 23-52-46 reportv1 0 pdf](https://github.com/tombinic/Leaf-classification/assets/91635053/3bdb8d63-08ea-4e5f-9b91-64b65215b470)

You can find all the details in the colab notebook and in the report.
Clearly, there could be some errors due to missing file or path.
