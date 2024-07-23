# CNN Classifier for Human, Cat, and Dog Images

## Overview
### This project implements a Convolutional Neural Network (CNN) classifier to distinguish between images of humans, cats, and dogs. The model is trained on a dataset of labeled images and is capable of predicting the class of new, unseen images with 95.66 Accuracy.

## Dataset
### The dataset used for training and testing the model contains images of three classes:
* Humans
* cats
* dogs
### Each class have 1536 images of each class in training dataset and 384 images of each classes in testing dataset.

## Requirements
* Python 12.+
* PyTorch
* NumPy
* Matplotlib

## Model Architecture
### The CNN architecture consists of the following layers:
==========================================================================================
Layer (type:depth-idx)                   Output Shape              Param #
==========================================================================================
Sequential                               [1, 3]                    --
├─Conv2d: 1-1                            [1, 32, 256, 256]         896
├─Conv2d: 1-2                            [1, 64, 256, 256]         18,496
├─ReLU: 1-3                              [1, 64, 256, 256]         --
├─MaxPool2d: 1-4                         [1, 64, 86, 86]           --
├─Conv2d: 1-5                            [1, 64, 86, 86]           36,928
├─Conv2d: 1-6                            [1, 64, 86, 86]           36,928
├─ReLU: 1-7                              [1, 64, 86, 86]           --
├─MaxPool2d: 1-8                         [1, 64, 29, 29]           --
├─Conv2d: 1-9                            [1, 64, 29, 29]           36,928
├─Conv2d: 1-10                           [1, 128, 29, 29]          73,856
├─ReLU: 1-11                             [1, 128, 29, 29]          --
├─MaxPool2d: 1-12                        [1, 128, 10, 10]          --
├─Flatten: 1-13                          [1, 12800]                --
├─Linear: 1-14                           [1, 128]                  1,638,528
├─Linear: 1-15                           [1, 64]                   8,256
├─ReLU: 1-16                             [1, 64]                   --
├─Linear: 1-17                           [1, 3]                    195
==========================================================================================
Total params: 1,851,011
Trainable params: 1,851,011
Non-trainable params: 0
Total mult-adds (Units.GIGABYTES): 1.91
==========================================================================================
Input size (MB): 0.79
Forward/backward pass size (MB): 59.20
Params size (MB): 7.40
Estimated Total Size (MB): 67.39
==========================================================================================


## Thanks For reading This
