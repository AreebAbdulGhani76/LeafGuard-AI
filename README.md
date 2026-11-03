# 🌿 LeafGuard AI – Plant Disease Classification

**LeafGuard AI** is a Computer Vision and Deep Learning project that focuses on classifying plant diseases using leaf images. It explores traditional neural networks, Convolutional Neural Networks (CNNs), and transfer learning with MobileNetV2 to recognize different plant disease categories.

The project uses image preprocessing and edge-based feature extraction techniques to investigate how visual features can support automated plant disease classification.

## ✨ Project Features

### 1. 📊 Dataset Collection
- Uses the Kaggle PlantVillage dataset.
- Loads plant leaf images from class-based directories.
- Extracts image labels from folder names.

### 2. 🖼️ Image Preprocessing
- Resizes images to 128 × 128 pixels.
- Converts images into grayscale.
- Normalizes processed image values.
- Prepares images for deep learning models.

### 3. 🔬 Image Feature Extraction
Applies three image-processing techniques:

- **Sobel X:** Detects horizontal intensity gradients.
- **Sobel Y:** Detects vertical intensity gradients.
- **Laplacian Filter:** Highlights rapid intensity changes and image edges.

Combines the original grayscale image and extracted edge information into a three-channel feature representation.

### 4. 🧠 Deep Learning Models

Three approaches are explored:

**A. Baseline Neural Network**
- Fully Connected Neural Network.
- Dense layers with ReLU activation.
- Dropout for regularization.
- Softmax output for multiclass classification.

**B. Custom CNN**
- Convolutional layers.
- Batch Normalization.
- Max Pooling.
- Dropout.
- Dense classification layers.

**C. MobileNetV2 – Transfer Learning**
- Uses ImageNet pretrained weights.
- Global Average Pooling.
- Custom classification head.
- Fine-tuning of the last 20 backbone layers.
- Adam optimizer with learning-rate adjustment.

## 🛠️ Technologies & Libraries

| Technology | Purpose |
|---|---|
| Python | Core programming |
| TensorFlow / Keras | Deep learning and model training |
| OpenCV | Image preprocessing and filtering |
| NumPy | Numerical operations |
| Matplotlib | Visualization |
| Scikit-learn | Dataset splitting and label encoding |
| KaggleHub | Dataset downloading |
| MobileNetV2 | Transfer learning |

## 📂 Project Structure

```text
LeafGuard-AI/
│
├── OEL1_of_CV.ipynb
│
└── README.md
```

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
```

### 2. Navigate to the Project

```bash
cd LeafGuard-AI
```

### 3. Install Dependencies

```bash
pip install tensorflow opencv-python numpy matplotlib scikit-learn kagglehub
```

### 4. Run the Notebook

Open the notebook using Jupyter:

```bash
jupyter notebook OEL1_of_CV.ipynb
```

Alternatively, upload it to Google Colab and execute the cells.

**Note:** KaggleHub may require appropriate Kaggle access and dataset availability.

## 🔄 Project Workflow

```text
PlantVillage Dataset
        |
        v
Image Loading
        |
        v
Image Resizing (128x128)
        |
        v
Grayscale Conversion
        |
        v
Sobel X + Sobel Y + Laplacian
        |
        v
Feature Combination & Normalization
        |
        v
Train-Test Split
        |
        v
Model Training
        |
        +-------------------+
        |         |         |
        v         v         v
     Baseline   Custom   MobileNetV2
       ANN       CNN     Transfer Learning
        |         |         |
        +---------+---------+
                  |
                  v
          Model Evaluation
```

## 🎯 Project Objectives

- Explore computer vision techniques for plant disease classification.
- Understand image preprocessing and edge detection.
- Compare traditional neural networks with CNN architectures.
- Implement transfer learning using MobileNetV2.
- Understand model fine-tuning and learning-rate optimization.
- Apply deep learning to an agricultural problem.

## 🚀 Future Improvements

- Develop a user-friendly web application for leaf image classification.
- Add real-time image prediction.
- Implement confusion matrix and classification reports.
- Compare model performance using accuracy, precision, recall, and F1-score.
- Improve image preprocessing for transfer learning.
- Deploy the trained model for practical demonstrations.

## 👨‍💻 Author

**Areeb Abdul Ghani**

AI Student | Computer Vision | Deep Learning | Machine Learning

- GitHub: [@AreebAbdulGhani76](https://github.com/AreebAbdulGhani76)

---

⭐ If you find this project interesting, consider giving it a star!
