# **RAG PDF Query System**

## **Overview**  
The **RAG PDF Query System** is an interactive tool that leverages Retrieval-Augmented Generation (RAG) techniques to enable users to upload PDF documents, process their content, and retrieve relevant information through natural language queries. The system integrates modern AI-powered language models and vector databases to deliver accurate and context-aware responses, making it an invaluable resource for research, documentation analysis, and automated query resolution.

---

## **Features**  

- **PDF Upload and Processing**:  
  Easily upload and process PDF documents to extract and analyze their content.  

- **Text Splitting and Chunking**:  
  Breaks large text documents into manageable chunks for better embedding and retrieval performance.  

- **Embedding Generation**:  
  Uses advanced embedding models (e.g., `OllamaEmbeddings`) to encode document content into a vectorized format for efficient retrieval.  

- **Conversational Query System**:  
  Allows multi-turn interactions using a conversational retrieval chain powered by state-of-the-art language models.  

- **Interactive GUI**:  
  A user-friendly interface built with `Tkinter` for seamless file upload, query input, and response visualization.  

---

## **Technologies and Libraries Used**

### **Core Libraries**
1. **[LangChain](https://python.langchain.com/)**  
   - Used for building the RAG pipeline, including document loaders, text splitters, embedding generation, and conversational chains.  

2. **[Chroma](https://docs.trychroma.com/)**  
   - Vector database for storing and retrieving document embeddings.  

3. **[Ollama](https://ollama.com/)**  
   - Embedding and language model provider for generating document embeddings and processing queries.  
  

---

## **How It Works**  

1. **PDF Upload**:  
   Users upload a PDF file through the Path.  

2. **Processing Pipeline**:  
   - The PDF is processed using `PyPDFLoader` to extract text.  
   - Text is split into smaller chunks using `RecursiveCharacterTextSplitter`.  
   - Embeddings for the chunks are generated using `OllamaEmbeddings`.  
   - The embeddings are stored in a `Chroma` vector database.  

3. **Query Execution**:  
   - The user inputs a natural language query.  
   - The RAG pipeline retrieves relevant chunks from the vector database.  
   - The language model generates a contextually accurate response.  

4. **Response Display**:  
   The response is displayed in a scrollable text.  

---

## **Setup Instructions**  

### **Dependencies**  
Ensure you have Python 3.9+ and install the following libraries:  

```bash
pip install langchain chromadb ollama tkinter
```

### **Running the Application**  

1. Clone the repository:  
   ```bash
   git clone https://github.com/YourUsername/RAG-PDF-Query-System.git
   cd RAG-PDF-Query-System
   ```

2. Run the application:  
   ```bash
   python rag_gui.py
   ```

3. Interact with the tool:  
   - Upload a PDF file.  
   - Enter your query in the input field.  
   - View the AI-generated response in the output window.  

---

## **Use Cases**  

- Research document analysis.  
- Automated document summarization and QA.  
- Legal, academic, and business document analysis.  

## **License**  

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.  
