# Classroom Emotion Detection Using Hybrid ResNet + Transformer Model

## Overview

This project presents a **Hybrid Deep Learning Framework** for detecting facial emotions in classroom environments using a combination of **ResNet** and **Transformer** architectures.
The system is designed to classify student emotions from classroom images and analyze emotional behavior in real-world educational environments.

The project explores **two experimental scenarios** for dataset preparation and evaluation:

1. **Scenario 1 — Standard Dataset Split**

   * Entire dataset was divided using an **80:20 train-test ratio**
   * Initial experiments were performed on the complete dataset
   * A major issue observed was **data imbalance and loss of important class information**, which negatively affected model performance

2. **Scenario 2 — Class-wise Distribution**

   * Dataset was distributed separately for each emotion class
   * Balanced samples were maintained across all classes
   * This approach improved training stability and overall classification performance

The final implementation uses the **class-wise distribution strategy** because it provides more reliable and balanced results.

---

# Features

* Hybrid architecture using:

  * ResNet for spatial feature extraction
  * Transformer for global feature learning
* Classroom emotion recognition
* Multi-class emotion classification
* Class-wise balanced data handling
* Performance evaluation using:

  * Accuracy
  * Precision
  * Recall
  * F1-Score
  * Confusion Matrix

---

# Project Structure

```bash
Classroom-Emotion-Detection/
│
├── dataset/
│   ├── train/
│   ├── test/
│   └── validation/
│
├── models/
│   ├── resnet_model.py
│   ├── transformer_model.py
│   └── hybrid_model.py
│
├── notebooks/
│   └── training.ipynb
│
├── results/
│   ├── confusion_matrix.png
│   ├── accuracy_graph.png
│   └── classification_report.txt
│
├── utils/
│   ├── preprocessing.py
│   ├── dataloader.py
│   └── metrics.py
│
├── requirements.txt
├── train.py
├── evaluate.py
└── README.md
```

---

# Methodology

## Hybrid Architecture

The proposed model combines:

### ResNet

Used for:

* Local feature extraction
* Deep spatial representation learning
* Capturing facial patterns

### Transformer

Used for:

* Global dependency learning
* Attention-based feature representation
* Understanding long-range relationships between facial regions

The extracted ResNet features are passed into the Transformer block for final emotion classification.

---

# Experimental Scenarios

## Scenario 1 — Random 80:20 Split

In the first experiment:

* Entire dataset was randomly divided into:

  * 80% Training
  * 20% Testing
* Although the model achieved reasonable accuracy, a major issue was observed:

  * Some classes became underrepresented
  * Important samples were lost during random splitting
  * Model performance became inconsistent for minority classes

---

## Scenario 2 — Class-wise Distribution

To overcome the imbalance issue:

* Each emotion class was distributed separately
* Balanced samples were ensured in training and testing sets
* The model achieved:

  * Better generalization
  * Improved class accuracy
  * More stable performance

This scenario produced the best overall results.

---

# Technologies Used

* Python
* PyTorch
* OpenCV
* NumPy
* Pandas
* Matplotlib
* Scikit-learn

---


# Results

The Hybrid ResNet + Transformer model demonstrated strong performance for classroom emotion detection.

### Key Observations

* Class-wise distribution improved model reliability
* Transformer enhanced global contextual understanding
* ResNet improved feature extraction quality
* Balanced datasets significantly improved classification performance

---


# Author

Muhammad Faizan Raja

---
