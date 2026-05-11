# Amazon Reviews Sentiment Analysis: From TF-IDF to RoBERTa

[![Hugging Face Model](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Model-blue)](https://huggingface.co/mlklt3/amazon-sentiment-roberta-base)
[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://amazon-sentiment-analysis-zmix2tcdvc7qhzq7syzxcj.streamlit.app/)

## 📌 Project Overview
This project focuses on building a robust Sentiment Analysis system for Amazon Fine Food reviews. It explores the evolution of Natural Language Processing (NLP) techniques, comparing traditional machine learning approaches with state-of-the-art Transformer models. 

The final solution is fine-tuned to classify customer feedback into **Negative**, **Neutral**, and **Positive** categories and is deployed as an interactive web application.

## 🚀 Key Features
* **End-to-End Pipeline:** From raw data cleaning to cloud deployment.
* **Model Comparison:** Evaluates **TF-IDF + Logistic Regression** vs. **DistilBERT** and **RoBERTa**.
* **Advanced Preprocessing:** Implementation of POS-tag-based Lemmatization for linguistic accuracy.
* **SOTA Performance:** Utilizes RoBERTa to handle complex linguistic nuances like negation and sarcasm.
* **Interactive Deployment:** Real-time inference via a **Streamlit** dashboard integrated with the **Hugging Face Hub**.

## 📊 Dataset
The project uses the **Amazon Fine Food Reviews** dataset.
* **Initial size:** ~568k reviews.
* **Processing:** Removed duplicates and handled significant class imbalance through undersampling to create a balanced dataset of 15,000 samples.

## 🛠️ Tech Stack
* **Language:** Python
* **Data Analysis:** Pandas, NumPy, Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn (TF-IDF, Logistic Regression)
* **Deep Learning:** PyTorch, Hugging Face Transformers & Datasets
* **Models:** DistilBERT, RoBERTa-base
* **Deployment:** Streamlit, Hugging Face Hub

## 📈 Model Performance Summary
| Model | Accuracy | F1-Score (Weighted) | Note |
| :--- | :---: | :---: | :--- |
| **TF-IDF + Logistic Reg.** | 70% | 0.70 | Baseline benchmark |
| **DistilBERT** | 73% | 0.73 | Efficient & Fast |
| **RoBERTa-base** | **78%** | **0.78** | **Best at context/negation** |

## 💡 Business Insights

* **The Challenge of Neutrality:** Neutral sentiment proved to be the most difficult to classify across all models due to the presence of mixed feedback. This suggests that for businesses, neutral reviews represent a critical "gray area" that often contains specific, actionable suggestions for product improvements hidden between balanced pros and cons.
* **Value of Advanced NLP:** Transitioning to Transformer-based models provided a significant **8% boost in accuracy** over traditional machine learning methods. This performance leap justifies the higher computational costs for high-stakes customer satisfaction monitoring where precision is paramount.
* **Real-time Scalability:** By leveraging the Hugging Face Hub and Streamlit, this project demonstrates how state-of-the-art models can be transformed into accessible tools for real-time sentiment tracking and rapid intervention.

## 💻 Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/emilka23/amazon-sentiment-analysis.git](https://github.com/emilka23/amazon-sentiment-analysis.git)

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
2. **Run the Streamlit App:**
   ```bash
   streamlit run app.py
