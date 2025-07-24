# GenAI Literature Review Assistant (RAG System)

This project is an end-to-end **Retrieval-Augmented Generation (RAG)** pipeline developed as part of the *Generative AI* module in the MSc Business Analytics programme at **Warwick Business School**. It demonstrates how unstructured academic content can be transformed into an interactive, explainable, and semantically searchable knowledge system using modern GenAI techniques.

The system is designed to automate literature reviews by integrating document processing, vector-based retrieval, and LLM-powered generation — producing **citation-backed, context-grounded responses** in real time.

---

## Project Overview

The application begins with a corpus of academic PDFs, which are parsed and split using a hybrid chunking approach. Documents are first segmented semantically via Markdown-style headers, followed by recursive character-based splitting with overlap to preserve context. These chunks are embedded using **OpenAI’s embedding models** (e.g., `text-embedding-3`), and stored in a **ChromaDB** vector database optimised for **cosine similarity** search.

At inference time, the system retrieves relevant chunks using a hybrid retrieval approach (dense similarity + score filtering) and passes them into a custom LLM prompt pipeline built on **LangChain**. The prompts are designed to:

- Reformulate vague queries into precise alternatives  
- Extract key supporting facts from the retrieved context  
- Generate answers with inline citations  
- Self-evaluate output confidence via context alignment, keyword overlap, and evidence quality scoring

The final output is served through a **Gradio** interface that allows users to input natural language questions and receive grounded, reference-linked answers — similar to what a human researcher might produce.

---

## Broader Implications

While the initial use case focused on automating academic literature reviews, the architecture is domain-agnostic. With minimal adaptation, it can be deployed for:

- Legal and compliance document summarisation  
- Financial report and market data synthesis  
- HR policy and onboarding support  
- Enterprise knowledge base querying

Any domain that relies on trust, traceability, and structured insight from large volumes of text stands to benefit from this architecture.

---

## Key Components

- **LangChain-based pipeline**: Prompt templating, document ingestion, and conversational memory  
- **OpenAI Embeddings + GPT-4o-mini**: For semantic representation and natural language generation  
- **ChromaDB vector store**: For fast, similarity-based retrieval  
- **Confidence Scoring Module**: Evaluates context coverage, answer alignment, and evidence strength  
- **Gradio UI**: Interactive front-end for end-user queries

---

## Learning Outcomes

This project was my first deep dive into GenAI systems. It pushed me to go beyond theory and build a working application that integrates multiple components of the modern NLP stack — from document parsing and semantic indexing to retrieval, prompting, and generation. Most importantly, it taught me how GenAI can be used not just for content creation, but for **evidence-based reasoning and decision support**.

---

