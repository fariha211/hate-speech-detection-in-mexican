# Multimodal Hate Speech Detection in Memes from Mexico using BLIP

This repository contains the implementation of the approach presented in our IberLEF 2024 paper, **"Multimodal Hate Speech Detection in Memes from Mexico using BLIP"**. The project addresses the task of detecting harmful content in Spanish-language memes by leveraging multimodal image-text representations extracted from the BLIP vision-language model and classifying them using a Gradient Boosting classifier.
Paper Link: https://ceur-ws.org/Vol-3756/DIMEMEX2024_paper3.pdf

## Abstract

The rapid spread of online content has increased the need for automatic detection of harmful and inappropriate material. In this work, we propose a multimodal framework for meme classification that combines visual and textual information using BLIP (Bootstrapping Language-Image Pre-training). The extracted image-text embeddings are subsequently used to train a Gradient Boosting classifier for categorizing memes into three classes:

- Hateful
- Inappropriate
- Harmless

The proposed approach was evaluated on the DIMEMEX 2024 shared task dataset.

## Methodology

Our pipeline consists of three main stages:

### 1. Data Preprocessing
- Extract meme images and associated text.
- Translate Spanish text into English.
- Process images and text using the BLIP processor.

### 2. Feature Extraction
- Generate multimodal embeddings using a pre-trained BLIP model.
- Apply mean pooling to obtain fixed-size feature representations.

### 3. Classification
- Train a Gradient Boosting Classifier on the extracted embeddings.
- Predict one of the three target categories.

## Dataset

The experiments were conducted using the dataset provided by the **DIMEMEX 2024 Shared Task**, which focuses on the detection of inappropriate memes from Mexico. The dataset contains Spanish-language memes annotated as:

- Hateful
- Inappropriate
- Harmless

Dataset statistics:

| Split | Samples |
|---------|---------:|
| Train | 2263 |
| Test | 648 |

【1-7c5350】

## Results

Official results obtained on the DIMEMEX 2024 test set:

| Metric | Score |
|----------|-------|
| Precision | 0.52 |
| Recall | 0.50 |
| Macro F1-score | 0.47 |

Ranking:
- 3rd in Precision
- 3rd in Recall
- 5th in Macro F1-score

## Requirements

Typical dependencies include:

```bash
torch
transformers
scikit-learn
numpy
pandas
Pillow
deep-translator
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Citation

If you use this repository, please cite:

```bibtex
@inproceedings{maqbool2024multimodal,
  title={Multimodal Hate Speech Detection in Memes from Mexico using BLIP},
  author={Fariha Maqbool and Elisabetta Fersini},
  booktitle={Proceedings of IberLEF 2024},
  year={2024}
}
```
