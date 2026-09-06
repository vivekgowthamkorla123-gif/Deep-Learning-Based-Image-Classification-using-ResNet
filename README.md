# Handwritten Digit Recognition using CNN

This project implements a **Convolutional Neural Network (CNN)** using **PyTorch** for handwritten digit classification. The model is first trained on the **MNIST dataset** and then adapted to recognize **Telugu handwritten numbers** through transfer learning and fine-tuning.

## Overview

The experiment demonstrates the complete workflow of training an image classification model, including:

* Loading and preprocessing the MNIST dataset
* Training a CNN for handwritten digit classification
* Using GPU acceleration for model training
* Applying image transformations and data augmentation
* Training the model on a custom Telugu handwritten number dataset
* Saving model checkpoints and the best-performing model
* Fine-tuning the classifier while freezing the convolutional layers
* Evaluating model performance on test data

## Dataset

### MNIST

The MNIST dataset is used as the initial training dataset. It consists of grayscale images of handwritten digits from **0 to 9**. Images are converted to tensors and normalized before being passed to the network.

### Telugu Handwritten Numbers

A custom dataset containing handwritten Telugu numbers is used for the second stage of the experiment. The dataset is organized into training and testing directories, with separate subdirectories representing different classes.

Images are resized to **28 × 28 pixels**, converted to grayscale, normalized, and augmented using random cropping.

## Model

A CNN is used for image classification with:

* 1 input channel for grayscale images
* 10 output classes
* Convolutional feature extraction layers
* A classifier/MLP layer for final classification

The model is trained using **Cross-Entropy Loss** and the **SGD optimizer with momentum**.

## Training

The model is trained using GPU acceleration when available. The training process includes:

1. Forward propagation
2. Calculation of classification loss
3. Backpropagation
4. Parameter updates using SGD
5. Validation on the test dataset
6. Saving the best-performing model and checkpoints

The initial training on the custom Telugu number dataset achieved approximately **63% test accuracy after 10 epochs**.

## Transfer Learning & Fine-Tuning

The best trained model is loaded and used for fine-tuning. During fine-tuning:

* The convolutional layers are frozen.
* Only the classifier layers are updated.
* The model is trained further on the Telugu handwritten number dataset.

The fine-tuning stage achieved a best recorded accuracy of approximately **67.6%** on the test set.

## Technologies Used

* **Python**
* **PyTorch**
* **Torchvision**
* **NumPy**
* **Matplotlib**
* **Google Colab**
* **CUDA/GPU acceleration**


## Key Concepts

**Convolutional Neural Networks • Image Classification • MNIST • Transfer Learning • Fine-Tuning • Data Augmentation • GPU Training • Model Checkpointing**

## Conclusion

This experiment demonstrates how a CNN trained for handwritten digit recognition can be adapted to a different handwritten numeral dataset using **transfer learning and classifier fine-tuning**. It provides practical experience with deep-learning model training, evaluation, preprocessing, augmentation, and model checkpoint management.
