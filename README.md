# Age-Invariant Face Recognition using FaceNet and MTCNN

## Overview

This project presents an age-invariant face recognition system that integrates FaceNet and Multi-task Cascaded Convolutional Networks (MTCNN). The system is designed to accurately recognize faces across diverse age groups by mitigating the effects of facial aging, without requiring age-specific datasets.

This work was published in the International Journal of Scientific Research in Engineering and Management (IJSREM), Volume 08, Issue 05, May 2024.

## Key Features

* Age-invariant face recognition across different age groups
* Accurate face detection and alignment using MTCNN
* Robust feature extraction using FaceNet embeddings
* No requirement for age-specific or age-labeled datasets
* High recognition accuracy on benchmark datasets

## System Architecture

The system follows a sequential pipeline:

1. MTCNN detects faces and performs alignment.
2. FaceNet extracts discriminative facial embeddings.
3. Similarity matching is performed using distance metrics.

**Pipeline Flow:**

Input Image → MTCNN (Detection and Alignment) → FaceNet (Feature Extraction) → Similarity Metric → Match Result

## Workflow

The complete workflow of the age-invariant face recognition system is described below:

1. **Image Input**: The user uploads or captures an image.
2. **Face Detection (MTCNN)**: Facial regions are detected and bounding boxes with five key landmarks (eyes, nose, mouth corners) are extracted.
3. **Face Alignment**: The detected face is geometrically normalized using affine transformations to ensure consistent orientation and scale.
4. **Feature Extraction (FaceNet)**: The aligned face is passed through FaceNet to generate a 128-dimensional embedding vector.
5. **Embedding Storage and Comparison**:

   * During enrollment, embeddings of known individuals are stored in a database.
   * During recognition, new embeddings are compared with stored ones using Euclidean or cosine distance.
6. **Decision Making**:

   * If the similarity score is below a predefined threshold, a match is declared.
   * Otherwise, the face is classified as unknown.
7. **Result Output**: The system displays the identified individual and confidence score.

## Workflow Diagram (Textual Representation)

```
Image Input
     ↓
Face Detection (MTCNN)
     ↓
Face Alignment
     ↓
Feature Extraction (FaceNet)
     ↓
Embedding Comparison (Euclidean or Cosine Distance)
     ↓
Match Result
```

## Datasets Used

* **LFW (Labeled Faces in the Wild)**: Unconstrained face dataset
* **IMDB-WIKI**: Large-scale dataset with wide age variations
* **MORPH**: Longitudinal dataset capturing facial aging over time
* **CACD (Celebrities in Aging Database)**: Dataset focused on age progression in celebrity images

## Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1-score
* ROC curve and AUC

## Preprocessing Steps

* Image normalization to handle illumination variations
* Face alignment using detected facial landmarks
* Data augmentation techniques such as rotation, scaling, and translation

## Implementation Details

* **Programming Language**: Python
* **Frameworks**: TensorFlow, Keras
* **Libraries**: OpenCV, NumPy, Matplotlib, Scikit-learn
* **Hardware**: GPU-enabled system for accelerated computation

### Training Pipeline

1. Dataset split into training, validation, and testing sets
2. Data augmentation to increase robustness
3. Transfer learning and fine-tuning of FaceNet
4. Integration of MTCNN for preprocessing
5. Performance monitoring and early stopping to avoid overfitting

## Results

The integrated FaceNet–MTCNN framework demonstrated:

* High recognition accuracy across age groups
* Improved facial alignment and reduced false positives
* Stable performance without age-based categorization

## Applications

* Security and surveillance systems
* Biometric access control
* Personal identification systems
* Intelligent customer service interfaces

## Future Scope

* Enhanced robustness under varying lighting and environmental conditions
* Integration of GAN-based age progression and regression models
* Deployment and testing in real-world, large-scale environments

## Acknowledgement

The author expresses sincere gratitude to East West Institute of Technology, Mrs. Shruthi T V (Assistant Professor, ISE), and Dr. Suresh M B (Professor and Head, ISE) for their continuous guidance and support.

## References

Key references include works by Schroff et al. (2015), Zhang et al. (2016), and other significant contributions in deep learning-based face recognition and facial aging research.

## Citation

Darshan M et al., "Age-Invariant Face Recognition using FaceNet and MTCNN," International Journal of Scientific Research in Engineering and Management (IJSREM), Volume 8, Issue 5, May 2024. DOI: 10.55041/IJSREM32848

---

**Developed by:** Darshan M
**Academic Year:** 2024–2025
