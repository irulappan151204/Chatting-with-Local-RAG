# **RAG PDF Query System**

## **Overview**  
The **RAG PDF Query System** is an interactive tool that leverages Retrieval-Augmented Generation (RAG) techniques to enable users to upload PDF documents, process their content, and retrieve relevant information through natural language queries. The system integrates modern AI-powered language models and vector databases to deliver accurate and context-aware responses, making it an invaluable resource for research, documentation analysis, and automated query resolution.

---

## **Features**  

### **PDF Upload and Processing**  
- Extract text from PDF documents efficiently.  

### **Text Splitting and Chunking**  
- Break large text documents into manageable chunks to optimize embedding generation and retrieval performance.  

### **Embedding Generation**  
- Leverage advanced embedding models (e.g., `OllamaEmbeddings`) to encode document content into a vectorized format for efficient storage and retrieval.  

### **Conversational Query System**  
- Enable multi-turn conversations with users using a **ConversationalRetrievalChain**.  
- Provide intelligent, context-aware responses powered by state-of-the-art language models.

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
   Users can upload a PDF file through the specified path.  

2. **Processing Pipeline**:  
   - The PDF is processed using `PyPDFLoader` or `pdfplumber` to extract text.  
   - The extracted text is split into smaller chunks using `RecursiveCharacterTextSplitter`.  
   - Embeddings for the text chunks are generated using `nomic-embed-text`.  
   - The embeddings are stored in a `Chroma` vector database for efficient retrieval.  

3. **Query Execution**:  
   - Users input a natural language query.  
   - The Retrieval-Augmented Generation (RAG) pipeline retrieves relevant chunks from the vector database.  
   - A language model processes the retrieved chunks to generate a contextually accurate and relevant response.  

4. **Response Display**:  
   The generated response is displayed in a user-friendly, scrollable text interface for easy reading.  

---

## **Getting Started**  

### **Prerequisites**  
1. Install Python 3.10 or later.  
2. Install the required libraries:  
   ```bash
   pip install langchain chromadb ollama pdfplumber
   ```  

### **Steps to Run**  
1. Clone the repository:  
   ```bash
   git clone <repository-url>
   ```  
2. Navigate to the project directory:  
   ```bash
   cd <project-directory>
   ```  
3. Add your PDF files to the `/data` folder.  
4. Run the notebook or Python script to start processing and querying

---

## **Use Cases**  

- Research document analysis.  
- Automated document summarization and QA.  
- Legal, academic, and business document analysis.  

## **License**  

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.  
