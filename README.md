# RAG-1 – A Simple Semantic QA Demo

This is a lightweight demo of a Retrieval-Augmented Generation (RAG) system. The goal is simple:  
→ find the most relevant document based on a question,  
→ then use a large language model (LLM) to generate a natural-language answer.

## 💡 What It Does

- I start with a few example documents (e.g., facts about Atatürk, Ankara, and Python).
- Each one is converted into an embedding vector using SentenceTransformers.
- A user asks a question. The question is also embedded into a vector.
- FAISS searches for the closest document semantically.
- Finally, the most relevant document + the question is passed into Falcon-7B-Instruct to generate the answer.

Basically, it’s a simple "understand before answering" kind of pipeline.

## 🧰 Tools & Libraries

- `sentence-transformers` (MiniLM)
- `faiss-cpu`
- `transformers` + Falcon 7B
- `torch`
- `numpy`

## ⚙️ How to Run

### Requirements

- Python 3.10+
- At least 16 GB VRAM (for Falcon)
- Or use Google Colab Pro (A100 recommended)

### Setup

```bash
git clone https://github.com/Mmtemre/RAG-1.git
cd RAG-1
pip install -r requirements.txt
