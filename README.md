# Multilingual Cyberbullying Detection Through Integrated Sentiment and Emotion Analysis

## Project Overview

This project focuses on detecting cyberbullying in multilingual social-media text, particularly English, Hindi, and Hinglish code-mixed text.

The proposed system integrates multilingual language understanding with emotion, sentiment, and sarcasm analysis to improve cyberbullying detection.

## Objective

The objective of the project is to develop a multitask deep-learning model capable of analyzing multilingual and code-mixed social-media text while considering emotional and contextual information.

## Model Architecture

The proposed architecture combines:

- XLM-RoBERTa as the multilingual language-model backbone
- LoRA for parameter-efficient fine-tuning
- Bidirectional GRU (Bi-GRU) for sequence modelling
- Emotion-Aware Attention (EAA) to emphasize emotionally relevant information
- Four task-specific classification heads

The four tasks are:

1. Cyberbullying detection
2. Emotion classification
3. Sentiment analysis
4. Sarcasm detection

### Architecture Flow

Input Text
↓
XLM-RoBERTa
↓
LoRA Fine-Tuning
↓
Bidirectional GRU
↓
Emotion-Aware Attention
↓
Multitask Classification Heads
├── Cyberbullying
├── Emotion
├── Sentiment
└── Sarcasm

## Dataset

The project uses multilingual English, Hindi, and Hinglish text datasets.

The raw datasets are not included in this public repository because their redistribution permissions have not been established.

See [`data/README.md`](data/README.md) for information about the datasets used in the project.

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- XLM-RoBERTa
- PEFT / LoRA
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Seaborn
- NLTK
- Google Colab

## Training

The model was trained using a GPU-enabled environment. The notebook contains the preprocessing, model architecture, training, evaluation, and inference pipeline.

## Reported Results

The project was trained on 59,537 samples covering English, Hindi, and Hinglish text.

| Metric | Reported Result |
|---|---:|
| Overall Accuracy | 88.96% |
| Combined F1-score | 87.72% |
| Hinglish Emotion F1-score | 99.01% |
| Sarcasm Detection Accuracy | 95.89% |
| Cyberbullying Detection Performance | 69.83% |

## Repository Contents

```text
cyberbullying-detection/
├── README.md
├── requirements.txt
├── .gitignore
├── Cyberbully_FRP_GitHub.ipynb
├── data/
│   └── README.md
└── results/
    └── results_summary.md
