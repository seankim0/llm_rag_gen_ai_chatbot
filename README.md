# llm_rag_gen_ai_chatbot

**One-liner summary**: A powerful AI ChatBot App that lets you chat with multiple documents using LLM and RAG

> **Note:** This is a prototype and not the actual code used in production.
> **Note:** Please reach out to me (seunghyk@tepper.cmu.edu) if you need full-stack real-world best practice.

---

## Introduction

AI ChatBotApp is a Python-based Generative AI application that allows users to interact with the content of multiple PDF files through natural language questions. It uses LangChain, OpenAI LLM, and vector stores (like Pinecone) to deliver smart, context-aware answers — based on your uploaded documents.

---

## How It Works

Here’s how the app processes your PDFs and generates responses:

### System Architecture

![AI ChatBot App Diagram]((https://raw.githubusercontent.com/seankim0/llm_rag_gen_ai_chatbot/blob/main/doc/PDF-LangChain.jpg))

Or take a look at the LangChain + RAG pipeline below:

![LangChain Workflow](attachment:811990aa-5094-4947-97b2-d0aac4deafcd:image.png)

### Step-by-Step Workflow

1. **PDF Loading**  
   - Multiple PDF files are loaded, and their text is extracted.

2. **Text Chunking**  
   - Long texts are split into smaller chunks for better processing.

3. **Text Embedding**  
   - Each chunk is converted into vector embeddings using OpenAI.

4. **Question Embedding & Semantic Search**  
   - Your question is also embedded and compared with document chunks in the vector store (like Pinecone).

5. **Answer Generation**  
   - The most relevant chunks are passed to the LLM to generate a final answer.

---

## Setup & Installation

1. Clone the repo
   ```bash
   git clone https://github.com/seankim0/llm_rag_gen_ai_chatbot.git
   cd llm_rag_gen_ai_chatbot

2. Install the required packages:
   ```bash
   pip install -r requirements.txt

3. Set your OpenAI API key:
   Create a .env file in the project root directory and add:
   ```ini
   OPENAI_API_KEY=your_secret_api_key


### Usage

1. Make sure all dependencies are installed and your API key is set.
2. Run the application using Streamlit:
   ```bash
   streamlit run app.py
3. A web browser will launch the app interface.
4. Upload one or more PDF documents.
5. Start chatting and ask questions about the content using natural language.


### Example Prompts

- "What is the main point of this document?"

- "What does the third page say about neural networks?"

- "Summarize the findings from the last section."

