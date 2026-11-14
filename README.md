# Gemini Drive Assistant

A Streamlit application that connects to **Google Drive** and answers natural-language questions about the documents stored there, using the **Google Gemini** API.

## How it works

1. **`drive_connector.py`** — authenticates against Google Drive via OAuth, lists and fetches files, and extracts text from PDFs (PyPDF2) and Word documents (python-docx).
2. **`gemini_query.py`** — builds the query context from the extracted document text and calls the Gemini API to generate an answer.
3. **`app.py`** — Streamlit front end with a dark theme, file browser, and chat interface.
4. **`config.py`** — API keys and runtime configuration, loaded from the environment via python-dotenv.

## Setup

```bash
pip install -r requirements.txt
```

Create a `.env` file with your credentials:

```
GEMINI_API_KEY=your_key_here
GOOGLE_CREDENTIALS_PATH=path/to/credentials.json
```

Then run:

```bash
streamlit run app.py
```

## Stack

Streamlit · Google Gemini API · Google Drive API · OAuth 2.0 · PyPDF2 · python-docx
