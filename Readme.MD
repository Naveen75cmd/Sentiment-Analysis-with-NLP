# README.md

# 🎬 Sentiment Analysis with 50K IMDB Movie Reviews

This project performs **Sentiment Analysis** on the popular **50,000 IMDB Movie Reviews Dataset** using a complete NLP pipeline and Logistic Regression. The final processed dataset is exported for visualization in **Power BI**, where a dashboard shows sentiment distribution, review samples, and KPIs.

---

## 🚀 Project Workflow

### 1. Dataset
- Dataset: **IMDB Dataset of 50K Movie Reviews**
- Columns:
  - `review` — raw IMDB review text  
  - `sentiment` — positive/negative  

---

## 🧹 2. Data Preprocessing (NLP Pipeline)

The following text-cleaning steps were applied:

- Remove HTML tags  
- Remove punctuation  
- Lowercase normalization  
- Tokenization  
- Stopword removal  
- Lemmatization  
- Final cleaned text stored in: `cleaned_review`

---

## 🔢 3. Feature Engineering — TF-IDF

Text is converted to numerical vectors using:
```python
TfidfVectorizer(max_features=5000)
```
- 5000 most important words  
- Output shape: `(50000, 5000)`  

---

## 🤖 4. Model Training — Logistic Regression  
Data split:
- 80% Train  
- 20% Test  
- Stratified sampling  

### ✔ Performance:
- **Accuracy:** ~0.888  
- **F1 Score:** 0.89  

Model predicts:
- `predicted_sentiment_label`  
- `predicted_sentiment`

---

## 📊 5. Power BI Export

Final CSV generated:

**`sentiment_analysis_results_for_power_bi.csv`**

Columns included:
- `review`
- `sentiment`
- `predicted_sentiment`
- `review_length`

Used to build a Power BI dashboard with:
- Donut chart (Positive vs Negative)
- Total reviews KPI
- Average review length KPI
- Slicer for sentiment
- Table with review text + predicted sentiment

---

## 📁 Project Structure

```
├── Sentiment_Analysis.ipynb
├── IMDB Dataset.csv
├── sentiment_analysis_results_for_power_bi.csv
├── README.md
└── requirements.txt
```

---

## ▶️ How to Run

### Install dependencies
```bash
pip install -r requirements.txt
```

### Run the notebook
```bash
jupyter notebook Sentiment_Analysis.ipynb
```

### Upload IMDB Dataset and run all cells.

---

## ✨ Key Features
- Full NLP pipeline  
- Machine Learning model training  
- Cleaned dataset generation  
- Power BI dashboard ready  
- Lightweight, easy to run  

---

## 📬 Author
**NAVEEN M S**

---

# requirements.txt

pandas
numpy
nltk
scikit-learn
tqdm
regex
google-colab
