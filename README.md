pullRequest --> Repo

# Fingerprint Models & Codebase Overview

## Project Summary
This repository contains advanced fingerprint analysis models and code for biometric identification, gender classification, and detection of altered fingerprints. The project leverages deep learning architectures (CNNs, ResNet) and robust data engineering to address real-world challenges in fingerprint recognition.

## Models & Structure

### 1. Altered vs Real Fingerprint Detection
- **Purpose:** Distinguish between genuine and altered fingerprints (Easy, Medium, Hard levels).
- **Files:**
  - `src/group_work/Altered vs real/Altered Easy vs Real.ipynb`
  - `src/group_work/Altered vs real/Medium altered vs real.ipynb`
  - `src/group_work/Altered vs real/Hard Altered vs Real.ipynb`
  - Model weights: `RVA.keras`, `RVA2.keras`, `RVA3.keras`
- **Approach:** Uses CNNs and ResNet, with data augmentation, regularization, and oversampling to handle class imbalance. Evaluation via AUC-ROC, confusion matrix, and classification reports.

### 2. Fingerprint Identification
- **Purpose:** Identify individual fingerprints and finger types (Easy, Medium, Hard levels).
- **Files:**
  - `src/group_work/Fingerprint Identification/Easy_Medium_ID_Fingername_identification.ipynb`
  - `src/group_work/Fingerprint Identification/Hard_ID_Fingername_identification.ipynb`
- **Approach:** Custom image parsing, label extraction, and multi-class classification using deep learning. Handles subject ID and finger type mapping.

### 3. Gender Classification from Fingerprints
- **Purpose:** Predict gender from fingerprint images, including altered samples.
- **Files:**
  - `src/group_work/Gender Classification Model/1st Model(Altered easy).ipynb`
  - `src/group_work/Gender Classification Model/AlteredMedium.ipynb`
  - `src/group_work/Gender Classification Model/HardAltered.ipynb`
  - Model weights: `Gender1.keras`, `Gender2.keras`, `Gender3.keras`
- **Approach:** CNN-based models, advanced preprocessing, and random oversampling for imbalanced data. Evaluation via confusion matrix and classification report.

## Dataset
- **Source:** [SOCOFing - Sokoto Coventry Fingerprint Dataset](https://www.kaggle.com/datasets/ruizgara/socofing)
- **Composition:**
  - Real: 6,000 images
  - Altered Easy: 17,931 images
  - Altered Medium: 17,067 images
  - Altered Hard: 14,272 images
- **Location:** `Recess_Project_Template/resources/datasets/dataset.csv`

## Key Technologies
- Python, TensorFlow, Keras, scikit-learn, OpenCV, imbalanced-learn
- Deep learning (CNN, ResNet), image augmentation, regularization, early stopping

## Usage
1. Clone the repository.
2. Explore notebooks in `src/group_work/` for model training, evaluation, and experimentation.
3. Use `.keras` model files for inference or further training.
4. Dataset and images are in `resources/datasets` and `resources/images`.

## Project Organization
- **src/group_work/**: All collaborative model development and experiments.
- **resources/**: Datasets and images for reproducibility.
- **docs/**: Project documentation and guidelines.
- **reports/**: Project reports and presentations.

## License
This project is licensed under the MIT License. See [LICENSE](./LICENSE) for details.

---
For questions or collaboration, please open an issue or contact the maintainers.
