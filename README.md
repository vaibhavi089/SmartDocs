# 📄 SmartDocs — Chat with Your PDF

Welcome to **SmartDocs**, a powerful Streamlit-based application that allows you to **chat with your PDF files** using **Google Gemini** and **LangChain**.

🔗 **Live App**: [https://smartdocss.streamlit.app](https://smartdocss.streamlit.app)

---

## ✨ Features

- 📥 Upload one or multiple PDF documents
- 🔍 Automatically extracts and chunks the content
- 🧠 Embeds text using Google Embeddings and stores them in FAISS
- 💬 Ask questions and get context-aware answers using **Gemini 1.5 Flash**
- 📌 Provides accurate responses only from the document — no hallucinations

---

## 🛠 Tech Stack

- Python
- Streamlit
- LangChain
- Google Gemini (Generative AI)
- GoogleGenerativeAIEmbeddings
- FAISS
- PyPDF2
- dotenv

---

## 📦 Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/smartdocs.git
   cd smartdocs
   ```

2. **Create Virtual Environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
4. **Add Your Google API Key**
   Create a .env file in the root folder and add:
   ```bash
   GOOGLE_API_KEY=your_google_api_key_here
   ```
5. **Run the App**
   ```bash
   streamlit run app.py
   ```
---

## 📂 Project Structure
```bash
smartdocs/
├── app.py                  # Main Streamlit application
├── requirements.txt        # Python dependencies
├── .env                    # Environment variable for Google API key
├── faiss_index/            # Auto-generated vector store directory
└── README.md               # Project overview and usage
```

## ⚙️ How It Works

1. **Upload PDFs via the sidebar.**
2. The app **extracts text using PyPDF2**.
3. Text is **split into chunks** using LangChain’s `RecursiveCharacterTextSplitter`.
4. Chunks are **embedded using GoogleGenerativeAIEmbeddings** and **stored in FAISS**.
5. When a user asks a question:
   - 🔍 **Relevant chunks are retrieved** from FAISS based on semantic similarity.
   - 🧠 The **context and question** are passed to **Gemini 1.5 Flash**.
   - 📌 The model **returns a detailed, grounded answer** based strictly on the provided content.

## 📍 Try It Live!
🚀 Deployed App: https://smartdocss.streamlit.app

## 🙋‍♀️Author
Vaibhavi Katiyar
- Github: @vaibhavi089
- linkedin: https://linkedin.com/vaibhavi-katiyar/
  


         
   
