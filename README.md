# Melanoma-Skin-Cancer-Detection

## Abstract
In the realm of cancer, there exist over 200 distinct variations. Among these, melanoma stands as the most lethal form of skin cancer. The diagnostic journey for melanoma commences with clinical screening, followed by dermoscopic analysis and histopathological examination. Timely identification of melanoma at its early stages significantly increases the chances of successful treatment. Initial diagnosis involves visual inspection of the affected skin area. Dermatologists capture dermoscopic images using high-speed cameras, with an accuracy range of 65-80% in diagnosing melanoma without additional technical support. Through further assessment by specialized cancer treatment experts and examination of these images, the overall prediction accuracy for melanoma diagnosis improves to 75-84%. The project's goal is to construct an automated classification system leveraging image processing techniques to classify skin cancer based on images of skin lesions.

## Problem Statement
 In the skin biopsy, the dermatologist takes some part of the skin lesion and examines it under the microscope. The current process takes almost a week or more, starting from getting a dermatologist appointment to getting a biopsy report.
 The aims to shorten the current gap to just a couple of days by providing the predictive model.
 The approach uses Convolutional Neural Network (CNN) to classify nine types of skin cancer from outlier lesions images. This reduction of a gap has the opportunity to impact millions of people positively.

## Motivation
The overarching goal is to support the efforts to reduce the death caused by skin cancer. The primary motivation that drives the project is to use the advanced image classification technology for the well-being of the people. Computer vision has made good progress in machine learning and deep learning that are scalable across domains.

## Dataset
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images.


To overcome the issue of class imbalance, used a python package  Augmentor (https://augmentor.readthedocs.io/en/master/) to add more samples across all classes so that none of the classes have very few samples.


## CNN Architecture Design
To classify skin cancer from images of skin lesions, I've developed a custom CNN model aiming for enhanced accuracy in the classification task.

- Rescaling Layer: Normalizes input from the [0, 255] range to [0, 1].
- Convolutional Layer: Extracts features by applying convolutions to reduce the image size and consolidate information within a receptive field.
- Pooling Layer: Reduces feature map dimensions, decreasing parameters and computational load in the network.
- Dropout Layer: Mitigates overfitting by randomly nullifying input units during training.
- Flatten Layer: Converts data into a 1-dimensional array, preparing it for input into subsequent layers.
- Dense Layer: A deeply connected neural network layer where each neuron receives input from all neurons in the previous layer.
- Activation Function (ReLU): Outputs input directly if positive, effectively tackling the vanishing gradient issue, facilitating faster learning and improved performance.
- Activation Function (Softmax): Used in the output layer for multinomial probability distribution predictions, ensuring outputs range from 0 to 1 with their sum equating to one.


## References
Melanoma Skin Cancer from https://www.cancer.org/cancer/melanoma-skin-cancer/about/what-is-melanoma.html

Introduction to CNN from https://www.analyticsvidhya.com/blog/2021/05/convolutional-neural-networks-cnn/

Image classification using CNN from https://www.analyticsvidhya.com/blog/2020/02/learn-image-classification-cnn-convolutional-neural-networks-3-datasets/

Efficient way to build CNN architecture from https://towardsdatascience.com/a-guide-to-an-efficient-way-to-build-neural-network-architectures-part-ii-hyper-parameter-42efca01e5d7
