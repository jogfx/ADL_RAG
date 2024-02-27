# ADL_RAG

This project outlines a process for loading, processing, and querying documents using the LangChain library, with a focus on handling a specific PDF document related to the dorm where i live,  Aalborghus kollegiet. The process involves the following steps:

**Loading a PDF Document:** The PyPDFLoader is used to load a PDF document from a specified path. This PDF is intended to contain information about Aalborghus kollegiet.

**Document Splitting:** The loaded document is then split into smaller chunks of text using a RecursiveCharacterTextSplitter to manage text size and overlap, facilitating more manageable processing and embedding.

**Database and Embedding Setup:** A LanceDB database is then set up at a specified URI and uses HuggingFaceEmbeddings for generating embeddings of the text chunks. These embeddings are crucial for enabling semantic search within the document contents.

**Document Indexing in LanceDB:** The texts are indexed in the LanceDB database, creating a searchable repository of document chunks based on their embeddings.

**Retrieval Setup:** The setup includes creating a retriever that can search through the indexed texts based on semantic similarity to a given query.

**Query Processing:** The code demonstrates how to process a user query (in this example: "Tell me where I can find the cinema") by searching the indexed texts for the most relevant information. The search results are then concatenated to form a context that can be used to generate a response to the user's query using a generative model.

This workflow exemplifies how to use LangChain and LanceDB for document loading, processing, embedding, indexing, and querying to retrieve relevant information from a corpus of documents, specifically targeting queries related to content within Aalborghus kollegiet document.
