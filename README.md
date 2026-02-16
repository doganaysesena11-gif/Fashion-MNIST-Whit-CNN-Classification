## Fashion MNIST Classification with CNN

This project demonstrates how to build a Convolutional Neural Network (CNN) to classify images from the Fashion MNIST dataset using TensorFlow and Keras. The dataset contains 70,000 grayscale images of 10 clothing categories, each of size 28x28 pixels.

## Dataset

Source: TensorFlow Keras datasets (tf.keras.datasets.fashion_mnist)

Train/Test Split: 60,000 training images and 10,000 test images

## Classes:

T-shirt/top

Trouser

Pullover

Dress

Coat

Sandal

Shirt

Sneaker

Bag

Ankle boot

Images were normalized by scaling pixel values to the range [0,1].

## Libraries Used
  import tensorflow as tf
  from tensorflow.keras.models import Sequential
  from tensorflow.keras.layers import Conv2D, MaxPooling2D, Flatten, Dense, Dropout
  import matplotlib.pyplot as plt
  from sklearn.metrics import accuracy_score

## Model Architecture

The CNN model consists of the following layers:

Conv2D Layer: 32 filters, 3x3 kernel, ReLU activation, padding='same', input shape (28,28,1)
MaxPooling2D Layer: 2x2 pool size
Conv2D Layer: 64 filters, 3x3 kernel, ReLU activation, padding='same'
MaxPooling2D Layer: 2x2 pool size
Flatten Layer
Dense Layer: 64 units, ReLU activation
Dropout Layer: rate 0.5
Dense Output Layer: 10 units, Softmax activation

## Training
Optimizer: Adam
Loss Function: Sparse Categorical Crossentropy
Metrics: Accuracy
Batch Size: 32
Epochs: 10


The model was trained on the training dataset with validation using the test dataset.

## Results

Training Accuracy: ~91.8%

Test Accuracy: ~91.7%

The model performs well in classifying fashion items, achieving over 91% accuracy on unseen test data.


