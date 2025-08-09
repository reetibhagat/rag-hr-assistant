# rag-hr-assistant
Here’s a **README.md** draft for your `Nestlé_HR_Policy_RAG_Chatbot` project based on the uploaded notebook:

---

# Nestlé HR Policy RAG Chatbot 🤖📚

A Retrieval-Augmented Generation (RAG) chatbot for answering **Nestlé HR policy-related questions** using **LangChain**, **Groq LLM**, **FAISS vector store**, and a **Gradio interface**.

The chatbot retrieves relevant HR policy content from uploaded documents and generates concise, citation-backed responses.

---

## 🚀 Features

* **Context-aware answers** — Uses RAG to ensure responses are grounded in HR policy documents.
* **Citations** — Provides `[p<page>]` references for transparency.
* **Groq LLM integration** — Fast, low-latency responses via `langchain_groq.ChatGroq`.
* **Gradio UI** — Simple and interactive interface for employees to ask HR questions.
* **FAISS Vector Store** — Efficient document chunk retrieval.

---

## 🛠️ Tech Stack

* **LangChain** — RAG pipeline orchestration
* **langchain\_groq** — Groq LLM API integration
* **FAISS** — Vector similarity search
* **HuggingFace Embeddings** — Semantic text representation
* **PyPDFLoader / TextLoader** — Document ingestion
* **Gradio** — Chatbot frontend

---

## 📂 Project Structure

```
Nestlé_HR_Policy_RAG_Chatbot_(Gradio_+_Groq).ipynb  # Main Colab notebook
data/                                                # HR policy documents (PDF/TXT)
requirements.txt                                     # Dependencies list
README.md                                            # Project documentation
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

Or inside Colab:

```python
!pip install langchain langchain-community langchain-groq faiss-cpu pypdf gradio sentence-transformers
```

### 3. Set your Groq API key

```python
import os
os.environ["GROQ_API_KEY"] = "your_api_key_here"
```

---

## 📄 Usage

1. **Upload HR policy PDFs or text files** into the `data/` folder (or Colab workspace).
2. **Run the notebook** `Nestlé_HR_Policy_RAG_Chatbot_(Gradio_+_Groq).ipynb`.
3. **Start the chatbot** — A Gradio link will appear:

```
Running on local URL:  http://127.0.0.1:7860
Running on public URL: https://xxxx.gradio.live
```

4. **Ask questions** related to HR policies.

---

## 🧠 Example Queries

* *"How does PTO accrue for new employees?"*
* *"What is the maternity leave policy?"*
* *"When are performance reviews conducted?"*

---

## 🔐 Environment Variables

| Variable       | Description                                          |
| -------------- | ---------------------------------------------------- |
| `GROQ_API_KEY` | API key from [Groq Cloud](https://console.groq.com/) |

---

## 📌 Notes

* The chatbot **only answers based on provided HR documents**.
* If the answer isn’t in the context, it will say: *"I don't know based on the provided information."*

---

## 📜 License

This project is for internal HR use and follows Nestlé’s policy guidelines. Redistribution is restricted without permission.

---
