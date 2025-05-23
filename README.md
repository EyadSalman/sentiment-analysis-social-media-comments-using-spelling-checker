# 🧠 Sentiment Analysis on Social Media Using Spelling Checker

This project performs **sentiment analysis** on user comments from merged dataset of **Twitter, Reddit, and YouTube**, with a focus on improving accuracy by applying **spelling correction** during text preprocessing. The pipeline classifies comments as **positive**, **negative**, or **neutral**, using classical NLP models and vectorization techniques.

---

## 🔍 Objective

- Classify social media comments into sentiment categories
- Normalize text with spell correction to handle noisy, user-generated data
- Compare performance of multiple classifiers
- Visualize insights from real-world public sentiment

---

## 📁 Dataset Sources

- YouTube comment dataset (CSV)
- Reddit threads (JSON or CSV)
- Twitter replies and threads (CSV)

Each dataset contains:
- Raw comment text
- Platform label (YouTube, Twitter, Reddit)
- Manually labeled or preprocessed sentiment classes

---

## ⚙️ Pipeline Overview

1. **Data Collection & Integration**
   - Combined datasets from multiple platforms
   - Balanced sentiment classes (positive, negative, neutral)

2. **Preprocessing**
   - Lowercasing, punctuation removal, tokenization
   - Stopword removal
   - **Spelling correction using `TextBlob` or `SymSpell`**
   - Lemmatization (WordNetLemmatizer)

3. **Vectorization**
   - `TfidfVectorizer` and `CountVectorizer`
   - N-gram range tuning for better context

4. **Model Training**
   - Logistic Regression
   - Naive Bayes (MultinomialNB)
   - Support Vector Machine (SVM)
   - Random Forest (optional)

5. **Evaluation**
   - Accuracy, Precision, Recall, F1-score
   - Confusion Matrix and Classification Report

6. **Visualization**
   - Sentiment distribution bar charts
   - Word clouds per sentiment
   - Misclassified sample analysis

---

## 🧠 Technologies Used

- Python 3.9+
- pandas, numpy, seaborn, matplotlib
- scikit-learn
- nltk, re, string
- `TextBlob` or `SymSpell` for spell correction
- `wordcloud` for visualizing frequent terms

---

## 📈 Results Snapshot

| Model              | Accuracy (with spellcheck) |
|--------------------|----------------------------|
| Logistic Regression| 69%                        |
| Naive Bayes        | 67%                        |
| SVM                | 76%                        |
| Random Forest      | 80%                        |      

> Accuracy improved by ~3-5% with spelling correction on noisy datasets.
