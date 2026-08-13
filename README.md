# Multilingual Cyberbullying Detection Through Integrated Sentiment and Emotion Analysis

A research project for detecting cyberbullying in multilingual social-media text, with a focus on English, Hindi, and Hinglish code-mixed text.

## Project Overview

The system uses a multitask deep-learning architecture that combines:

- **XLM-RoBERTa** as the multilingual language-model backbone
- **LoRA** for parameter-efficient fine-tuning
- **Bidirectional GRU (Bi-GRU)** for sequence modeling
- **Emotion-Aware Attention (EAA)** to emphasize emotionally relevant context
- Four task-specific heads for:
  - Cyberbullying detection
  - Emotion classification
  - Sentiment analysis
  - Sarcasm detection

The multitask objective jointly learns the four related tasks.

## Project Structure

```text
cyberbullying-detection/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   └── Cyberbully_FRP_GitHub.ipynb
├── data/
│   └── README.md
├── results/
│   └── results_summary.md
└── docs/
```

## Dataset

The project uses two datasets covering multilingual English, Hindi, and Hinglish text. The raw CSV files are not included in this public repository because redistribution rights have not been established.

See [`data/README.md`](data/README.md) for details.

## Model Architecture

```text
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
Shared Representation
    ├── Cyberbullying Head
    ├── Emotion Head
    ├── Sentiment Head
    └── Sarcasm Head
```

## Training

The reported project experiments used a consumer-level GPU/Google Colab environment. The notebook contains the preprocessing, model construction, training, evaluation, and inference pipeline.

## Reported Results

The project report reports training on **59,537 text samples** across English, Hindi, and Hinglish.

| Metric | Reported Result |
|---|---:|
| Overall Accuracy | 88.96% |
| Combined F1-score | 87.72% |
| Hinglish Emotion F1-score | 99.01% |
| Sarcasm Detection Accuracy | 95.89% |
| Cyberbullying Detection Performance | 69.83% |

See [`results/results_summary.md`](results/results_summary.md).

## How to Run

1. Install Python and the packages in `requirements.txt`.
2. Obtain the datasets through their original sources and confirm that their licenses permit use.
3. Place the datasets in the `data/` directory using the filenames expected by the notebook.
4. Open `notebooks/Cyberbully_FRP_GitHub.ipynb`.
5. Run the notebook on a suitable GPU-enabled environment such as Google Colab.

The XLM-RoBERTa base model is downloaded through the Hugging Face Transformers library when the notebook runs.

## Author

**Prakriti Krishna**

Role in the academic project included model architecture design, training strategy and evaluation planning, data preprocessing, PPT preparation, and manuscript writing.

## Note

This repository is a public project artifact prepared from an academic research project. The public repository does not include private documents, consent forms, similarity/AI reports, raw datasets, or trained model checkpoints.
