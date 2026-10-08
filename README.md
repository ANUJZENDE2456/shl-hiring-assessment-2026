# SHL Hiring Assessment 2026 — Grammar Scoring

This repository contains my solution for the SHL Hiring Assessment 2026 audio grammar-scoring challenge.

## Objective

Predict a grammar score from spoken-audio clips. The competition metric is RMSE, where lower is better.

## Solution

The current notebook contains the modeling pipeline used for the final work:

- Acoustic audio features and an ExtraTrees baseline
- Whisper encoder representations
- Whisper-small / Whisper-medium representation experiments
- WavLM-large hidden-state representations
- Regression models including SVR, Ridge, and ExtraTrees
- Non-negative linear stacking of model predictions
- WavLM layer-combination experiments

The notebook was developed in stages so different representations could be evaluated using consistent cross-validation splits.

## Final Kaggle Result

The best submitted result was:

**Stage 6 — Public RMSE: 0.4200**

This remains the selected/final Kaggle submission.

A later Stage 6.1 experiment was also submitted and achieved **0.4231**, so it was not selected over Stage 6.

### Submission history

| Submission | Public RMSE | Result |
|---|---:|---|
| Stage 2 | 0.4215 | Earlier submission |
| Stage 5 | 0.4494 | Earlier submission |
| **Stage 6** | **0.4200** | **Final selected** |
| Stage 6.1 | 0.4231 | Not selected |

## Repository Structure

```text
.
├── SHL_Grammar_Scoring.ipynb
├── README.md
├── RESULTS.md
├── requirements.txt
└── .gitignore
```

## Reproducibility

The competition dataset and audio files are not included in this repository.

The notebook is intended for code and methodology review. The competition data must be supplied separately in the Kaggle environment.

Install the dependencies with:

```bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

## Technologies

- Python
- PyTorch
- Hugging Face Transformers
- Whisper
- faster-whisper
- WavLM
- Librosa
- scikit-learn
- LightGBM
- spaCy
- Sentence Transformers
- Pandas
- NumPy

## Data / Security

Private competition data, audio files, generated caches, model weights, embeddings, API keys, and other secrets are intentionally excluded from this repository.
