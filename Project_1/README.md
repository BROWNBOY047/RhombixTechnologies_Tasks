# MobileNetV2 Image Classifier

This project implements an image classification model using **MobileNetV2** to identify three categories: `vehicle`, `animal`, and `solid object`. The model is trained on a custom image dataset using **TensorFlow** and is capable of classifying user-uploaded images with high accuracy.

# 📁 Project Overview

- **Model**: Transfer Learning with MobileNetV2 (pre-trained on ImageNet)
- **Input Image Size**: 160x160 pixels
- **Output Classes**: 3 — Vehicle, Animal, Solid Object
- **Platform**: Google Colab (with GPU/TPU support)
- **Format Saved**: `.keras` (recommended Keras format)

---

# 🛠️ Technologies & Libraries Used

| Library         | Purpose                                       |
|----------------|-----------------------------------------------|
| TensorFlow      | Deep Learning framework for model training   |
| Keras           | High-level API for TensorFlow modeling       |
| NumPy           | Numerical operations and array handling      |
| Matplotlib      | Visualizing predictions and images           |
| Google Colab    | Cloud-based training with GPU/TPU support    |

---

# 📦 Features

- Preprocessing with `ImageDataGenerator`
- Transfer learning using MobileNetV2 base
- Training with TPU acceleration
- Prediction on user-uploaded images
- Model export in `.keras` and `.zip` formats

---

# 🧪 How to Test the Model

1. **Upload the trained model file**:
    - `mobilenetv2_classifier.keras`
2. **Upload a test image**:
    - Accepted formats: `.jpg`, `.png`, etc.
3. **Run prediction script**:
      python
    from google.colab import files
    uploaded = files.upload()
    # Load image and predict...
    

---

# 📁 Model File

- **mobilenetv2_classifier.keras**: Trained model file.
- You can share it as a `.zip` file via Google Drive, email, or WhatsApp.



# 📌 Scope of the Project

This model is designed to classify real-world images into the defined classes. It can be extended for:
- Safety monitoring (e.g., detecting vehicles or obstacles)
- Object identification in autonomous systems
- Real-time image classification on edge devices (with optimization)

---

## 🚀 Getting Started (Google Colab)

1. Upload dataset and preprocess
2. Train model using TPU
3. Save using:
   ```python
   model.save("mobilenetv2_classifier.keras")

