# 🤖 Chatbot using RAG (Retrieval Augmented Generation)

This project is a **Streamlit-based RAG (Retrieval Augmented Generation) Chatbot** that allows users to **upload their own PDF documents** and interact with them conversationally.  
Instead of relying only on a language model, the chatbot **retrieves relevant information directly from your document**, ensuring **more accurate, context-specific and trustworthy responses**.

The system works in four key steps:
1. **PDF Loading:** Your uploaded document is read and processed.
2. **Chunking & Embeddings:** The document is split into meaningful text chunks and converted into vector embeddings using **HuggingFace BGE**.
3. **Vector Search with FAISS:** The embeddings are stored in a **FAISS vector database** for fast and relevant similarity search.
4. **Conversational QA:** The chatbot uses **Llama 3.3 (via Groq API)** and a **conversation memory buffer**, so the chat feels natural and context-aware.

This makes it ideal for:
- Study / Research
- Company Knowledge Base Chatbot
- PDFs like Policies, Reports, Notes, Books, Manuals
- Any scenario where you need **accurate answers from your own document**

## 📌 Features
- Retrieves accurate information from your data.
- Uses Embeddings to understand context.
- Lightweight and easy to run locally.
- `.env` file used to keep API Key **secure**.

---

## 🗂️ Project Structure
```
├── chatbot_using_rag.py # Main Python application
├── requirements.txt # Required Python libraries
├── .env # API Key (This file is NOT included for security)
```

## 🔧 Setup Instructions

### 1️⃣ Clone the repository
```
git clone https://github.com/<your-username>/Chatbot-using-rag.git
cd Chatbot-using-rag
```

### 2️⃣ Create and activate virtual environment (recommended)
```
python3 -m venv rag_env
source rag_env/bin/activate     # Linux / Mac
rag_env\Scripts\activate
```
### 3️⃣ Install dependencies
```
pip install -r requirements.txt
```
### 4️⃣ Create .env file in the project directory
```
nano .env
```
Add your API Key inside:
```
API_KEY=your_api_key_here
```
### 🚀 Run the Chatbot
```
python chatbot_using_rag.py
```
