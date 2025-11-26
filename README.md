# 📚 RAGTool Demo: Personal Research Assistant

A local **Retrieval-Augmented Generation (RAG)** tool designed to help researchers chat with their PDF documents. This tool leverages **Google Gemini** for advanced reasoning and embeddings, paired with **ChromaDB** for efficient, local vector storage.

---

## ✨ Features

- **🔒 Local Storage:** Your vector database is stored entirely locally in `chroma_db/`.
- **📝 Source Citations:** Every answer includes citations, telling you exactly which document the information came from.
- **🧠 Persistent Memory:** Ingest your PDFs once, and the database remembers them for future sessions.
- **🚀 Powered by Gemini:** Uses Google's state-of-the-art models for embeddings and text generation.

---

## 🛠️ Prerequisites

- **Python 3.9+** installed on your machine.
- A **Google AI Studio API Key**. [Get one here](https://aistudio.google.com/).

---

## 📦 Installation

1. **Clone the repository** (or download the source code):
   ```bash
   git clone https://github.com/sifat371/rag-tool.git
   cd rag-tool
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

---

## 🌐 Setup Environment

Copy `.env.example` to a new file named `.env`.

Open `.env` and paste your Google API Key.

---

## 🚀 Usage

1. **Generate Sample Data** (Optional)

   If you don't have PDFs handy, run this helper script to create a dummy research paper in `sample_data/`:

   ```bash
   python utils/generate_sample_pdf.py
   ```

2. **Ingest Documents**

   Place your real PDFs in the `sample_data/` folder (or keep the generated one). Then run:

   ```bash
   python src/main.py --ingest
   ```

3. **Chat with your Papers**

   Start the chat interface:

   ```bash
   python src/main.py
   ```

---

## 📚 Project Structure

- `src/rag_engine.py`: Handles loading, splitting, embedding, and retrieval logic.
- `src/main.py`: The Command Line Interface (CLI) for the user.
- `utils/`: Helper scripts.
- `chroma_db/`: Where the vector database files will be created (auto-generated).
