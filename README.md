# 🧠 Document AI Chatbot

A RAG system built in Flowise that reads a business document and answers questions from it — only from it, not from the model's general knowledge.

## 🚀 What it does

- Takes a PDF, Word or text document
- Understands the content rather than keyword-matching it
- Answers questions in plain English, in seconds
- Answers only from the document you gave it

## 🛠️ Tech stack

| Tool | Purpose |
|---|---|
| Flowise | Visual RAG builder |
| Groq (Llama 3.3) | Language model |
| HuggingFace Embeddings | Document understanding |
| In-memory vector store | Knowledge storage |

## 🔄 How it works

```
Document uploaded
      ↓
HuggingFace embeds it
      ↓
Stored in the vector store
      ↓
Question asked
      ↓
Relevant passages retrieved
      ↓
Groq writes the answer from those passages
```

## ⚙️ Building it yourself

The chatflow export isn't published in this repo. To rebuild it in Flowise:

1. Run Flowise locally
2. Add a **Conversational Retrieval QA Chain** — not an LLM Chain
3. Connect a Groq node with your API key (free at console.groq.com)
4. Connect HuggingFace Inference Embeddings with your token (free at huggingface.co)
5. Add an in-memory vector store and a document loader
6. Upload your document and start asking

## 💡 Where it fits

Customer support that knows one business · exam coaching from study material · restaurant menus and prices · property listings · any set of documents people keep asking questions about.

## ⚡ Problems I hit, and what I did

**1. Ran out of Gemini quota mid-build.** Free tier limits stopped the responses dead. Switched to Groq — free, no daily cap, and faster than what I'd been using.

**2. Picked the wrong chain type.** Flowise has a lot of nodes and the connections weren't working. The answer: Conversational Retrieval QA Chain is built for document Q&A, LLM Chain is for general chat. Using the right one fixed every connection problem at once.

**3. The embeddings model wasn't available.** Google GenerativeAI Embeddings didn't exist in my Flowise version, so the pipeline failed at the embedding stage. Switched to HuggingFace Inference Embeddings — free, and the retrieval quality was good.

---

**Asad Ullah** — AI automation and QA engineer. [Portfolio](https://asad-portfolio-drab.vercel.app) · [GitHub](https://github.com/greatman-786)
