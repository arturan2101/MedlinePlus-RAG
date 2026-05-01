# MedlinePlus RAG Health Assistant

A Retrieval-Augmented Generation (RAG) chatbot for medical Q&A, built entirely in Python on Google Colab.

## How it works
Medical articles from MedlinePlus XML data are parsed, embedded using sentence transformers, 
and stored in a FAISS vector index. User queries are matched semantically to relevant 
articles, which are then passed as context to a local LLM for answer generation.

## Stack
| Component | Technology |
|---|---|
| Language | Python |
| Embeddings | HuggingFace `all-mpnet-base-v2` |
| Vector search | FAISS |
| LLM | Qwen 2.5-0.5B-Instruct (local) |
| Interface | Gradio |
| Environment | Google Colab |

## Features
- Semantic search over 1000+ MedlinePlus medical articles
- Local LLM inference — no external API calls
- Multi-turn chat interface via Gradio
- Zero-cost deployment on Google Colab
