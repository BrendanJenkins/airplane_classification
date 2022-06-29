# Airplane Classification

Contributors: [Michael Reigeleman](https://github.com/mtreigelman) and [Brendan Jenkins](https://github.com/BrendanJenkins).

## Introduction

This repository contains python code and instructions on how to train Convultional Neural Networks to classify aircraft from a databank of images. 

## Data

The data can be found [here](https://paperswithcode.com/dataset/fgvc-aircraft-1). It contains 10,200 images for 70 different families and 30 different manufacturers. A family of aircraft is the manufacturer and model for the plane (i.e. Boeing 707). The manufacturer is who makes the plane (i.e. Boeing or Airbus). The images are prelabeled in text files that are included in the data. 

## Pre-Processing

All the images had a banner at the bottom that needed to be cropped. So we used `Cropping_Pre_Processing.ipynb`
