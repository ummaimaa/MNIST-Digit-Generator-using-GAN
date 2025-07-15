# MNIST-Digit-Generator-using-GAN# MNIST Digit Generator using GAN

This repository contains the implementation of a **Generative Adversarial Network (GAN)** using **PyTorch** to generate synthetic handwritten digits based on the **MNIST dataset**.

##  Objective

To implement and train a basic GAN that can generate realistic-looking handwritten digit images by learning the distribution of the MNIST dataset.

---

##  Dataset

- **Name:** MNIST (Modified National Institute of Standards and Technology)
- **Source:** [TensorFlow Datasets - MNIST](https://www.tensorflow.org/datasets/catalog/mnist)
- **Details:** 70,000 grayscale images (28x28 pixels) of digits (0–9)
- **Subset Used:** 10,000 training images (to reduce training time)

---

##  GAN Architecture

### 🔹 Generator
- **Input:** 100-dim random noise vector
- **Layers:**
  - Linear → ReLU
  - Linear → ReLU
  - Linear → Tanh (Output reshaped to 28×28)

### 🔹 Discriminator
- **Input:** Flattened 28×28 image (784-dim)
- **Layers:**
  - Linear → LeakyReLU
  - Linear → LeakyReLU
  - Linear → Sigmoid (Output: 0 or 1)

---

##  Training Details

- **Framework:** PyTorch
- **Loss Function:** Binary Cross-Entropy Loss (BCELoss)
- **Optimizer:** Adam (Learning Rate = 0.0002)
- **Epochs:** 20
- **Batch Size:** 64
- **Device:** GPU 

---
