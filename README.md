# Predicting Categories of Averaged CIFAR-10 Images

This repository contains the implementation of a model designed to predict the categories of two component images created by averaging random samples from the CIFAR-10 dataset. The project includes data generation, model training, and evaluation based on a specific metric.

## Problem Description

### Input
- Each input is an image obtained by averaging two random samples from CIFAR-10.
- The first image belongs to one of the first five CIFAR-10 categories:
  - Airplane
  - Automobile
  - Bird
  - Cat
  - Deer
- The second image belongs to one of the remaining five categories:
  - Dog
  - Frog
  - Horse
  - Ship
  - Truck

### Output
- The model outputs two labels:
  1. A label <5 for the first image category.
  2. A label >=5 for the second image category.

### Evaluation Metric
1. Calculate the classification accuracy for the two predicted labels.
2. Compute the average accuracy across the two predictions.
3. Evaluate the metric on **10,000 inputs** generated from the CIFAR-10 test dataset.
4. Repeat the evaluation **10 times** and report the **standard deviation** of the results.

## Dataset
- CIFAR-10: A dataset consisting of 60,000 images (50,000 for training, 10,000 for testing) across 10 classes.
- Classes:
  1. Airplane
  2. Automobile
  3. Bird
  4. Cat
  5. Deer
  6. Dog
  7. Frog
  8. Horse
  9. Ship
 10. Truck

## Implementation

### Data Generator
A data generator is provided to create inputs by averaging two random CIFAR-10 images:
- The first image is sampled from the first five classes.
- The second image is sampled from the remaining five classes.
- The generated dataset is split into training and evaluation sets.


### Training
- Train the model using the CIFAR-10 training data.
- Loss function: Multi-task classification loss 
- Optimizer: Adam 
- Monitor classification accuracy for both labels during training.

### Evaluation
1. Generate 10,000 test inputs using the provided data generator.
2. Evaluate the model’s accuracy on the test set.
3. Repeat the evaluation 10 times.
4. Report the average accuracy and standard deviation.


### Results
The evaluation results, include average accuracy of 79.81% and standard deviation of 0.28%

