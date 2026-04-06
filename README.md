# Summarizer-HF

A full-stack Natural Language Processing (NLP) application that generates concise summaries from long conversations, articles, or dialogue using a fine-tuned T5 Transformer model.
Built with a FastAPI backend and a clean, interactive web interface for real-time summarization.

# Objective

Reading long conversations or documents is time-consuming and inefficient.
This project solves that problem by building an end-to-end AI-powered summarization system that transforms lengthy text into short, meaningful, and human-readable summaries.

The goal was not just to train a model, but to:

Deploy it in a real-world application
Build a complete ML pipeline
Make NLP accessible through a simple web interface

# Project Highlights

#### Fine-tuned T5 Transformer for high-quality abstractive summarization
#### FastAPI backend with REST endpoint (POST /summarize/)
#### Interactive Web UI — paste text → click → get summary instantly
### Text preprocessing pipeline:
* Removes HTML tags
* Normalizes whitespace
* Converts to lowercase
#### Beam Search Decoding (num_beams=4) for improved output quality
#### Pre-trained model stored locally — no retraining required
#### Device-aware inference:
* Apple Silicon (MPS)
* GPU (CUDA)
* CPU fallback

# Model Details

**Architecture:** T5 (Text-To-Text Transfer Transformer)
**Task:** Abstractive Text Summarization
**Training:** Fine-tuned on dialogue/conversation dataset
**Decoding Strategy:** Beam Search
* num_beams = 4
* early_stopping = True
**Input Limit:** 512 tokens
**Output Limit:** 150 tokens
**Model Path:** ./saved_summary_model/

# How It Works
1. User inputs long text or dialogue
2. Text is cleaned and preprocessed
3. Tokenizer converts text → tokens
4. T5 model generates summary using beam search
5. Output tokens are decoded into readable summary

# Getting Started
1. Clone the Repository
git clone https://github.com/Sanket73/TextSummarizerApp
cd text-summarizer
2. Install Dependencies
pip install -r requirements.txt
3. Run the Application
uvicorn app:app --reload
4. Open in Browser
http://localhost:8000

Paste your text and click **Summarize**