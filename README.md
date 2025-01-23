Deep Learning Project for UNIBO

Separation of CIFAR-10 Images\
The model takes as input an image created by averaging two random samples from CIFAR-10 and is tasked with predicting the categories of the two components.\

The first image belongs to the first five categories (airplane, automobile, bird, cat, deer), while the second belongs to the remaining categories (dog, frog, horse, ship, truck).\
The model returns two labels, each within a range of five possible values.\

The evaluation metric for the model is as follows: \
calculate the classification accuracy for the two component images and then compute their average.\

The metric is evaluated on 10,000 inputs generated from test data. The calculation is repeated 10 times, standard deviation is also measured.
