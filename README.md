🧠 Document AI Chatbot

An AI-powered RAG (Retrieval Augmented Generation) system built with **Flowise** that reads and understands any business document and answers customer questions accurately and instantly — 24/7 automated support.

🌐 **Portfolio:** https://portfolio-pink-eta-84.vercel.app

---

## 🚀 Features

- 📄 **Upload any document** — PDF, Word, or text files
- 🧠 **AI understands content** — not just keyword search
- 💬 **Natural conversation** — ask questions in plain English
- ⚡ **Instant answers** — responds in seconds
- 🔄 **Works 24/7** — no human needed
- 🎯 **Accurate responses** — answers only from YOUR documents

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Flowise | Visual RAG builder |
| Groq (Llama 3.3) | AI language model |
| HuggingFace Embeddings | Document understanding |
| In Memory Vector Store | Knowledge storage |

---

## 🔄 How It Works
Upload Your Document (PDF)

↓

HuggingFace reads and understands it

↓

Knowledge stored in Vector Store

↓

User asks a question

↓

AI finds relevant information

↓

Groq generates natural answer

↓

User gets accurate response instantly

---

## ⚙️ Setup & Installation

1. Make sure you have **Flowise** running locally
2. Import the chatflow JSON into Flowise
3. Add your **Groq API key** (free at console.groq.com)
4. Add your **HuggingFace token** (free at huggingface.co)
5. Upload your document
6. Start chatting!

---

## 💡 Use Cases

- Customer support bots that know YOUR business
- IELTS coaching chatbots that answer from study material
- Restaurant bots that know the menu and prices
- Real estate bots that answer from property listings
- Hospital bots that answer from medical procedures
- Any business with documents that need answering!

---

## ⚡ Challenges & How I Solved Them

### 1. 🔑 API Quota Issues
**Problem:** Google Gemini free tier quota ran out during testing, completely blocking the AI responses.
**Solution:** Switched to **Groq** (completely free, no daily limits) as the LLM provider — which turned out to be faster than Gemini anyway!

### 2. 🧩 Node Connection Complexity
**Problem:** Flowise has many node types and connecting them correctly for RAG was confusing at first — especially choosing between LLM Chain and Conversational Retrieval QA Chain.
**Solution:** Discovered that **Conversational Retrieval QA Chain** is specifically designed for document Q&A while LLM Chain is for general chat — using the right chain solved all connection issues immediately.

### 3. 📦 Embeddings Model Selection
**Problem:** Google GenerativeAI Embeddings were not available in the Flowise version installed, causing the RAG pipeline to fail at the embeddings stage.
**Solution:** Switched to **HuggingFace Inference Embeddings** as a free alternative — worked perfectly and produced accurate document understanding.

---

## 🙋‍♂️ Author

**Asad** — AI Agent Builder & Digital Product Creator
Building AI-powered solutions for real-world use cases.

[![Portfolio](https://img.shields.io/badge/Portfolio-4F46E5?style=flat&logoColor=white)](https://portfolio-pink-eta-84.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/asad-ullah-b0190a236)
[![GitHub](https://img.shields.io/badge/GitHub-000000?style=flat&logo=github&logoColor=white)](https://github.com/greatman-786)
