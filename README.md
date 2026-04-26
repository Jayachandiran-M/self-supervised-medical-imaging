# 🩺 Self-Supervised Medical Image Classification using SimCLR

---

## 📌 Project Title

**Self-Supervised Learning for Chest X-Ray Image Classification using SimCLR**

---

## 📖 Project Description

This project focuses on applying **Self-Supervised Learning (SSL)** to medical image classification using the **SimCLR framework**. The aim is to learn meaningful visual representations from **unlabeled chest X-ray images** and improve classification performance when labeled data is limited.

The system classifies chest X-ray images into:

* **Normal**
* **Pneumonia**

The project compares three different approaches:

1. Fully Supervised Learning
2. Transfer Learning
3. Self-Supervised Learning (SimCLR + Fine-tuning)

---

## 🩻 Dataset Used

Dataset: Chest X-Ray Images (Pneumonia) dataset

### 📊 Dataset Details

* Categories:

  * Normal
  * Pneumonia
* Image Type: Chest X-ray images (grayscale)

---

## 📁 Dataset Structure

```
data/
│
├── unlabeled/
│   ├── normal/
│   ├── pneumonia/
│
├── labeled/
│   ├── train/
│   │   ├── normal/
│   │   ├── pneumonia/
│   │
│   ├── val/
│       ├── normal/
│       ├── pneumonia/
```

---

## 🎯 Objectives

* To utilize **unlabeled medical images** using self-supervised learning
* To compare performance of:

  * Fully supervised learning
  * Transfer learning
  * Self-supervised learning
* To improve classification accuracy with limited labeled data

---

## 🧩 Modules Implemented

### 1. Data Preprocessing Module

* Image loading using `torchvision.datasets`
* Transformations:

  * Random Resized Crop
  * Horizontal Flip
  * Rotation
  * Color Jitter
  * Resize and Tensor conversion

---

### 2. Self-Supervised Learning Module (SimCLR)

* Encoder: ResNet18 (without classification layer)
* Projection Head:

  * Fully connected layers
* Contrastive learning using augmented image pairs

---

### 3. Fully Supervised Learning Module

* Training ResNet18 from scratch using labeled dataset

---

### 4. Transfer Learning Module

* Pretrained ResNet18 (ImageNet weights)
* Fine-tuned on chest X-ray dataset

---

### 5. Self-Supervised Fine-Tuning Module

* Encoder trained using SimCLR
* Classification layer added and trained

---

### 6. Evaluation Module

Performance metrics used:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC Score

---

## 🛠️ Technologies Used

* Programming Language: Python

* Deep Learning Framework: PyTorch

* Libraries:

  * torchvision
  * scikit-learn
  * tqdm
  * numpy

* Model Architecture:

  * ResNet18

---

## ⚙️ Model Workflow

1. Load unlabeled dataset and apply data augmentation
2. Train SimCLR model using contrastive learning
3. Train:

   * Fully supervised model
   * Transfer learning model
   * Self-supervised fine-tuned model
4. Evaluate all models using performance metrics
5. Compare results

---

## 📊 Output

The system prints results for:

* Fully Supervised Model
* Transfer Learning Model
* Self-Supervised Model

Example Output:

```
Fully Supervised Results: (Accuracy, Precision, Recall, F1, ROC-AUC)
Transfer Learning Results: (Accuracy, Precision, Recall, F1, ROC-AUC)
Self-Supervised Results: (Accuracy, Precision, Recall, F1, ROC-AUC)
```

---

## 📌 Conclusion

This project demonstrates that **self-supervised learning improves feature extraction** by leveraging unlabeled data. It is especially useful in medical imaging, where labeled data is limited and expensive to obtain.

---
