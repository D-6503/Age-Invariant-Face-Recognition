# 🧠 Age-Invariant Face Recognition using FaceNet and MTCNN

## 📘 Overview

This project presents an **age-invariant face recognition system** that integrates **FaceNet** and **Multi-task Cascaded Convolutional Networks (MTCNN)**. The system is designed to accurately recognize faces across diverse age groups by mitigating the effects of facial aging without requiring age-specific datasets.

Published in **International Journal of Scientific Research in Engineering and Management (IJSREM), Volume 08, Issue 05, May 2024**.

## 🚀 Key Features

* **Age-Invariant Recognition**: Robust face recognition across different age groups.
* **Face Detection & Alignment**: Utilizes MTCNN for precise face localization and alignment.
* **Feature Extraction**: Employs FaceNet for mapping facial images to a high-dimensional embedding space.
* **No Age-Specific Databases Needed**: Works effectively without categorizing or segmenting by age.
* **High Accuracy**: Demonstrates state-of-the-art results on benchmark datasets.

## 🧩 System Architecture

1. **MTCNN** – Detects and aligns faces to standardize pose and geometry.
2. **FaceNet** – Extracts discriminative embeddings for each aligned face.
3. **Similarity Matching** – Uses Euclidean or cosine distance for face comparison.

```
Input Image → MTCNN (Detection & Alignment) → FaceNet (Feature Extraction) → Similarity Metric → Match Result
```

## 🔄 Workflow

The complete workflow of the **Age-Invariant Face Recognition System** is illustrated below:

1. **Image Input**: User uploads or captures an image.
2. **Face Detection (MTCNN)**: The MTCNN detects facial regions and extracts bounding boxes with five key facial landmarks (eyes, nose, mouth corners).
3. **Face Alignment**: The detected face is geometrically normalized using affine transformations for consistent input to the model.
4. **Feature Extraction (FaceNet)**: The aligned face is passed through the FaceNet model to generate a unique 128-dimensional embedding vector.
5. **Embedding Storage/Comparison**:

   * **Enrollment Phase**: The embeddings of known faces are stored in a database.
   * **Recognition Phase**: The embedding of a new face is compared with stored embeddings using **Euclidean** or **Cosine similarity**.
6. **Decision**:

   * If similarity score < threshold → **Match Found** ✅
   * Else → **Unknown Face** ❌
7. **Result Display**: Outputs the name/ID of the recognized individual and confidence level.

### 🔧 Workflow Diagram (Textual Representation)

```
                ┌────────────────────────┐
                │      Image Input       │
                └──────────┬─────────────┘
                           │
                           ▼
                ┌────────────────────────┐
                │  Face Detection (MTCNN)│
                └──────────┬─────────────┘
                           │
                           ▼
                ┌────────────────────────┐
                │   Face Alignment        │
                └──────────┬─────────────┘
                           │
                           ▼
                ┌────────────────────────┐
                │  Feature Extraction     │
                │      (FaceNet)         │
                └──────────┬─────────────┘
                           │
                           ▼
                ┌────────────────────────┐
                │ Embedding Comparison    │
                │ (Euclidean/Cosine Dist.)│
                └──────────┬─────────────┘
                           │
                           ▼
                ┌────────────────────────┐
                │      Match Result       │
                └────────────────────────┘
```

## 🧪 Datasets Used

* **LFW (Labeled Faces in the Wild)** – Unconstrained face dataset.
* **IMDB-WIKI** – Large-scale dataset with age diversity.
* **MORPH** – Longitudinal dataset capturing aging over time.
* **CACD (Celebrities in Aging Database)** – For studying facial aging in celebrities.

## 📊 Evaluation Metrics

* **Accuracy**
* **Precision**
* **Recall**
* **F1-Score**
* **ROC Curve & AUC**

## ⚙️ Preprocessing Steps

* **Normalization** – Adjust brightness and contrast.
* **Face Alignment** – Using MTCNN for consistent geometry.
* **Image Augmentation** – Rotation, scaling, and translation for robustness.

## 💻 Implementation Details

* **Programming Language**: Python
* **Frameworks**: TensorFlow, Keras
* **Libraries**: OpenCV, NumPy, Matplotlib, Scikit-learn
* **Hardware**: GPU-enabled system for faster training

### Training Pipeline

1. Dataset split into train/validation/test.
2. Data augmentation for diversity.
3. Fine-tuning FaceNet with transfer learning.
4. Integrating MTCNN pre-processing pipeline.
5. Monitoring model performance and early stopping to prevent overfitting.

## 📈 Results

The integrated **FaceNet-MTCNN framework** achieved:

* High recognition accuracy across age groups.
* Improved alignment and reduced false positives.
* Consistent performance without the need for age categorization.

### Example Output

| Input Image (Child) | Matched Image (Adult) | Result  |
| ------------------- | --------------------- | ------- |
| 👦 Childhood Photo  | 🧔 Adult Photo        | ✅ Match |

## 🧠 Applications

* **Security and Surveillance Systems**
* **Access Control Systems**
* **Personal Identification**
* **Customer Service Interfaces**

## 🔮 Future Scope

* Improve robustness under varying lighting and environmental conditions.
* Incorporate GAN-based models for synthetic age progression/regression.
* Real-world deployment and testing in large-scale systems.

## 🙏 Acknowledgement

Special thanks to **East West Institute of Technology**, **Mrs. Shruthi T V (Assistant Professor, ISE)**, and **Dr. Suresh M B (Professor & Head, ISE)** for their invaluable support and guidance.

## 📚 References

Key references include works by Schroff et al. (2015), Zhang et al. (2016), and others on deep learning, face recognition, and generative adversarial networks (GANs).

## 🧾 Citation

> Darshan M, et al. "Age-Invariant Face Recognition using FaceNet and MTCNN." *International Journal of Scientific Research in Engineering and Management (IJSREM)*, Vol. 8, Issue 5, May 2024. DOI: 10.55041/IJSREM32848

---

**Developed by:** *Darshan M*
**Year:** *2024-2025*
