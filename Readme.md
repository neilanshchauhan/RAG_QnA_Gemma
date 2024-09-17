# Gemma Document Q&A Application

## Try the App

You can try out the deployed app here [https://ragqnagemma-aecqs2hkutn4pwkfx9z4so.streamlit.app/](https://ragqnagemma-aecqs2hkutn4pwkfx9z4so.streamlit.app/)

## Overview

The Gemma Document Q&A application allows users to upload PDF documents and interact with them using a question-answering model. Built with Streamlit and leveraging various AI and machine learning tools, this application enables efficient retrieval and processing of document content based on user queries.

## Features

- **PDF Upload:** Allows users to upload PDF files.
- **Document Embedding:** Converts PDF content into vector embeddings for efficient retrieval.
- **Contextual Q&A:** Uses a Groq-based language model to answer questions based on the provided document context.
- **Document Similarity Search:** Displays similar document content in the sidebar for better context understanding.

## Setup

### Prerequisites

- Python 3.9 or higher
- A virtual environment (recommended)

### Installation

#### 1. Clone the Repository:

```bash
git clone https://github.com/neilanshchauhan/RAG_QnA_Gemma.git
cd RAG_QnA_Gemma
```

#### 2. Setup

#### With Docker

1. Create a `.env` file in the root directory of your project and add your API keys:
   ```plaintext
   GOOGLE_API_KEY=<your_google_api_key>
   GROQ_API_KEY=<your_groq_api_key>
   ```
2. Build the Docker image:
   ```bash
   docker build -t gemma-doc-qa .
   ```
3. Run the Docker container:
   ```bash
   docker run --env-file .env -p 8501:8501 gemma-doc-qa
   ```

---

#### Without Docker

**Set Up a Virtual Environment:**
**For Windows:**

```bash
python -m venv env
env\Scripts\activate
```

**For macOS/Linux:**

```bash
python -m venv env
source env/bin/activate
```

#### 3. Install Dependencies:

```bash
pip install -r requirements.txt
```

#### 4. Configure API Keys:

Create a `.env` file in the root directory of your project and add your API keys:

```plaintext
GOOGLE_API_KEY=<your_google_api_key>
GROQ_API_KEY=<your_groq_api_key>
```

#### 5. Run the Streamlit App:

Start the Streamlit application with:

```bash
streamlit run app.py
```

### Usage

1. **Upload a PDF:**

   Navigate to the application in your web browser and use the file uploader to upload a PDF document.

2. **Generate Embeddings:**

   Click on "Generate Embeddings" to process the uploaded document and create vector embeddings.

3. **Ask Questions:**

   Enter your questions in the provided input field. The application will use the Groq model to provide answers based on the document content.

4. **View Document Similarity Search:**

   The sidebar will display similar document content based on the query to provide additional context.
