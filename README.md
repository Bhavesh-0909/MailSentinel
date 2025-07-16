# MailSentinel

**Email Threat Intelligence** is a full-stack application that uses Machine Learning to detect **spam**, **phishing**, and **malware-related** emails. The system is designed to assist users and organizations in identifying malicious emails before they can cause harm.

---

## 🚀 Project Overview

### 🎯 Problem Statement
Email remains the **#1 attack vector** for cyber threats like:
- 📩 **Phishing attacks** (credential theft, fraud)
- 🐛 **Malware distribution** (via attachments or links)
- 🗑️ **Spam overload** (wasting time and resources)

Despite spam filters, traditional methods often fail to detect **evolving threats**. This project aims to create an **intelligent and adaptive system** to classify emails based on real threats using machine learning.

---

## 🧠 How It Works

### 🔍 Machine Learning Pipeline

1. **Data Collection**
   - Public datasets (SpamAssassin, Nazario Phishing Corpus, etc.)
   - Labelled as: `spam`, `phishing`, or `ham` (legit)

2. **Preprocessing**
   - HTML tag removal
   - Lowercasing and punctuation cleanup
   - Tokenization and stopword removal

3. **Feature Extraction**
   - TF-IDF vectorization of email subject and body
   - Optional: embeddings from BERT for better accuracy

4. **Model Training**
   - Algorithms used: `Logistic Regression`, `Random Forest`, `XGBoost`
   - Evaluation metrics: Accuracy, Precision, Recall, F1 Score
   - Best performing model saved using `joblib`

5. **Threat Detection**
   - Email content passed to the model
   - Model outputs one of: `SPAM`, `PHISHING`, `HAM`

---

## 🧱 Tech Stack

### 📦 Backend
- **FastAPI** – REST API for prediction
- **Scikit-learn** – ML model training and inference
- **joblib** – Model serialization
- **email** module – Email parsing and cleanup

### 💻 Frontend
- **React.js** – Clean UI to input email content
- **Axios** – For sending prediction requests to backend

### 🧠 ML Libraries
- Scikit-learn
- NLTK
- Pandas / NumPy
- Optional: HuggingFace Transformers (for BERT)

---

## 🖼️ Screenshots

> _Add screenshots here after building the frontend_

---

## 🔄 Workflow

1. **User pastes email** subject and body into the UI
2. The text is sent to the FastAPI backend
3. Email is cleaned and transformed into feature vectors
4. The model predicts the category (SPAM, PHISHING, HAM)
5. Result is displayed back on the frontend

---

## 📁 Project Structure
```
email-threat-intelligence/
├── backend/
│ ├── app/ (FastAPI routes, inference logic)
│ ├── models/ (trained ML models)
├── frontend/
│ ├── components/, pages/, App.jsx
├── data/ (raw and cleaned email datasets)
├── notebooks/ (training and evaluation notebooks)
```

---

## ⚙️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/your-username/email-threat-intelligence.git
cd email-threat-intelligence
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload
cd ../frontend
npm install
npm start
```
---

Let me know if you want me to:
- Add **badges** (e.g., version, license, made with love)
- Auto-generate a **training notebook**
- Or create a **live demo deployment guide**

Would you like a version of this README for GitHub with images and better formatting?