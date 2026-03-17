# Digit Recognizer

## 📌 Project Overview
This project implements a Convolutional Neural Network (CNN) to classify and predict handwritten digits (0–9) using the MNIST dataset. The built model is then deployed on an edge device(Android phone) and live testing of hand written digits is implemented.

## Project Link
https://snigdha-c.github.io/CNN-Based-Handwritten-Digit-Recognition-on-Edge-Device/

## Project Flow
Train CNN using TensorFlow on MNIST Dataset
       ↓
Convert model to ONNX
       ↓
Quantize the model
       ↓
Inference using ONNX Runtime on Edge Device

## 📂 Dataset
- **Dataset:** MNIST Handwritten Digits  
- **Training samples:** 60,000  
- **Test samples:** 10,000  
- **Image size:** 28 × 28 pixels (grayscale)  
- **Classes:** 10 (digits 0–9)  

---

## ⚙️ Technologies Used
- Python  
- NumPy  
- Matplotlib  
- TensorFlow / Keras
- ONNX
- Quantization 

---

## Implementation
- Built a Convolutional Neural Network (CNN) using TensorFlow/Keras to classify MNIST digits.
- Converted the trained TensorFlow model to ONNX format for cross-framework compatibility.
- Applied model quantization to reduce model size and improve efficiency for edge deployment.
- Deployed the model on an Android device and performed inference using ONNX Runtime.
- Implemented live handwritten digit testing on the phone.

## 🏗️ Model Architecture
- **Input Layer:** 28 × 28 × 1 neurons 
- **Hidden Layers:**  Conv2D (28 filters, 3×3 kernel) with ReLU activation
                      MaxPooling2D (2×2)
                      Conv2D (28 filters, 3×3 kernel) with ReLU activation
                      MaxPooling2D (2×2)
                      Flatten
                      Dense layer with 64 neurons and ReLU activation
- **Output Layer:** 10 neurons with Softmax activation  
- **Loss Function:** Sparse Categorical Crossentropy  
- **Optimizer:** Adam  

---

## 📊 Model Performance
- **Training Accuracy:** 99.19%  
- **Test Accuracy:** 98.76%
- **Test Accuracy of ONNX Quantized model:** 98.76%
- **Original model size:** 211.3505859375 KB
- **Quantized model size:** 64.8544921875 KB
 

## 📉 Learning Curve — Accuracy vs Epochs
<img width="772" height="566" alt="image" src="https://github.com/user-attachments/assets/636ec9a3-97e6-491c-a0ee-d9d14dfba3f4" />

## 📉 Learning Curve — Loss vs Epochs
<img width="748" height="560" alt="image" src="https://github.com/user-attachments/assets/61dc6e39-7ee7-4ef9-ac80-bdc0cc31f1d3" />

---

## 📈 Key Observations
- CNNs are effective for handwritten digit recognition
- ONNX conversion maintains model consistency, preserves the model structure and predictions.
- The ONNX Runtime allows the model to run inference directly on the Android device without relying on cloud computation or internet             connection.
- Quantization significantly reduces model size
- Real-time handwritten digits can differ from MNIST samples in thickness, alignment, or scale, which can affect prediction quality.

## Conclusion
- **End-to-end ML pipeline from training to deployment**  
  The project demonstrates the complete workflow from model training and optimization to deployment and inference on an edge device.

