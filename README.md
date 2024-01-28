# rag-intro

# Overview
Traditional LLMs can struggle with factual accuracy, especially for Question answering systems.
RAG addresses this by:
Retrieving relevant documents: A search engine identifies documents from a large corpus that are most relevant to the input query.
Augmenting LLM input: The retrieved documents are used to contextualize the query, providing relevant facts and information for the LLM to draw upon.
Generating improved output: The LLM generates text based on the combined information from the query and the retrieved documents, leading to more factually accurate and relevant responses.

#  Requirements
Document: we use databricks dolly 15k dataset from huggingface
Embedding Model: "sentence-transformers/all-MiniLM-l6-v2"
Search Engine: we use FAISS with similarity search
pre trained model : "Intel/dynamic_tinybert"
dependencies: langchain,torch,transformer,sentence-transformers & faiss

# steps we take: 
1)install dependencies
2) import library
3) load data
4) text_splitter
5) embedding model specified
6) store embedding into faiss vectorstore
7) model we use & tokenizer
8) retrival

# problem we faced
use t4 gpu ( if you use already free limit use again ) if u not use this they will show error not install torch
use big dataset ( suggest use less than 1 mb dataset )
while using faiss it take lot of time to store embedding in mine case it take 45min thats why interpret results
