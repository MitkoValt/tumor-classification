# Brain Tumor Classification in MRI Scans

This project focuses on automated detection of brain tumors in MRI scans using classical Machine Learning algorithms, Convolutional Neural Networks (CNNs), and Transfer Learning with MobileNetV2.

---

## Goal

Develop a model that distinguishes between MRIs **with** and **without** tumors. Compared approaches:

- Classical ML (Logistic Regression, Random Forest, SVM)
- Custom CNN
- Transfer Learning (MobileNetV2)

---

## Dataset

- **Source**: [Brain MRI Images for Brain Tumor Detection (Kaggle)](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)  
- **Classes**: `yes` (tumor), `no` (no tumor)  
- **Image size**: 512×512, grayscale (some RGB)  
- **Preprocessing**:
  - Resize to 224×224
  - Normalize (0–1)
  - Label-encoding (0 = no tumor, 1 = tumor)

---

## Models

### Classical ML

- Logistic Regression  
- Random Forest  
- Support Vector Machine (SVM)  

> Trained on flattened preprocessed image data.

### Deep Learning

- CNN: basic Conv2D + MaxPooling architecture  
- MobileNetV2: pretrained (transfer learning, feature extraction)

---

## Results

| Model               | Test Accuracy |
|----------------------|---------------|
| Logistic Regression  | 0.85 |
| Random Forest        | 0.88 |
| SVM                  | 0.86 |
| CNN (custom)         | 0.90 |
| MobileNetV2           | **0.93** |

---

## Visual Examples

| Tumor | No Tumor |
|-------|-----------|
| ![](data/yes/Y1.jpg) | ![](data/no/N1.jpg) |

---

## Tools

- Python (3.10)
- scikit-learn
- OpenCV
- TensorFlow / Keras
- Matplotlib / Seaborn
- Jupyter Notebook

---

## Learnings

- Classical ML provides a solid baseline
- CNNs capture image patterns more effectively
- Transfer learning (MobileNetV2) performs well even on small datasets
- Visual error analysis is key for model improvement

---

## Next Steps

- Hyperparameter tuning for CNNs
- Cross validation
- Confusion matrix + precision/recall
- Grad-CAM visualizations
- Export as `.h5` model

---

## Author

**Mitko Valtchev**  
M.Sc. Computer Engineering – TU Berlin  
Focus: Machine Learning for Medical Imaging

---

## License

This project is public for educational use. Please provide attribution.


