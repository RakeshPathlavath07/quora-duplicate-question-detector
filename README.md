# 🧠 Quora Duplicate Question Detection App (Streamlit)

This project builds a web-based application using Streamlit to detect whether two questions from Quora are duplicates or not. The system uses Natural Language Processing (NLP) techniques, feature engineering, and a machine learning model to predict question similarity.

---
Dataset Link - https://www.kaggle.com/c/quora-question-pairs
## 📊 Dataset

- **Source**: [Quora Question Pairs Dataset on Kaggle](https://www.kaggle.com/competitions/quora-question-pairs/data)
- **Size**: ~400,000+ question pairs
- **Fields**:
  - `qid1`, `qid2`: unique question IDs
  - `question1`, `question2`: the two questions to compare
  - `is_duplicate`: 1 if duplicate, 0 otherwise

---

## ⚙️ Tech Stack

| Component            | Technology          |
|----------------------|---------------------|
| Programming Language | Python              |
| Web Framework        | Streamlit           |
| NLP                  | NLTK, Spacy         |
| ML Models            | Logistic Regression, XGBoost |
| Feature Engineering  | FuzzyWuzzy, TF-IDF, Shared Word Features |
| Visualization        | Matplotlib, Seaborn |
| Model Deployment     | Pickle + Streamlit  |

---

## 🔍 Features & Engineering

- **Text Preprocessing**:
  - Lowercasing
  - Removing punctuation, stopwords
  - Lemmatization (using spaCy)
- **Similarity Features**:
  - Common words count
  - Total words ratio
  - Fuzzy string matching scores
  - Token set ratio and partial ratios

---

## 🧠 Machine Learning

- Trained multiple models (Logistic Regression, XGBoost) on extracted features.
- Used cross-validation for reliable results.
- Final model chosen based on highest F1-score and ROC-AUC.

---

## 🚀 Streamlit App

The user interface allows:
- Input of two custom questions
- Real-time prediction of "Duplicate" or "Not Duplicate"
- Confidence score
- Display of extracted similarity metrics

##Folder Structure
duplicate-question-detector/
│
├── app.py                    # Streamlit UI logic
├── model.pkl                 # Trained ML model
├── preprocessing.py          # Custom functions for cleaning & feature extraction
├── requirements.txt          # Dependencies
├── README.md                 # Project documentation
├── utils/                    # (Optional) Utility scripts
└── data/                     # Sample input data


To run:

```bash
streamlit run app.py
