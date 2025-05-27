# Face Detection using Triplet Loss and ResNet50

This project implements a face Detection system using **Triplet Loss** for training, with **ResNet50** as the backbone feature extractor. The goal is to learn an embedding space where faces of the same person are close together, and faces of different people are far apart.

>  **Note**:  
> The model structure is based on an exercise provided by the course instructor for Detection **colored images of celebrities**, which has been **adapted here for grayscale face image recognition** using the AT&T dataset.

---

##  Description

We use triplets of images:
- **Anchor (A)**: Image of a person  
- **Positive (P)**: Another image of the same person  
- **Negative (N)**: Image of a different person

The loss function ensures that the distance between A and P is smaller than between A and N by a margin (α):

\[
\|f(A) - f(P)\|^2 + α < \|f(A) - f(N)\|^2
\]

---

##  Model

- **Backbone**: ResNet50 (pre-trained on ImageNet)
- **Embedding Layer**: Dense layer added after ResNet50 output
- **Loss Function**: Triplet Loss
- **Dataset**: [AT&T Face Dataset (ORL)](https://www.kaggle.com/datasets/kasikrit/att-database-of-faces)

---


