# PCVC Speech Classification using Wav2Vec2

## Overview

This project implements a **speech classification pipeline** for the **PCVC (Persian Consonant-Vowel Combination) Speech Dataset** using **Wav2Vec2**, a state-of-the-art self-supervised speech representation model. The notebook performs end-to-end preprocessing, feature extraction, model training, and evaluation to classify spoken utterances.

The project demonstrates how modern deep learning-based speech embeddings can be combined with a lightweight classifier to achieve robust speech recognition performance.

---

## Features

* Automatic download of the PCVC Speech Dataset
* Audio preprocessing and silence removal
* Fixed-length audio normalization
* Feature extraction using **Facebook's Wav2Vec2**
* Logistic Regression classifier
* Train/Test split for evaluation
* Performance analysis using:

  * Accuracy
  * Precision
  * Recall
  * F1-Score
  * Confusion Matrix
* Audio visualization and waveform inspection

---

## Dataset

The project uses the **PCVC (Persian Consonant-Vowel Combination) Speech Dataset**, downloaded automatically using **KaggleHub**.

The dataset contains recordings of Persian consonant-vowel combinations spoken by multiple speakers and is commonly used for speech recognition and speech processing research.

---

## Project Workflow

```
Download Dataset
        │
        ▼
Load Audio Files (.mat)
        │
        ▼
Silence Removal
        │
        ▼
Length Normalization
        │
        ▼
Train/Test Split
        │
        ▼
Feature Extraction
     (Wav2Vec2)
        │
        ▼
Logistic Regression
        │
        ▼
Performance Evaluation
```

---

## Audio Preprocessing

Before feature extraction, each audio sample undergoes several preprocessing steps:

* Load speech signals from MATLAB (.mat) files
* Remove leading and trailing silence
* Normalize signal duration
* Convert signals into a consistent format
* Prepare data for Wav2Vec2 feature extraction

---

## Feature Extraction

The project uses the pretrained **Facebook Wav2Vec2** model from the Hugging Face Transformers library.

Advantages include:

* Self-supervised speech representations
* No handcrafted acoustic features required
* Robust embeddings for downstream speech classification
* High-quality contextual speech features

---

## Classification Model

The extracted Wav2Vec2 embeddings are used to train a **Logistic Regression** classifier.

This approach combines powerful deep speech representations with a computationally efficient classifier, making the model fast to train while maintaining strong classification performance.

---

## Evaluation Metrics

The notebook evaluates the classifier using:

* Accuracy
* Precision
* Recall
* F1-Score
* Classification Report
* Confusion Matrix

Visualization of prediction results helps assess model performance across different speech classes.

---

## Technologies Used

* Python
* NumPy
* Pandas
* SciPy
* Matplotlib
* Librosa
* Scikit-learn
* PyTorch
* Hugging Face Transformers
* KaggleHub

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/pcvc-speech-classification.git
cd pcvc-speech-classification
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install numpy pandas scipy matplotlib librosa scikit-learn torch transformers kagglehub tqdm
```

---

## Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
PCVCFinal.ipynb
```

Run all notebook cells sequentially.

The notebook will:

1. Download the dataset.
2. Preprocess the audio files.
3. Extract Wav2Vec2 embeddings.
4. Train the Logistic Regression classifier.
5. Evaluate the model.
6. Display performance metrics and visualizations.



## Results

The implemented pipeline demonstrates that pretrained Wav2Vec2 embeddings provide highly discriminative speech representations for the PCVC dataset. Combined with a Logistic Regression classifier, the model offers an effective and computationally efficient solution for speech classification.

---

## Future Improvements

Potential extensions include:

* Fine-tuning Wav2Vec2 on the PCVC dataset
* Experimenting with HuBERT and Whisper embeddings
* CNN or Transformer-based classifiers
* Speaker-independent evaluation
* Data augmentation techniques
* Hyperparameter optimization
* Deployment as a web application using Streamlit or Flask

---

## References

* Facebook AI Research – Wav2Vec2
* Hugging Face Transformers
* PCVC Speech Dataset
* Librosa Audio Processing Library
* Scikit-learn Documentation

---

## License

This project is intended for educational and research purposes.

---

