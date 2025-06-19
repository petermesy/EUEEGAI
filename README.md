# EUEE AI Question Answering System

Welcome to the **EUEE AI Question Answering System**, a project designed to extract, structure, and provide intelligent answers to questions from the Ethiopian University Entrance Exam (EUEE), with a focus on subjects like Chemistry, Physics, and more. This repository includes tools for processing scanned PDF exams, structuring extracted text, and deploying a multi-platform QA system using Telegram, FastAPI, and Streamlit interfaces, powered by AI models like SentenceTransformers and Google Gemini.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [PDF Extraction](#pdf-extraction)
  - [Text Structuring](#text-structuring)
  - [QA System Deployment](#qa-system-deployment)
    - [Telegram Bot](#telegram-bot)
    - [FastAPI Backend](#fastapi-backend)
    - [Streamlit App](#streamlit-app)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Overview
This project leverages OCR (Optical Character Recognition) to extract questions from scanned EUEE PDFs, structures them into a clean JSONL format, and uses AI to provide answers via multiple interfaces. The system is designed to support educational assistance for students preparing for the EUEE, with an initial focus on Chemistry (2002-2010) and plans to expand to other subjects.

## Features
- **PDF Extraction**: Converts scanned PDF exam papers to text using Tesseract OCR and Poppler.
- **Text Structuring**: Parses and cleans OCR output into structured JSONL files with questions, options, answers, and explanations.
- **QA Engine**: Utilizes SentenceTransformers for vector search and Google Gemini for generating detailed answers.
- **Multi-Platform Support**:
  - **Telegram Bot**: Interactive bot for real-time question answering.
  - **FastAPI Backend**: RESTful API for programmatic access.
  - **Streamlit App**: Web-based interface for user queries.
- **Robust Handling**: Includes error logging, preprocessing for OCR, and confidence scoring for structured data.
- **Ethiopian Context**: Supports English and Amharic OCR, with years in Ethiopian Calendar format (e.g., 2002/03 EC).

## Installation

### Prerequisites
- Python 3.8+
- Git (for cloning the repository)

### Dependencies
Install the required Python packages:
```bash
pip install pytesseract pdf2image pillow sentence-transformers google-generativeai python-dotenv python-telegram-bot fastapi uvicorn streamlit
