# Bird_Identification
CSE455 Final Project

## Introduction
This is a repository for my bird classification model that I used to compete in the in-class Kaggle competition.

The task involved training a machine learning model that takes images as inputs and predicts the species of birds present in the images.

## Dataset
The dataset provided for the competition consists of 555 classes of bird species, and it includes around 38000 images with labels for training and 10000 unlabeled images for evaluation.

## Usage
The bird_classification.ipynb should be pretty self-explanatory in data loading, training, predicting, etc.

## Model Architecture
My approach was to use an ensemble method with two pretrained SOTA models and finetune it to the task. Particularly, I decided on EfficientNet-b4 and DenseNet169 as my models since they can achieve nearly SOTA performance on image classification tasks with significantly less number of parameters. DenseNet could be loaded directly through pytorch, but EfficientNet had to be imported from an external library. Due to the limitation of GPU memory on Kaggle, these models were picked instead of their deeper counterparts.

## Results
The ensemble method with alpha=0.45 achieved a final test accuracy of 84.912%.
