# 🚀 AI Projects Repository

This repository contains two distinct mini-projects aimed at solving common problems in recommendation systems and chatbot relevance using rule-based logic and transformer models respectively.

---

## 📌 Project 1: Solving Repetitive Product Recommendations

### 🧩 Problem
Recommender systems often show the same type of product repeatedly, reducing variety and user engagement.

### 🎯 Goal
Avoid redundancy by balancing:
- User interest
- Unseen items
- Cross-category variety

### 🔧 Tools & Tech
- Python (core logic)
- Rule-based filtering (no ML used)
- `random` module for shuffling
- Google Colab
- List & dictionary operations

### ⚙️ Core Logic
1. Track product categories the user sees frequently.
2. Temporarily down-rank or remove over-shown categories.
3. Recommend from less-shown ones.
4. Shuffle results to keep variety.

### 💡 Example
If user browses "Shoes" repeatedly:
- Hide "Shoes"
- Show alternatives like "T-Shirts", "Jackets", etc.
- Shuffle for freshness

### 📎 Colab Link
[View Colab Notebook](https://colab.research.google.com/drive/1BDS1HVhJpUxPVCQHfn08JqNKWmHr6W-d)

---

## 🤖 Project 2: Avoiding Generic Replies – Chatbot with T5 Transformer

### 🧩 Problem
Customer support bots often give generic, repetitive answers.

### 🎯 Goal
Fine-tune a **T5 Transformer** to generate specific and context-aware support replies using real Twitter support data.

### 📦 Dataset
- Source: Kaggle (Customer Support on Twitter)
- Key Features: `text`, `inbound`, `response_tweet_id`, `tweet_id`

### ⚙️ Methodology
1. **Preprocessing**: Cleaned and paired tweets (customer + support)
2. **Input Format**: `"question: <customer_query>"`
3. **Model**: `t5-small` from Hugging Face
4. **Training**: 10 epochs on 37 tweet pairs using `Trainer`

### 🔧 Tools & Tech
- Hugging Face Transformers & Datasets
- Google Colab
- `pandas`, `kagglehub`

### 📈 Results
- Training loss reduced from **4.07 → 1.77**
- Outputs context-specific and non-generic responses

---

## 📂 Folder Structure

