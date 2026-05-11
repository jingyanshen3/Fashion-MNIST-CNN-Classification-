## Project Overview

This project focuses on image classification using Convolutional Neural Networks (CNNs) on the Fashion-MNIST dataset. Two approaches were implemented and compared: a custom CNN built from scratch and a transfer learning model using MobileNetV2.

The goal was to evaluate model performance, generalization ability, and interpretability when classifying clothing images.

---

## Dataset

- **Fashion-MNIST dataset**
- 70,000 grayscale images (28×28 pixels)
- 10 clothing categories (e.g., T-shirt, trouser, dress, bag)
- 60,000 training images and 10,000 test images

For transfer learning, images were resized to 128×128 and converted to RGB format.

---

## Models Used

- **Baseline Model:** Custom CNN built from scratch  
- **Transfer Learning Model:** MobileNetV2 (pretrained on ImageNet)

---

## Key Findings

- MobileNetV2 outperformed the baseline CNN in accuracy and training efficiency
- Achieved **89.6% test accuracy**
- Fine-tuning the last layers further improved performance
- Transfer learning showed strong generalization ability even on grayscale-derived RGB images

---

## Model Interpretation

- Grad-CAM was used to visualize model decision-making
- The model focused mainly on overall shape rather than fine details
- Misclassifications mostly occurred among similar upper-body clothing items:
  - Shirt
  - T-shirt/top
  - Pullover
  - Coat

---

## Key Challenges

- Low-resolution (28×28) images limit feature detail
- High similarity between clothing categories causes confusion
- Grayscale images reduce distinguishable texture and edge information

---

## Conclusion

This study demonstrates that transfer learning with MobileNetV2 significantly improves image classification performance compared to a simple CNN. However, dataset limitations such as low resolution and visual similarity between classes still restrict overall accuracy.

The project also highlights the importance of model interpretability using techniques like Grad-CAM to better understand CNN decision-making.
