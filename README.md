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

## Project Architecture Diagram

![Summarizer-HF Architecture](https://github.com/Sanket73/TextSummarizerApp/blob/main/Image.png?raw=true)

## 🎥 TextSummarizer in Action
https://github.com/user-attachments/assets/32ecc5df-39bb-49e5-a6e7-ea090d942bd2

# Tech Stack

### Backend
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Uvicorn](https://img.shields.io/badge/Uvicorn-4051B5?style=flat&logo=gunicorn&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white)

---

### Frontend
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

---

### Machine Learning
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21F?style=flat&logo=huggingface&logoColor=black)
![T5](https://img.shields.io/badge/T5_Model-FF6F00?style=flat&logo=google&logoColor=white)

---

### Other Tools
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)
![VSCode](https://img.shields.io/badge/VS_Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white)

# Future Improvements
* Support multiple models (T5, BART, Pegasus)
* Adjustable summary length (user control slider)
* File upload support (.txt, .pdf)
* Multilingual summarization
* Docker containerization for deployment
* Add evaluation metrics (ROUGE scores)
* Interactive API docs (Swagger UI improvements)


# Conclusion

This project demonstrates a complete machine learning lifecycle:

Model fine-tuning (Jupyter Notebook)
Backend deployment (FastAPI)
Frontend integration (Web UI)

It bridges the gap between AI research and real-world application, making powerful NLP models accessible through a simple browser interface.

# Author

Sanket Dongardive

GitHub: https://github.com/Sanket73

LinkedIn: https://linkedin.com/in/sanket-dongardive-515793315
