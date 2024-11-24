# Content Engine Chatbot

The Content Engine Chatbot is an intelligent assistant built to interact with users and provide answers by querying relevant information from a set of documents. The chatbot is integrated into a Streamlit web interface, where users can type in questions, and the system responds by extracting information from a collection of pre-processed PDFs. This project combines document processing, natural language processing (NLP), and a user-friendly interface to create an efficient query-response system.




## Run Locally

Clone the project

```bash
  git clone https://github.com/thorbus/alemeno_assignment.git
```

Go to the project directory

```bash
  cd alemeno_assignment
```

Install dependencies

```bash
  pip install -r requirements.txt

```

Start the server

```bash
  streamlit run app.py
```


## Environment Variables

To run this project, you will need to add the following environment variables to your .env file


`HUGGINGFACEHUB_API_TOKEN=Your_access_token`




## Features



    Document Processing:
        Extracts text from PDF files using the PyPDF2 library.
        Splits the content into smaller, manageable chunks for efficient processing.

    Vector Store Integration:
        Converts text chunks into vector embeddings using SentenceTransformers.
        Stores embeddings in ChromaDB for quick similarity-based document retrieval.

    Query Engine:
        Uses a MultiQueryRetriever to fetch documents relevant to the user’s query.
        Leverages a Hugging Face language model (e.g., GPT-2) for generating context-aware responses.

    Streamlit Interface:
        Provides a simple and user-friendly web interface for users to ask questions.
        Displays a real-time conversation history between the user and the chatbot.

    Error Handling:
        Ensures the chatbot gracefully manages errors during retrieval or response generation.
        Logs critical events for debugging and maintenance.

