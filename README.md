🕵️‍♀️ Fake Job Posting Detection

This project aims to detect fake job postings using advanced machine learning techniques. With the increasing number of online job scams, this project helps identify fraudulent job listings through automated classification models.

📌 Objective

To build and evaluate models capable of classifying job postings as fake or real by analyzing their content and structure.

📊 Dataset

The dataset includes labeled job postings with the following features:

Job title
Company profile
Job description
Requirements
Location
Employment type
Label: fraudulent (0 = Real, 1 = Fake)
🧹 Data Preprocessing

Preprocessing steps:

Removed missing values and duplicates
Dropped irrelevant columns (e.g., job ID, salary, logo)
Merged key text fields (e.g., description, requirements) for unified analysis
Text cleaned: lowercased, punctuation removed, and standardized

🧠 Feature Engineering

🔡 TF-IDF Vectorization

1-Applied TF-IDF (Term Frequency–Inverse Document Frequency) on textual data.
2-Transformed text into numerical form for model input.
3-Limited to the top 5,000 features to focus on the most relevant terms and reduce dimensionality.
🤖 Models Trained

🌲 Random Forest (RF)

1-A powerful ensemble model that builds multiple decision trees and averages their outputs.
2-Performed well in identifying fake jobs based on structured and TF-IDF-based features.

🧠 BERT (Bidirectional Encoder Representations from Transformers)

1-A pre-trained deep learning model developed by Google for understanding language context.
2-Fine-tuned for fake job classification.
3-Used raw text inputs for deep semantic analysis, outperforming traditional models on contextual understanding.

📈 Results

1-Random Forest showed high accuracy and interpretability with TF-IDF inputs.
2-BERT achieved superior performance in capturing deeper patterns in text, offering higher precision and recall for detecting fraud.

📌 Conclusion

This project proves that combining traditional machine learning (Random Forest) with state-of-the-art deep learning (BERT) enables robust detection of fraudulent job postings. It has practical applications for job platforms and users who want to avoid online scams.
