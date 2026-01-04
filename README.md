# Retrieval-Augmented Question Answering (RAG) System

## Overview
This project implements an end-to-end Retrieval-Augmented Generation (RAG) pipeline that answers natural language questions by grounding responses in relevant source documents. The system reduces hallucinations in large language models by combining semantic retrieval with transformer-based text generation.

Instead of relying only on a model’s internal knowledge, the system retrieves relevant document context and conditions the generated answer on that information.

---

## System Architecture
The pipeline consists of the following steps:

1. **Document Embedding**
   - Documents are converted into dense vector representations using a pretrained Sentence Transformer.

2. **Vector Indexing & Retrieval**
   - FAISS is used to index embeddings and perform fast similarity search.

3. **Query Processing**
   - User queries are embedded and matched against the FAISS index to retrieve the most relevant document chunks.

4. **Answer Generation**
   - Retrieved context is passed to a FLAN-T5 model to generate grounded answers.

---

## Technologies Used
- Python  
- PyTorch  
- Hugging Face Transformers  
- Sentence Transformers  
- FAISS  
- Google Colab (GPU)

---

## How to Run
1. Open `.ipynb` in Google Colab  
2. Enable GPU: `Runtime → Change runtime type → GPU`  
3. Run all notebook cells sequentially  
4. Modify documents or queries to test different use cases  

---

## Use Cases
- Academic and research question answering  
- Technical document search  
- Notes and report summarization  
- Analysis of hallucination in LLMs  

---

## Key Learning Outcomes
- Understanding RAG architecture  
- Working with vector databases  
- Integrating retrieval with generative models  
- Practical experimentation with LLMs  

---

## Future Improvements
- PDF and multi-document ingestion  
- Quantitative evaluation metrics  
- Advanced FAISS indexing strategies  
- Web or API-based deployment  
