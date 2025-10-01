# A Framework for Analyzing and Detecting Bengali Malicious Memes 
 
[![Python Version](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)

This repository includes dataset, code, and models for [Title of Paper] of Bengali memes.

---

## 📌 Overview

Traditional content moderation approaches often rely on **topic-based or binary classification** (hate vs. non-hate).  
This project introduces a **culturally aware**, ... for Bengali memes, aiming to detect nuanced intents in multimodal content.

### Why it Matters
1. Automated Detection: Replaces manual user reporting with a fast, automated system for more efficient content moderation.

2. Proactive Intervention: Moves beyond reacting to hate speech by identifying the subtle, X, and sarcastic content that often precedes it.

3. Precise Threat Analysis: Distinguishes between generally hostile groups and targeted hate-speech creators for more effective moderation.

4. Code-Mixed Language Support: Accurately analyzes modern online conversations that mix languages (e.g., Banglish), where conventional tools often fail.

The system classifies memes into three categories:

| Category      | Description |
|---------------|-------------|
| **X**  | Personal or group attacks, harassment |
| **Y** | Content designed to .... |
| **Z**  | Neutral, humorous, or non-offensive content |

---

## 🗂 Dataset

### Bangla X Dataset (BID)
- **Source:** 25 public Facebook groups  
- **Raw Memes:** 5,000 images → filtered to **3,247 multimodal memes**  
- **Annotation:** 3 expert annotators (Fleiss’ kappa: 0.79)  
- **Languages:** Bengali, English, and code-switched memes  
- **Splits:** 70% train / 15% validation / 15% test  
- **Text Extraction:** OCR (Gemini API) with manual correction  

The dataset, Annotation Guideline, Data Source and End-to-End Pipeline will be publicly available in this repository upon publication.

---
## Models and Fusion Strategies
| Model Type        | Model Name        |
|-------------------|-------------------|
| **Text Encoders** | Banglish-BERT     |
|                   | mDeBERTa-v3       |
|                   | XLM-RoBERTa       |
|                   | MuRIL             |
|                   | mBERT             |
| **Visual Encoders** | ResNet50        |
|                   | ConvNeXt          |
|                   | Swin Transformer  |
|                   | ViT-B16           |
|                   | EfficientNet-B3   |
|                   | FocalNet          |
| **Fusion Approaches** | Co-Attention |
|                   | Cross-Attention   |
|                   | CLIP              |
|                   | Early Fusion      |
|                   | Late Fusion       |

---


## Example of Memes
<img width="500" height="500" alt="photo-collage png" src="https://github.com/user-attachments/assets/e694afd8-e4d0-4cf2-b1db-c7214d9aae73" />


## 📈 Evaluation

- **Metric:** Macro F1-score and Accuracy
- **Multi-Modal Performance:** **77.65% Macro F1**, improving 5.3% over best baseline with task-adapted Co-attention Fusion
- **Baseline Performance:** **72.35% Macro F1** with MDeberta

---

## 🛠 Installation

1. Clone the repository:
```
git clone https://github.com/secrakib/Bengali_Malicious_Memes.git
```


## 📂 Repository Structure
```
bengali-meme-x-classification/
├── 📄 README.md
├── 📄 LICENSE
├── 📁 Annotation Guideline/
│   └── (Annotation guidelines document)
├── 📁 Code/
│   └── (Main code files)
├── 📁 Facebook Troll Groups/
│   └── (List of Facebook troll groups)
├── 📁 Graphics/
│   └── (Paper graphics and figures)
├── 📁 Results with experimental details/
│   └── (Experimental results and details)
├── 📁 dataset/
    └── (Meme dataset)
```
## Contribution
```
Rakib Ullah : Coding,Conceptaulization,Formal Analysis,Data-Creation,Annotation-GuideLine-Formulation, Writing-Original-Draft
Mominul Islam : Writing And Review, Supervision, Data-Curation, Project-Administration
Sanjid Ahmed : Data-Curation, Writing-Original-Draft
```

## 📚 Citation
```
@inproceedings{rakib2025bengali,
  title={Low-Resource Multimodal Content Moderation: X-Aware Classification of Bengali Memes},
  author={Rakib Ullah et al.},
  year={2025},
}
```
