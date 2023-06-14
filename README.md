# Siamese Network for Signature Classification
This repository contains an adapted implementation of a Siamese Network for one-shot learning, specifically designed for the classification of signatures using two input images. The model is built using two pre-trained MobileNet models with shared weights.

## Background
The Siamese Network architecture is a popular choice for one-shot learning tasks, where the objective is to classify objects based on a limited number of examples. In this case, the goal is to determine whether a given signature is real or fake by comparing two signature images.

## Model Architecture
The Siamese Network consists of two branches, each utilizing a pre-trained MobileNet model. The weights of the MobileNet models are shared to encourage the learning of common features between the two input images. By calculating the Euclidean distance between the outputs of the two branches, a similarity score is obtained, which indicates the similarity between the two signatures.

## Training
To train the Siamese Network, a triplet loss function is used. This loss function takes into account three images: an anchor image (a genuine signature), a positive image (another genuine signature), and a negative image (a fake signature). The model aims to minimize the distance between the anchor and positive images, while maximizing the distance between the anchor and negative images. This way, the network learns to discriminate between real and fake signatures.

During training, the weights of the MobileNet models are updated using backpropagation and gradient descent, optimizing the triplet loss. The training process involves iteratively feeding triplets of images to the network and adjusting the weights based on the loss function.

## Usage
To use the trained Siamese Network for signature classification, you can provide pairs of signature images as input. The model will calculate the Euclidean distance between the outputs of the two branches and produce a similarity score. Based on a predefined threshold, you can determine whether the signature is classified as real or fake.

Please refer to the documentation and code provided in this repository for detailed instructions on setting up the environment, training the model, and using it for signature classification.

## Acknowledgments
This project is based on the Siamese Network architecture and utilizes pre-trained MobileNet models. The implementation builds upon existing research and open-source contributions in the field of one-shot learning and deep neural networks.

