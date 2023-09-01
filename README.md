# Persian e-Commerce Sentiment Analysis

## Overview

This repository contains the code and resources to training a ML model to perform sentiment analysis on Persian text. The model is trained on a dataset collected from Digikala.com, an Iranian e-Commerce website. The dataset used in the training process can be found on Kaggle [here](https://www.kaggle.com/datasets/soheiltehranipour/digikala-comments-persian-sentiment-analysis).

The data preprocessing stage included the following steps to prepare the text data for training:

- Converting Persian numerals to Arabic numerals to ensure uniform representation of numbers.
- Identical character conversion (e.g., 'ك' to 'ک') to increase the consistency of text processing.
- Replacing URLs and Emojis with `<URL>` and `<emoji>` to remove noise.
- Removing repeated letters that are used for emphasis.

## Model

The model was trained using keras and utilizing a feedforward neural network with multiple dense layers. Dropout layers with a dropout rate of 0.5 were added to reduce overfitting. The model is compiled with the categorical cross-entropy loss function and the `Adam` optimizer. You can change the parameters based on your specific requirements and dataset to optimize the model for your use case.
### Parameters

```python
# Model parameters
nb_classes = 2
batch_size = 32
nb_epochs = 10
```
