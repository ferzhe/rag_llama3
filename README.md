# 🧠 RAG with LangChain and Llama 3 Hugging Face

This notebook demonstrates a **Retrieval-Augmented Generation (RAG)** pipeline using **LangChain** and the **LLaMA 3** model from Hugging Face. Optimized for GPU execution with **4-bit quantization**, it leverages open-source tools to provide a cost free platform for learning and experimenting with RAG.

---

## 📄 Data Description

The pipeline processes a PDF dataset (`data/rendang.pdf`) that explores **Indonesia’s culinary heritage**, focusing on **rendang**, a traditional Minangkabau dish.

The PDF is sourced from the following article:

> **"Rendang: The treasure of Minangkabau"**  
> Muthia Nurmufida, Gervasius H. Wangrimen, Risty Reinalta, Kevin Leonardi  
> *Journal of Ethnic Foods*, Volume 4, Issue 4, 2017, Pages 232–235  
> [https://doi.org/10.1016/j.jef.2017.10.005](https://doi.org/10.1016/j.jef.2017.10.005)

This dataset serves as the **primary retrieval source**, complemented by **real-time Wikipedia summaries** to deliver accurate answers about Indonesian cuisine’s cultural and historical significance.

---

## ✨ Features

### 🧠 LLaMA 3 (8B) via Hugging Face
- Text generation using `glaiveai/Llama-3-8B-RAG-v1`
- Efficient inference with **4-bit quantization** using `bitsandbytes`

### 📚 ChromaDB Vector Store
- Embeds and indexes PDF content with `sentence-transformers/all-MiniLM-L6-v2`
- Enables fast, semantic similarity search over document chunks

### 🌐 Wikipedia Integration
- Retrieves real-time external knowledge via `WikipediaQueryRun` from LangChain

### 🧱 LangChain Framework
- Manages **document loading**, **text splitting**, **embedding**, **retrieval**, and **prompt construction** end-to-end