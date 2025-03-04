# Variational Autoencoder (VAE) for Shoe Image Generation

## Overview
This repository contains an implementation of a Variational Autoencoder (VAE) designed to generate and reconstruct shoe images. The model is trained using deep learning techniques to learn a latent representation of the data, enabling it to generate new realistic images.

## Dataset
The dataset consists of shoe images. The images are preprocessed before being fed into the VAE model. Preprocessing includes resizing, normalization, and reshaping.

## Preprocessing
- Images are loaded using OpenCV (`cv2`).
- Resized to a fixed dimension suitable for the model.
- Normalized to a range of [0,1] for stable training.
- Converted into tensors for processing in deep learning models.

## Model Architecture
The Variational Autoencoder (VAE) consists of:
- **Encoder**: Compresses the input images into a latent vector (mean and variance).
- **Latent Space Sampling**: Samples a latent representation using the reparameterization trick.
- **Decoder**: Reconstructs the image from the latent space.

The model is implemented using `PyTorch`.

## Training
- The model is trained using the **Reconstruction Loss** (Mean Squared Error) and **Kullback-Leibler (KL) Divergence** to regularize the latent space.
- Uses the **Adam optimizer** for efficient training.
- Trained for a fixed number of epochs while monitoring loss trends.

## Evaluation
- The trained model is evaluated by reconstructing test images and visually inspecting their quality.
- The loss function values are plotted to assess convergence.

## Results
- The model successfully learns a meaningful latent representation of shoe images.
- Generated images show realistic features with variations.
- Evaluation metrics demonstrate the effectiveness of the model in reconstructing images.
