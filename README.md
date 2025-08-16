# 📌 BBC News Topic Modeling

## 📖 Overview
This project applies **Topic Modeling** techniques to the **BBC News dataset** to uncover hidden themes within news articles.  
Using **Latent Dirichlet Allocation (LDA)** and **Non-negative Matrix Factorization (NMF)**, the project extracts dominant topics from news descriptions and visualizes them with **pyLDAvis** and **Word Clouds**.  

The dataset is unsupervised, so topic modeling helps in automatically grouping articles into meaningful categories without predefined labels.

---

## 📊 Dataset
- **Source:** [BBC News Dataset (Kaggle)](https://www.kaggle.com/datasets/gpreda/bbc-news)  
- **Size:** ~40K articles  
- **Columns:**
  - `title` → Headline of the news article  
  - `pubDate` → Publication date  
  - `guid` → Unique identifier  
  - `link` → URL to the full article  
  - `description` → News article text (used for topic modeling)  

---

## ⚙️ Tools & Libraries
- **Python**  
- **NLTK** / **spaCy** → Text preprocessing (tokenization, lemmatization, stopword removal)  
- **Gensim** → Latent Dirichlet Allocation (LDA)  
- **Scikit-learn** → Non-negative Matrix Factorization (NMF), TF-IDF Vectorization  
- **pyLDAvis** → Interactive topic visualization  
- **Matplotlib / WordCloud** → Word cloud visualization  

---

## 🔄 Workflow

### 1. Data Loading
- Downloaded the dataset using **kagglehub**.  
- Loaded into **Pandas DataFrame** for processing.  

### 2. Preprocessing
- Convert text to lowercase  
- Remove punctuation, numbers, and special characters  
- Tokenize text into words  
- Remove stopwords (NLTK)  
- Lemmatization using spaCy  

### 3. Topic Modeling
- **LDA (Latent Dirichlet Allocation)** with Gensim  
- **NMF (Non-negative Matrix Factorization)** with Scikit-learn  

### 4. Visualization
- **pyLDAvis** → Interactive topic visualization  
- **Word Clouds** → Highlight most significant words per topic  

### 5. Evaluation
- Compared **LDA** vs **NMF**  
- Observed differences in interpretability and sharpness of topics  

---

## 📌 Results
- Extracted **5 main topics** (configurable).  
- **LDA**: Provides probabilistic word-topic distributions, good for interpretability.  
- **NMF**: Faster and produces sharper topics with TF-IDF.  

---

## 🚀 How to Run
1. Clone this repository  
2. Open the notebook in **Google Colab** or Jupyter Notebook  
3. Run all cells step by step  

```bash
pip install kagglehub gensim pyLDAvis wordcloud nltk spacy scikit-learn
