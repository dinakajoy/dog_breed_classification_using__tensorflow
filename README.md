# 🐶 Dog Breed Classification using TensorFlow

This project is an end-to-end deep learning pipeline that classifies **dog breeds from images** using **TensorFlow** and **transfer learning**. It was developed in Google Colab and leverages the **Kaggle Dog Breed Identification dataset** with 120 unique dog breeds.

> Imagine sitting in a café, snapping a photo of a dog, and instantly knowing its breed

## 📌 Project Highlights

- **Dataset**: [Kaggle Dog Breed Identification](https://www.kaggle.com/c/dog-breed-identification/data)
- **Modeling Approach**: Transfer learning using EfficientNet
- **Tools**: TensorFlow, TensorFlow Hub, Google Colab
- **Output**: Top-1 breed prediction with confidence score
- **Deployment-ready**: Can be extended to web or mobile apps

## 🧠 Problem Statement

Given an image of a dog, predict its breed from a list of 120 possible categories.  
This is a **multi-class image classification** problem using supervised learning.

---

## 🗂️ Dataset Overview

- **Train set**: ~10,000 labeled dog images  
- **Test set**: ~10,000 unlabeled images  
- **Labels**: 120 distinct dog breeds  
- Each label maps to an image ID (not file name)

## 🚀 Project Workflow

### 1. Data Setup
- Downloaded the dataset using Kaggle API.
- Extracted and loaded training images and labels.

### 2. Preprocessing
- Resized all images to a uniform size.
- Normalized pixel values to improve training.
- Encoded labels using one-hot encoding.
- Created training and validation splits.
- Used `tf.data` pipelines for efficient loading.

### 3. Model Building
- Utilized **EfficientNetB0** from TensorFlow Hub.
- Frozen base layers; added custom classification head.
- Used dropout for regularization.
- Compiled with categorical crossentropy and Adam optimizer.

### 4. Model Training
- Trained using 10+ epochs (adjustable).
- Tracked training and validation accuracy/loss.
- Added callbacks for:
  - Early stopping
  - Model checkpointing
  - TensorBoard logging

### 5. Evaluation
- Visualized training curves.
- Validated predictions with real dog images.
- Displayed predictions with confidence scores.

---

## 📊 Example Output

```text
Input: 🖼️ uploaded_dog.jpg  
Prediction: 🐕 Golden Retriever  
Confidence: 97.2%
```

## 🧰 Tech Stack
| Tool / Library      | Purpose                            |
| ------------------- | ---------------------------------- |
| TensorFlow          | Model building & training          |
| TensorFlow Hub      | Pretrained model access            |
| TensorFlow Datasets | tf.data pipeline support           |
| Matplotlib          | Visualization                      |
| Google Colab        | Development & training environment |
| Kaggle API          | Dataset access                     |



