# Chatbot with PDF Embedding and Querying

This project is a chatbot application that allows users to upload PDF files, create embeddings from the PDF content, store them in a Chroma vector store, and query the database using natural language queries. The chatbot uses the LangChain library for document processing and the Flask framework for the web interface.

## Project Structure

```
.
├── __pycache__/
├── .gitignore
├── app.py
├── data/
├── get_embedding_function.py
├── populate_database.py
├── query_data.py
├── README.md
├── requirements.txt
├── static/
│   └── style.css
├── templates/
│   ├── index.html
│   └── upload.html
└── test_rag.py
```

## Setup

1. **Clone the repository:**

    ```sh
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Install dependencies:**

    ```sh
    pip install -r requirements.txt
    ```

3. **Run the application:**

    ```sh
    python app.py
    ```

## Usage

### Upload PDF Files

1. Navigate to the [`/upload`] route in your browser.
2. Upload a PDF file using the provided form.
3. The application will process the PDF, create embeddings, and store them in the Chroma vector store.

### Query the Database

1. Navigate to the root route [`/`] in your browser.
2. Use the chat interface to ask questions based on the uploaded PDF content.
3. The chatbot will respond with answers based on the context extracted from the PDFs.

## Code Overview

### [`app.py`]

- **Routes:**
  - [`/upload`]: Allows users to upload PDF files.
  - [`/`]: Main chat interface.
- **Functions:**
  - [`create_database_based_on_pdf_files()`]: Reads PDF files, creates embeddings, and stores them in Chroma.
  - [`query_rag(query_text: str)`]: Queries the Chroma database and generates responses.

### [`populate_database.py`]

- Imports necessary modules and functions for processing PDFs and creating embeddings.

### [`query_data.py`]

- Contains functions to query the Chroma database using natural language queries.

### [`get_embedding_function.py`]

- Provides the function to generate embeddings from text.

### Templates

- **[`templates/upload.html`]**: HTML template for the PDF upload page.
- **[`templates/index.html`]**: HTML template for the chat interface.

### Static Files

- **[`static/style.css`]**: CSS file for styling the web pages.

## License

This project is licensed under the MIT License.


