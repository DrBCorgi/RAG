# RAG

This Python application uses advanced machine learning models to provide answers to questions based on the content of an uploaded PDF file. It utilizes Hugging Face's Transformers for embeddings, Faiss for efficient similarity search, and Streamlit for a user-friendly interface.

Features
PDF Processing: Load and process text data from PDF files.
Embeddings Creation: Generate embeddings for text data to facilitate semantic search.
Question Answering: Respond to user queries by finding relevant information in the PDF.
Streamlit Interface: A web interface that allows users to upload PDFs, input questions, and view answers.

Requirements
Python 3.8+
Pandas, Numpy, Faiss, Pickle, Streamlit
Hugging Face Transformers

Installation
Clone the repository:
bash
Copy code
git clone <repository-url>
Install required packages:
bash
Copy code
pip install pandas numpy faiss-cpu streamlit transformers

Usage
Setting Up the Model
Before running the application, ensure the model is correctly set in the code. The model path needs to be specified manually in the code for the LlamaCPP class:

python
Copy code
llm = LlamaCPP(
    model_path="C:/path/to/your/model/file",
    # Other parameters...
)
Running the Streamlit Application
Start the Streamlit application:

streamlit run your_script_name.py
Upload Model File: When prompted, upload the model file through the Streamlit interface. This step must be done each time the application is restarted.

Upload PDF File: Upload the PDF you want to query.

Input Your Question: Type your question into the text box and submit.

View Answers: The application processes your question and displays the most relevant answers extracted from the PDF.

Notes
Model Path: Ensure the model path in the code is correct before running the application. Streamlit will also require you to select the model file through its interface each time for security reasons.

File Types: Currently, only PDF files are supported for querying.

Troubleshooting
If you encounter errors related to model loading, verify that the model path is correct and accessible.
