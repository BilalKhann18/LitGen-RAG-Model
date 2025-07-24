📚 GenAI Literature Review Assistant (RAG System)
This project is an end-to-end Retrieval-Augmented Generation (RAG) pipeline developed as part of the Generative AI module in the MSc Business Analytics programme at Warwick Business School. It demonstrates how unstructured academic content can be transformed into an interactive, explainable, and semantically searchable knowledge system using modern GenAI techniques.

The system is designed to automate literature reviews by integrating document processing, vector-based retrieval, and LLM-powered generation — producing citation-backed, context-grounded responses in real time.

🧠 Project Overview
The application begins with a corpus of academic PDFs, which are parsed and split using a hybrid chunking approach. Documents are first segmented semantically via Markdown-style headers, followed by recursive character-based splitting with overlap to preserve context. These chunks are embedded using OpenAI’s embedding models (e.g., text-embedding-3), and stored in a ChromaDB vector database optimised for cosine similarity search.

At inference time, the system retrieves relevant chunks using a hybrid retrieval approach (dense similarity + score filtering) and passes them into a custom LLM prompt pipeline built on LangChain. The prompts are designed to:

Reformulate vague queries into precise alternatives

Extract key supporting facts from the retrieved context

Generate answers with inline citations

Self-evaluate output confidence via context alignment, keyword overlap, and evidence quality scoring

The final output is served through a Gradio-based interface that allows users to input natural language questions and receive grounded, reference-linked answers — similar to what a human researcher might produce.

💡 Broader Implications
While the initial use case focused on automating academic literature reviews, the architecture is domain-agnostic. With minimal adaptation, it can be deployed for:

Legal and compliance document summarisation

Financial report and market data synthesis

HR policy and onboarding support

Enterprise knowledge base querying

Any domain that relies on trust, traceability, and structured insight from large volumes of text stands to benefit from this architecture.

🔍 Key Components
LangChain-based pipeline: Handles prompt templating, document ingestion, and conversational memory

OpenAI Embeddings + GPT-4o-mini: Embeds chunks and generates grounded responses

ChromaDB vector store: Stores and retrieves semantically indexed document chunks

Confidence Scoring Module: Quantitatively evaluates context coverage, answer alignment, and citation quality

Gradio UI: Front-end chat interface for end-user interaction

🧪 Learning Outcomes
This project was my first deep dive into GenAI systems. It pushed me to move beyond theory and develop a working application that combines multiple layers of the modern NLP stack — from data preparation and retrieval to prompt design and evaluation. More importantly, it gave me a solid grasp of how GenAI can be used not just to generate language, but to enable structured reasoning over knowledge.
