# 🤖 Simple RAG Chatbot Workshop

## Quick & Easy Implementation with Hugging Face

A streamlined 70-minute workshop for building simple but effective RAG (Retrieval-Augmented Generation) chatbots using FAQ datasets and Hugging Face transformers.

![Workshop Banner](https://img.shields.io/badge/Workshop-Simple%20RAG-blue?style=for-the-badge&logo=python)
![Status](https://img.shields.io/badge/Status-Complete-green?style=for-the-badge)
![Duration](https://img.shields.io/badge/Duration-70%20minutes-orange?style=for-the-badge)

---

## 📋 Workshop Overview

This workshop provides a simple, hands-on journey from CSV data to a working web chatbot in just 70 minutes. Perfect for beginners and those who want to understand RAG fundamentals without complexity.

### 🎯 Learning Objectives

- Understand RAG (Retrieval-Augmented Generation) basics
- Use Hugging Face transformers for text embeddings
- Build simple similarity-based question matching
- Create interactive chatbots with confidence scoring
- Deploy a web interface with Gradio

### 🏗️ Simple Architecture

```
User Question → Text Embeddings → Similarity Search → FAQ Match → Answer + Confidence
     ↓              ↓                  ↓              ↓               ↓
  "What hours?"  [0.1, 0.8, ...]   Cosine Similarity  Best FAQ    "9AM-6PM (High)"
```

---

## 📚 Simple Workshop Structure

### 📊 Day 1: Quick Data Analysis (15 minutes)

**Notebook:** `Day1_Simple_Data_Analysis.ipynb`

**What you'll do:**

- Load CSV FAQ dataset
- Count categories and entries
- Simple visualization
- Quick data overview

**Time:** 15 minutes - just the basics!

### 🤖 Day 2: Build RAG Chatbot (30 minutes)

**Notebook:** `Day2_Simple_RAG_Chatbot.ipynb`

**What you'll do:**

- Install packages automatically
- Load Hugging Face embedding model
- Create text embeddings for FAQ questions
- Build simple chatbot class with similarity matching
- Test with confidence scoring

**Key Features:**

- Automatic package installation
- SentenceTransformers embeddings (`all-MiniLM-L6-v2`)
- Cosine similarity matching
- Smart "I don't know" responses
- Confidence scores (High/Medium/Low)

### 🌐 Day 3: Web Interface (25 minutes)

**Notebook:** `Day3_Simple_Web_Chatbot.ipynb`

**What you'll do:**

- Rebuild chatbot for web use
- Create beautiful Gradio interface
- Add example questions
- Launch web app with public link

**Features:**

- Professional web UI
- Example questions
- Real-time responses
- Shareable public link

---

## 🚀 Quick Start

### Prerequisites

```bash
# Python 3.8+ required
# The notebooks will auto-install packages for you!
```

### 📁 Simple Project Structure

```
workshop2/
├── README.md                          # This guide
├── requirements_simple.txt           # Essential packages only
├── data/
│   └── simple_faq.csv                # 15 FAQ entries ready to use
└── notebooks/
    ├── Day1_Simple_Data_Analysis.ipynb      # 15 min - data overview
    ├── Day2_Simple_RAG_Chatbot.ipynb        # 30 min - build chatbot
    └── Day3_Simple_Web_Chatbot.ipynb        # 25 min - web interface
```

### 📖 Step-by-Step Usage

1. **Day 1 (15 min)**: Open `Day1_Simple_Data_Analysis.ipynb` and run all cells
2. **Day 2 (30 min)**: Open `Day2_Simple_RAG_Chatbot.ipynb` and run all cells
3. **Day 3 (25 min)**: Open `Day3_Simple_Web_Chatbot.ipynb` and run all cells

That's it! No complex setup, no tokens required for basic functionality.

---

## 🎯 Sample FAQ Dataset

Simple CSV with 15 FAQ pairs covering:

- **General:** Business hours, company info
- **Support:** Contact methods, customer service
- **Payment:** Credit cards, PayPal, bank transfers
- **Shipping:** Delivery times, international shipping
- **Returns:** Return policies, damaged items
- **Orders:** Tracking, cancellation
- **Account:** Sign up, password reset
- **Discounts:** Student discounts, coupons

### ✅ Questions the Chatbot CAN Answer:

- "What are your business hours?"
- "How can I contact customer support?"
- "What payment methods do you accept?"
- "How long does shipping take?"
- "What is your return policy?"
- "Do you ship internationally?"
- "How do I track my order?"
- "Can I cancel my order?"

### ❌ Questions That Return "I Don't Know":

- "What's the weather today?"
- "How do I cook pasta?"
- "Tell me a joke"

---

## 🔧 Simple Configuration

### Adjust Similarity Threshold

```python
# In Day 2 notebook - make it more/less strict
bot = SimpleRAGBot(model, df, embeddings, threshold=0.3)
# Lower = more permissive (0.1-0.2)
# Higher = more strict (0.5-0.7)
```

### Essential Packages Only

```txt
pandas
numpy
scikit-learn
sentence-transformers
gradio
matplotlib
```

---

## 📊 How It Works

### Simple RAG Process

1. **Load FAQ data** from CSV file
2. **Create embeddings** using SentenceTransformers
3. **Find similar question** using cosine similarity
4. **Return answer** if similarity > threshold
5. **Say "I don't know"** if similarity too low

### Confidence Scoring

- **High (0.7+)**: Very confident match
- **Medium (0.3-0.7)**: Decent match
- **Low (<0.3)**: No good match - returns "I don't know"

---

## 🌐 Web Interface Features

- **Clean UI** with Gradio
- **Example questions** to get started
- **Real-time responses** with confidence
- **Public sharing link** to share your bot
- **No complex setup** required

---

## 🛠️ Simple Troubleshooting

### Package Installation Issues

```bash
# If sentence-transformers fails to install
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install sentence-transformers
```

### Model Download Issues

```python
# The notebooks handle this automatically
# But if needed, models download to ~/.cache/torch/sentence_transformers/
```

### Memory Issues

```python
# Use a smaller model if you have limited RAM
model = SentenceTransformer('all-MiniLM-L6-v2')  # Small & fast (already default)
```

---

## 🚀 What You'll Build

By the end of this workshop, you'll have:

✅ **Working RAG chatbot** that answers FAQ questions  
✅ **Web interface** people can actually use  
✅ **Confidence scoring** so users know how sure the bot is  
✅ **Smart fallbacks** for questions outside your FAQ scope  
✅ **Understanding of RAG** concepts and how they work

## � Next Steps

Want to improve your chatbot? Try:

- **Add more FAQs** to the CSV file
- **Adjust the threshold** for stricter/looser matching
- **Try different models** like `all-mpnet-base-v2`
- **Add conversation memory** to remember chat history
- **Deploy to cloud** using Hugging Face Spaces

---

## 🤝 Simple & Educational

This workshop focuses on:

- ✅ **Understanding over complexity** - simple but effective
- ✅ **Hands-on learning** - build while you learn
- ✅ **Real results** - working chatbot you can demo
- ✅ **Quick wins** - see results in minutes, not hours
- ✅ **Foundation building** - understand core concepts

Perfect for beginners, students, and anyone who wants to understand RAG without getting lost in production complexities!

---

**🎉 Ready to build your first RAG chatbot? Start with Day 1!** 🚀
