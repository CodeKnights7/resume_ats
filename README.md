# 💼 Resume ATS – AI-Powered Resume Screening Web Platform

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red?logo=pytorch)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers-yellow?logo=huggingface)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-green?logo=fastapi)
![React](https://img.shields.io/badge/React-Frontend-61DAFB?logo=react)
![Model](https://img.shields.io/badge/Model-DeBERTa%20v3--base-purple)

---

# 🚀 Resume ATS – Smart Resume Scoring Platform

An AI-powered web application that evaluates resumes and generates an intelligent **ATS compatibility score** based on job-role alignment.

Designed for recruiters, hiring managers, and HR teams to quickly identify high-potential candidates using a fine-tuned Transformer model.

---

# 🎯 What This Platform Does

* Upload a resume via the web interface
* Instantly analyze job-role relevance
* Generate an AI-based ATS score
* Rank candidates efficiently
* Reduce manual screening time

This system simulates how modern Applicant Tracking Systems (ATS) evaluate resumes in real-world hiring environments.

---

# 💼 15 Job Roles Covered

The model is trained to evaluate resumes for:

* Software Engineer
* Data Scientist
* Product Manager
* DevOps Engineer
* Finance Analyst
* Marketing Manager
* Sales Manager
* HR Manager
* UX Designer
* Operations Manager
* Full Stack Developer
* Cloud Architect
* Business Analyst
* QA Engineer
* Data Engineer

---

# 🖥️ Web Application Workflow

```id="webflow1"
User Uploads Resume (Frontend - React)
            ↓
Resume Text Extraction
            ↓
API Request to Backend
            ↓
AI Model Processing
            ↓
ATS Score Returned to Web App
            ↓
Score Displayed to User
```

---

# 🧠 AI Model Architecture

## Base Model: microsoft/deberta-v3-base (Fine-Tuned)

This system uses a transformer-based deep learning model trained specifically for resume scoring.

### Architecture Diagram

```id="archdiagram1"
Resume Text
     ↓
DeBERTa Encoder (Transformer Backbone)
     ↓
[CLS] Token Representation
     ↓
Linear Layer (Regression Head)
     ↓
Single Continuous ATS Score
```

---

## 🔍 Model Explanation (Simple & Clear)

### 1️⃣ DeBERTa Encoder

* Reads and understands the resume context
* Captures skills, experience, and semantic meaning
* Provides powerful contextual embeddings

### 2️⃣ CLS Token Representation

* Summarizes the entire resume into one vector
* Acts as the main feature representation

### 3️⃣ Linear Regression Head

* Converts the embedding into a score
* Predicts how well the resume matches the selected role

### 4️⃣ Output

* A single continuous ATS score
* Higher score = Stronger role alignment

---

# 📉 Training Configuration

* **Model:** microsoft/deberta-v3-base
* **Task Type:** Regression
* **Loss Function:** `nn.MSELoss()`
* **Framework:** PyTorch + HuggingFace Transformers

### Why Regression?

ATS scoring is not classification (selected/rejected).
It predicts a **continuous match score**.

Mean Squared Error is used:

```id="mseformula1"
MSE = (1/n) Σ (Predicted - Actual)²
```

This ensures stable and smooth learning behavior.

---

# ⚙️ Backend Working (Behind the Web App)

Although this is a web platform, the backend handles:

* Resume text preprocessing
* Tokenization using DeBERTa tokenizer
* Model inference
* Score normalization
* Returning structured JSON response

### Backend Flow

```id="backendflow1"
Resume Text
     ↓
Tokenizer
     ↓
Fine-Tuned DeBERTa Model
     ↓
Regression Head
     ↓
ATS Score
     ↓
API Response (JSON)
```

The backend is designed to be:

* Scalable
* Modular
* Cloud-deployable
* Production-ready

---

# 🏗️ Full System Architecture (SaaS Ready)

```id="fullsystem1"
React Frontend
       ↓
API Layer
       ↓
AI Inference Engine (DeBERTa)
       ↓
Score Generation
       ↓
User Dashboard Display
```

---

# 🌟 Key Highlights

* State-of-the-art Transformer architecture
* Fine-tuned specifically for resume scoring
* Regression-based ATS prediction
* Clean web-based user experience
* Production SaaS-ready design
* Easily extendable for enterprise hiring systems

---

# 📈 Future Enhancements

* Skill-gap detection
* Resume improvement suggestions
* Multi-role comparison scoring
* Recruiter analytics dashboard
* Cloud deployment with CI/CD
* Enterprise integration

---

# 👨‍💻 Author

**Karthik Kallapiran**
AI Developer | NLP Engineer | Deep Learning Enthusiast

GitHub: [https://github.com/CodeKnights7](https://github.com/CodeKnights7)

---

> Built to make intelligent hiring faster, smarter, and AI-driven.
