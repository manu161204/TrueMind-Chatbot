# 🧠 TrueMind AI – RAG-Based Mental Health Chatbot

TrueMind AI is a **Retrieval-Augmented Generation (RAG)** based Mental Health Chatbot that provides grounded, reliable, and context-aware responses using **authoritative mental health PDF documents** instead of relying solely on an LLM's internal knowledge.

The chatbot retrieves relevant information from a curated knowledge base, then uses the **Groq LLM API** to generate accurate responses with a significantly lower hallucination rate. It also incorporates safety constraints and crisis-aware response handling for responsible AI-assisted mental health support.

> **Note:** This chatbot is designed for **educational and informational purposes only** and should not be considered a substitute for professional medical advice, diagnosis, or treatment.

---

## 🚀 Features

* 📚 Retrieval-Augmented Generation (RAG)
* 🧠 Semantic search using Sentence-BERT (SBERT)
* ⚡ Fast vector retrieval using FAISS
* 🤖 LLM response generation using Groq API
* 📄 Knowledge grounded in curated mental health PDF documents
* 🛡️ Reduced hallucination through document retrieval
* 🔍 Source-aware response generation
* 🚨 Crisis-aware response handling

---

## 🛠️ Tech Stack

* **Language:** Python
* **Framework:** LangChain
* **Embedding Model:** Sentence-BERT (SBERT)
* **Vector Database:** FAISS
* **LLM:** Groq API
* **Document Loader:** PyPDF
* **Knowledge Source:** Curated Mental Health PDFs

---

## 📂 Project Structure

```text
TrueMind-AI/
│
├── app.py
├── chatbot.py
├── vector_store.py
├── requirements.txt
├── documents/
│   └── mental_health.pdf
├── assets/
└── README.md
```

---

# ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/TrueMind-AI.git
cd TrueMind-AI
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🔑 Configure the Groq API Key

This project uses the **Groq API** for LLM inference.

### Step 1

Create a free account on **Groq Cloud**.

https://console.groq.com/

### Step 2

Generate an API Key.

### Step 3

Open the project and locate the line where the Groq API key is initialized.

Replace the placeholder with your own API key.

```python
GROQ_API_KEY = "YOUR_GROQ_API_KEY"
```

or, if your project uses environment variables:

```python
os.environ["GROQ_API_KEY"] = "YOUR_GROQ_API_KEY"
```

> **Never commit your personal API key to GitHub.**

---

# 📄 Add Your PDF Knowledge Base

The chatbot answers questions **only from the PDF document provided by you**.

Replace the document path with the location of your own PDF.

Example:

```python
pdf_path = "documents/mental_health.pdf"
```

or

```python
loader = PyPDFLoader("C:/Users/YourName/Documents/mental_health.pdf")
```

Simply update this path to your desired PDF file before running the project.

You can replace the default PDF with any domain-specific document to build your own RAG chatbot.

Examples:

* Medical Guidelines
* Legal Documents
* Research Papers
* Company Policies
* Educational Books

---

# ▶️ Run the Project

```bash
python app.py
```

or

```bash
streamlit run app.py
```

(depending on your implementation)

---

# 🧠 How It Works

1. User enters a query.
2. The PDF is processed and split into chunks.
3. SBERT converts each chunk into vector embeddings.
4. FAISS stores and retrieves the most relevant chunks.
5. Retrieved context is combined with the user's question.
6. Groq LLM generates a grounded response.
7. The chatbot returns an accurate answer based on the retrieved documents.

---

# 📈 Advantages

* Lower hallucination compared to standalone LLMs
* Grounded responses from trusted documents
* Faster semantic retrieval using FAISS
* Easy to customize with your own PDFs
* Modular RAG pipeline
* Suitable for educational and research purposes

---

# 📌 Future Improvements

* Multi-PDF support
* Cloud vector database
* Conversation memory
* Multilingual support
* Citation highlighting
* Web interface deployment
* User authentication
* Continuous document updates

---

# 🤝 Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Open a Pull Request.

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Manu Gaur**

B.Tech Computer Science (AI & ML)

SRM Institute of Science and Technology

---

⭐ If you found this project useful, consider giving it a **Star** on GitHub!
