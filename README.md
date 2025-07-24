# CNN_ON_MALARIA_DATASET

# 🦠 Malaria Cell Image Classification with CNN

This project uses a Convolutional Neural Network (CNN) to classify cell images as **Parasitized** or **Uninfected**, leveraging the [Malaria Cell Images Dataset](https://www.tensorflow.org/datasets/catalog/malaria) from TensorFlow Datasets.

---

## 📊 Model Performance

| Metric           | Value (Epoch 10) |
|------------------|------------------|
| Accuracy (Train) | ~95.69%          |
| Loss (Train)     | ~0.1574          |
| Accuracy (Val)   | ~95.19%          |
| Loss (Val)       | ~0.1737          |

### 🧠 Epoch Progress Summary


---

## 🧬 Dataset

- **Source**: TensorFlow Datasets - `malaria`
- **Classes**: `Parasitized`, `Uninfected`
- **Image Size**: 128x128 (resized)
- **Total Samples**: ~27,558
- **Supervised**: Yes (`(image, label)` format)

---

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- Google Colab (GPU)
- Matplotlib (for plotting)

---

## 🧱 Model Architecture

```python
model = Sequential([
    Conv2D(32, (3, 3), activation='relu', input_shape=(128, 128, 3)),
    MaxPooling2D(2, 2),
    Conv2D(64, (3, 3), activation='relu'),
    MaxPooling2D(2, 2),
    Conv2D(128, (3, 3), activation='relu'),
    MaxPooling2D(2, 2),
    Flatten(),
    Dense(128, activation='relu'),
    Dropout(0.5),
    Dense(1, activation='sigmoid')
])
