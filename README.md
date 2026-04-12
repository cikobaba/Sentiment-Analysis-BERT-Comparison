# Sentiment Analysis of Customer Reviews using NLP

[cite_start]This repository contains the source code for the comparative performance analysis of transformer-based language models (**BERT, RoBERTa, and DistilBERT**) on customer reviews collected from a Shopify-based e-commerce environment[cite: 7, 25].

[cite_start]This study specifically evaluates these models under **low-data conditions**, focusing on both predictive success and computational efficiency for Small and Medium-sized Enterprises (SMEs)[cite: 28, 30].

---

## 📌 Project Overview
[cite_start]The primary goal of this research is to compare state-of-the-art transformer architectures to identify the most suitable model for small businesses operating with limited customer feedback[cite: 25, 30].

### Technical Workflow & Implementation
[cite_start]The implementation follows a structured pipeline as described in the thesis methodology [cite: 467, 499, 500]:

* [cite_start]**Data Acquisition**: Loading raw data from Shopify CSV/Excel exports using `pandas`[cite: 348, 471].
* **Preprocessing**:
    * [cite_start]**Data Cleaning**: Removal of empty/duplicate entries and records without textual content[cite: 340, 400, 406].
    * [cite_start]**Translation**: Converting non-English reviews (Spanish, Italian, French, Dutch) into English via `deep-translator` to ensure consistency[cite: 410, 475].
* [cite_start]**Labeling**: Mapping star ratings (1-5) to sentiment labels: **Negative (0), Neutral (1), and Positive (2)**[cite: 352, 353].
* **Tokenization**: Utilizing `AutoTokenizer` to maintain architectural integrity. [cite_start]This ensures that **WordPiece** is loaded for BERT/DistilBERT and **Byte-Level BPE** is loaded for RoBERTa, as specified in the research[cite: 213, 245, 438, 481].
* [cite_start]**Model Training**: Supervised fine-tuning of pre-trained models on the specific Shopify dataset[cite: 455, 487].

---

## 📁 Repository Structure
[cite_start]The models are separated into individual notebooks to highlight architectural differences and facilitate independent testing[cite: 314, 452]:

1.  [cite_start]`bert_(1).ipynb`: Implementation of the `bert-base-uncased` model[cite: 230].
2.  [cite_start]`roberta.ipynb`: Implementation of the `roberta-base` model[cite: 236].
3.  [cite_start]`distilbert.ipynb`: Implementation of the `distilbert-base-uncased` model[cite: 263, 269].

---

## 📊 Summary of Results
[cite_start]Below is the summary of the performance and efficiency metrics derived from the experimental results (**Table 4** and **Table 5**)[cite: 536, 551]:

| Metric | BERT | RoBERTa | DistilBERT |
| :--- | :---: | :---: | :---: |
| **Accuracy** | 0.8667 | 0.8667 | 0.8667 |
| **F1-Score** | 0.8048 | 0.8048 | 0.8048 |
| **Inference Time (s)** | 0.5098 | 0.4533 | **0.3571** |
| **GPU Peak Memory** | 1312.70 MB | 1491.06 MB | **824.44 MB** |

> [cite_start]**Conclusion**: While classification performance remained consistent due to dataset imbalance, **DistilBERT** demonstrated superior efficiency in terms of speed and resource usage, making it the most practical choice for SME deployment[cite: 552, 560, 621, 622].

---

## 🎓 Academic Author
* [cite_start]**Student**: Anil Kaya (Student ID: 211ADB103) [cite: 4, 6]
* **Scientific Adviser**: Assoc. [cite_start]Prof. Ingars Eriņš [cite: 9, 10]
* [cite_start]**Institution**: Riga Technical University (RTU), 2026 [cite: 1, 11]

---
