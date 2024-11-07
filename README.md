# GAN for MNIST Digit Generation and Evaluation

## Project Overview

This project involves designing a GAN to generate digit images from the MNIST dataset. The Generator (G) creates fake digits, and the Discriminator (D) distinguishes between real and fake images. A classifier was trained to evaluate both real and fake datasets, and classification errors were reported.

## Deliverables

1. **G.pkl** - Generator model
2. **D.pkl** - Discriminator model
3. **C.pkl** - Classifier model
4. **Fake_Digits/** - Folder with 100 generated fake images and corresponding latent samples `Z`
5. **S0 (MNIST test set images)** - 100 random MNIST test images
6. Python Script

## Code Overview

### GAN Model
- **Generator (G):** Generates images from random latent vectors.
- **Discriminator (D):** Distinguishes between real and fake images.
- **Optimization:** Adam optimizer with Binary Cross Entropy loss.

### Classifier Model
- A simple CNN trained on MNIST, tested on both real (`S0`) and fake (`S1`) datasets.

### Fake Dataset
- 100 fake images generated using latent vectors from the Generator, with well-formed digits included.

### Evaluation
- Classifier evaluated on real (`S0`) and fake (`S1`) datasets. Errors were recorded for both.

## Observations

- The classification error for the fake dataset (`S1`) was higher than for the real dataset (`S0`).
- Generated digits improved over training but still had artifacts.

