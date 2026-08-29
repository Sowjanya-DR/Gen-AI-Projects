# Coachbot

A multimodal GenAI assistant for technical interview prep, resume review,
and study help. Built with LangChain, LangGraph, and FAISS. Streamlit is
the main UI, FastAPI is there as a backend for anyone who wants to build
a separate frontend against it later.

Upload a resume, notes, or a screenshot, and ask questions. Requests get
routed to one of four agents depending on what you're asking:

- Mentor: resume feedback, interview questions, career advice
- Document agent: answers based on whatever you've uploaded
- Reasoning agent: coding/architecture/algorithm problems, step by step
- Well-being agent: stress and motivation check-ins

## Requirements
- Python 3.12
- Tesseract OCR, only needed if you plan to upload screenshots/images:
  - Windows: [UB-Mannheim build](https://github.com/UB-Mannheim/tesseract/wiki), add it to PATH
  - macOS: `brew install tesseract`
  - Linux: `sudo apt-get install tesseract-

## Setup


bash
python -m venv .venv
.venv\Scripts\activate        # Windows
source .venv/bin/activate     # macOS/Linux

pip install -r requirements.txt
cp .env.example .env
