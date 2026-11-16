# RAG Application

A Retrieval-Augmented Generation (RAG) application that allows users to upload documents and ask questions based on their content using Google Gemini.

## 🚀 Features

- Upload PDF, TXT, and DOCX documents.
- Split documents into smaller chunks.
- Store document embeddings in ChromaDB.
- Retrieve relevant information using similarity search.
- Generate AI-powered answers using Google Gemini.
- Interactive chat interface built with Streamlit.
- FastAPI backend for API communication.

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Frontend:** Streamlit
- **Backend:** FastAPI
- **LLM:** Google Gemini
- **Vector Database:** ChromaDB
- **Framework:** LangChain
- **Document Processing:** PyPDF

## 📁 Project Structure

```text
RAG_Application/
│
├── Backend/
│   ├── main.py
│   ├── database.py
│   ├── services.py
│   ├── requirement.txt
│   └── .gitignore
│
├── Frontend/
│   ├── frontend.py
│   └── chunking.py
│
├── .gitignore
└── README.md
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Kunalshinde2627/RAG-Application.git
```

### 2. Navigate to the Project

```bash
cd RAG-Application
```

### 3. Setup Backend

```bash
cd Backend
python -m venv myenv
```

Activate virtual environment (Windows PowerShell):

```powershell
.\myenv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirement.txt
```

### 4. Configure Environment Variables

Create a `.env` file inside the Backend folder and add your Google Gemini API key using the environment variable name expected by your application.

**Never upload your API key to GitHub.**

### 5. Run Backend

From the Backend folder:

```bash
uvicorn main:app --reload
```

Backend URL:

```text
http://127.0.0.1:8000
```

### 6. Run Frontend

Open a new terminal from the project root:

```powershell
cd Frontend
..\Backend\myenv\Scripts\Activate.ps1
```

Start Streamlit:

```bash
streamlit run frontend.py
```

## 🔗 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Check backend status |
| POST | `/collection` | Store document chunks |
| POST | `/chat` | Ask questions about documents |

## 💡 How It Works

1. User uploads a document.
2. The application extracts text from the document.
3. Text is divided into smaller chunks.
4. Chunks are stored in ChromaDB.
5. User asks a question.
6. Relevant chunks are retrieved.
7. Google Gemini generates an answer using the retrieved context.

## 👨‍💻 Author

**Kunal Shinde**

GitHub: https://github.com/Kunalshinde2627