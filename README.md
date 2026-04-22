# 🌸 Flower Recognition using SVM & HOG Features

A machine learning project that classifies flower images into five categories using feature engineering (HOG + color histograms) and a Support Vector Machine (SVM) model.

---

## 📌 Project Overview

This project focuses on building an image classification model that can recognize different types of flowers based on visual features.

### 🌼 Classes:
- Daisy
- Dandelion
- Rose
- Sunflower
- Tulip

---

## 🧠 Approach

Instead of using deep learning, this project relies on **classical computer vision + machine learning** techniques:

- Feature Extraction:
  - **HOG (Histogram of Oriented Gradients)** for shape & texture
  - **LAB Color Histograms** for color representation
- Model:
  - **Support Vector Machine (SVM)** with RBF kernel

---

## 📊 Dataset

- Source: Google Drive dataset (`/datasets/flowers`)
- Total samples used: **1500 images**
- **300 images per class**
- Train/Test Split: **80% / 20%**

---

## 🔍 Feature Engineering

Each image is processed as follows:

1. Resize image to **128x128**
2. Convert to:
   - Grayscale → for HOG
   - LAB color space → for color features
3. Extract:
   - HOG features (texture & edges)
   - Histogram features (L, A, B channels)
4. Combine into a single feature vector

---

## 🤖 Model Training

- Algorithm: **Support Vector Machine (SVM)**
- Kernel: `RBF`
- Parameters:
  - `C = 10`
  - `gamma = 'scale'`
  - `class_weight = 'balanced'`

---

## 📈 Results

- ✅ **Accuracy:** ~49%

### 📊 Classification Report:
- Balanced performance across classes
- Best performing:
  - **Tulip (Recall: 0.62)**
  - **Sunflower (F1: 0.54)**
- Lower performance on:
  - Daisy & Rose

---

## 📉 Evaluation Methods

- Accuracy Score
- Classification Report (Precision, Recall, F1-score)
- Confusion Matrix Visualization

---

## 🖼️ Visualizations

- Confusion Matrix (with exact values)
- Sample predictions:
  - 15 test images
  - Displaying **True vs Predicted labels**

---

## 🛠️ Technologies Used

- Python 🐍  
- OpenCV  
- NumPy  
- Matplotlib  
- Scikit-learn  
- scikit-image (HOG)  

---

## 📂 Project Structure

```
Flower-Recognition/
│
├── Flowers_Recognition.ipynb
├── LICENSE
└── README.md
```

---

## ▶️ How to Run

1. Mount Google Drive:
```python
from google.colab import drive
drive.mount('/content/drive')
```

2. Set dataset path:
```python
image_dir = Path('/content/drive/MyDrive/datasets/flowers')
```

3. Run the notebook cells step-by-step.

---

## ⚠️ Limitations

- Accuracy is relatively low (~49%)
- Classical ML struggles with complex image variations
- Limited dataset size

---

## 🚀 Future Improvements

- Use **Deep Learning (CNNs)** for higher accuracy  
- Apply **data augmentation**  
- Increase dataset size  
- Try advanced models (Random Forest, XGBoost)  
- Optimize hyperparameters further 
