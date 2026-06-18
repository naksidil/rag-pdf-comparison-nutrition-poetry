# RAG PDF Comparison: Nutrition Textbook vs Poetry

This project is a PDF-based Retrieval-Augmented Generation system built in Google Colab.

It is adapted from the open-source project:

https://github.com/mrdbourke/simple-local-rag

## Project Idea

The original project builds a RAG pipeline for one factual PDF document.

In this project, I extend the pipeline by comparing two different document types:

1. **Human Nutrition PDF** — factual textbook
2. **Leaves of Grass PDF** — literary poetry collection

The main goal is to analyze how RAG behavior changes when the document type changes from factual explanatory text to literary poetic text.

## Main Modification

Original pipeline:

* One factual PDF
* Sentence-based chunking
* Factual question answering

Modified pipeline:

* Two PDF datasets
* Factual textbook vs poetry
* Sentence-based chunking for the textbook
* Line-based chunking for poetry
* Different prompts for factual and interpretive answers
* Comparison table for retrieval scores and answer styles

## Tools Used

* Python
* Google Colab
* PyMuPDF
* spaCy
* SentenceTransformers
* PyTorch
* Hugging Face Transformers
* Qwen/Qwen2.5-1.5B-Instruct
* pandas

## Results

The nutrition textbook produced direct factual answers.

The poetry dataset produced interpretation-based answers grounded in retrieved excerpts.

This shows that RAG can work on different document types, but preprocessing, chunking, and prompting should be adapted to the structure of the document.

## Files

* `RAG_Nutrition_vs_Poetry.ipynb` — main notebook
* `proposal.md` — project proposal
* `nutrition_vs_poetry_rag_comparison.csv` — comparison results
* `requirements.txt` — required libraries
