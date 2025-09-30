# A Framework for Analyzing and Detecting Bengali Malicious Memes: A Spectrum from Benign Humor to Inflamatory And Outright Hate

 
[![Python Version](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)

This repository includes dataset, code, and models for [Title of Paper] of Bengali memes.

---

## 📌 Overview

Traditional content moderation approaches often rely on **topic-based or binary classification** (hate vs. non-hate).  
This project introduces a **culturally aware, communicative-intent-driven framework** for Bengali memes, aiming to detect nuanced intents in multimodal content.

### Why it Matters
1. Automated Content Moderation: Traditional systems rely on users to manually report malicious content. This project automates the detection process, leading to faster and more efficient moderation without burdening users.

2. Proactive Intervention: Simply blocking users for overt hate speech is a reactive measure. This work focuses on identifying the more subtle, inflammatory content that often precedes hate speech. By understanding sarcastic and nuanced language, we can intervene earlier.

3. Nuanced Threat Analysis: The model helps distinguish between generally hostile communities and those specifically creating and spreading targeted hate speech. This allows for more precise moderation and a better understanding of the origins of harmful content.

4. Advanced Linguistic Support: This project is designed to handle code-mixed and code-switched language. This is a critical feature for accurately analyzing modern online conversations, where conventional tools often fail. 

The system classifies memes into three categories:

| Category      | Description |
|---------------|-------------|
| **Hate**  | Personal or group attacks, harassment |
| **Inflamatory** | Content designed to provoke controversy or manipulate emotions |
| **Benign**  | Neutral, humorous, or non-offensive content |

---

## 🗂 Dataset

### Bangla Intent Dataset (BID)
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

## 📈 Evaluation

- **Metric:** Macro F1-score and Accuracy
- **Performance:** **77.65% Macro F1**, improving 5.3% over strong baselines.  
- **Baseline models:** Standard multimodal classification baselines for benchmarking.

---

## 🛠 Installation

1. Clone the repository:
```bash
git clone https://github.com/<username>/bengali-meme-intent-classification.git
cd bengali-meme-intent-classification
```


## 📂 Repository Structure
```
bengali-meme-intent-classification/
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
Rakib Ullah : Coding,Conceptaulization,Formal Analysis,Data-Creation,Annotation GuideLine Formulation, Writing Original Draft
Mominul Islam : Writing And Review, Supervision, Data-Curation
```

## 📚 Citation
```
@inproceedings{rakib2025bengali,
  title={Low-Resource Multimodal Content Moderation: Intent-Aware Classification of Bengali Memes},
  author={Rakib Ullah et al.},
  year={2025},
}
```
