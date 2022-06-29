# Airplane Classification

Contributors: [Michael Reigeleman](https://github.com/mtreigelman) and [Brendan Jenkins](https://github.com/BrendanJenkins).

## Introduction

This repository contains python code and instructions on how to train Convultional Neural Networks (CNN) to classify aircraft from a databank of images. 

## Data

The data can be found [here](https://paperswithcode.com/dataset/fgvc-aircraft-1). It contains 10,200 images for 70 different families and 30 different manufacturers. A family of aircraft is the manufacturer and model for the plane (i.e. Boeing 707). The manufacturer is who makes the plane (i.e. Boeing or Airbus). The images are prelabeled in text files that are included in the data. 

## Pre-Processing

Each image contained a 20 pixel high banner that contained copyright information that needed to be removed. The `Cropping_Pre_Processing.ipynb` is used to crop all the photos and save them into its own subdirectory.

## Tasks

We developed models for two classification tasks.

  1. Classifying the Family of aircraft.
  2. Classifying the Manufacturer of the aircraft.

## Models and Performance

### Family Classification Models

For the first task to classify the Family of the aircraft. For our first model we created our own CNN that contained 4 convolutional layers followed by 2 linear layers. This model did not perform as well as we would have liked, only getting the correct family 8% of the time. We expanded our accuracy metric to the top 5 accuracy, where if the correct label was in the top 5 probabilities it is counted as a correct prediciton. The top 5 accuracy for this model was 23%. 

Since this was low, we decided to use the VGG-16 pretrained model. We froze all the weights in the model except for the last linear layer. This resulted in a top 5 accuracy of 40%.

Correctly Classified Planes:

Incorrectly Classified Planes:

### Manufacturer Classification Model

For this task we used a CNN with the same architecture as our first family classification model. With less classes to predict we saw an increase in true accuracy to 50%. For this model we added the hyperparameters of a dynamic learning rate and reshuffled our training and validation data every 3 epochs to improve model generality and performance.

## Conclusion

