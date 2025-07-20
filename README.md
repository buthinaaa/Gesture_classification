# ✋ Hand Gesture Classification with Deep Learning

This project aims to classify 10 different hand gestures using deep learning models. We evaluate and compare the performance of three popular CNN architectures — **ResNet-34**, **DenseNet**, and **Xception** — on the LeapGestRecog dataset.

---

## 📂 Project Structure

- `Gesture_Classification.ipynb`: Main training and evaluation notebook.
- `Gesture_project_Documentation.pdf`: Detailed project report, including dataset description, model architectures, training process, and results.

---

## 📊 Dataset

- **Source**: [LeapGestRecog (Kaggle)](https://www.kaggle.com/datasets/gti-upm/leapgestrecog/data)
- **Description**:
  - 10 classes (hand gestures) × 10 individuals × 200 images each = **20,000 images**
  - All images are grayscale, size `(240, 640)`, resized to `(224, 224)`
  - Classes: `Palm`, `I`, `Fist`, `Fist Moved`, `Thumb`, `Index`, `Ok`, `Palm Moved`, `C`, `Down`
  - **Splits**:
    - Train: 70%
    - Validation: 15%
    - Test: 15%

---

## 🧪 Preprocessing

- Images resized to `(224, 224)`
- Normalization tailored to each model
- Data augmentation (rotation, zoom, shear, flip) applied on training data

---

## 🧠 Models Used

| Model      | Key Feature                          | Performance Summary                       |
|------------|--------------------------------------|--------------------------------------------|
| **ResNet-34** | Residual connections (deep network)  | Train: 98% / Val: 55–60% / Test: 10% (overfit) |
| **DenseNet** | Densely connected blocks             | Train: 97% / Val: ~88% / Test: 88%          |
| **Xception** | Depthwise separable convolutions     | Train: 69% / Val: 83.5% / Test: 79% ✅ Best |

> 🔍 **Conclusion**: Xception generalizes best for this dataset. ResNet overfits severely despite high train accuracy.

---

## 🛠️ Tech Stack

- **Language**: Python
- **Frameworks**: TensorFlow, Keras
- **Libraries**:
  - NumPy, Pandas
  - Matplotlib, Seaborn
  - OpenCV
  - Scikit-learn
- **Augmentation**: Keras `ImageDataGenerator`
- **Environment**: Google Colab
