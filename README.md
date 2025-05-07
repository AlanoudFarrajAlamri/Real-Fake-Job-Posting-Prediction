# 🕵️ Fake Job Postings Detection

## 📌 Overview
Job fraud is a growing problem, especially with the increasing reliance on online job platforms. This project aims to use machine learning and natural language processing (NLP) techniques to detect fake job postings based on their textual content and associated metadata.

---

## 🎯 Objective
The primary goal of this project is to build a classification system that accurately identifies whether a job posting is **fake or legitimate**. This system can help job seekers avoid scams and assist job platforms in filtering out malicious content.

---

## 📊 Dataset
We used the **Fake Job Postings dataset** from Kaggle. It includes over 17,000 job postings with the following features:

- **Company Information** (company name, location, department)
- **Job Description Fields** (title, description, requirements, benefits)
- **Metadata** (telecommuting status, employment type, required experience, etc.)
- **Target Variable**: `fraudulent` (1 = Fake, 0 = Real)

---

## 🧠 Approach

### 1. **Data Preprocessing**
- Removed missing values, irrelevant columns, and duplicates
- Combined and cleaned text columns (e.g., title, description, requirements)
- Lowercased all text and removed special characters and stopwords
- Tokenized and lemmatized the textual content

### 2. **Feature Engineering**
- Applied **TF-IDF Vectorization** on combined text fields with a vocabulary size limited to 5,000 features
- Retained only the most relevant metadata for modeling

### 3. **Model Training**

We trained and compared two main models:

#### ✅ **Random Forest Classifier (RF)**
- Traditional machine learning model
- Trained on TF-IDF features
- Tuned using GridSearchCV for optimal parameters

#### ✅ **BERT (Bidirectional Encoder Representations from Transformers)**
- Pre-trained deep learning model for natural language understanding
- Fine-tuned on job posting text
- Achieved higher accuracy and robustness for subtle language-based fraud patterns

---

## 📈 Results & Performance

| Model      | Accuracy | Precision | Recall | F1-Score |
|------------|----------|-----------|--------|----------|
| Random Forest | ~0.96    | High      | Moderate | Good     |
| BERT         | ~0.98    | Very High | High    | Excellent |

- BERT outperformed Random Forest in all major metrics.
- The use of NLP and pre-trained models proved highly effective for fraud detection.

---

## 🧪 Project Highlights
- Balanced NLP and tabular modeling approaches
- High-performing models with strong recall for fraud detection
- Scalable to large datasets using BERT architecture
- Clean modular code for reproducibility and enhancement

---

## 🤝 Contributions
Feel free to fork the repo, suggest enhancements, or raise issues!
---

## 🙏 Acknowledgments
Thanks to open-source contributions and [Kaggle](https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction/data) for the dataset on real or fake job.

---
