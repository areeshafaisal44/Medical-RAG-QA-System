# Medical-RAG-QA-System — LangChain + Chroma + Gemini/OpenAI

## Overview
This project builds a Retrieval-Augmented Generation (RAG) pipeline using the Kaggle "medical transcriptions" dataset and LangChain. It supports Chroma vector store and two LLM backends: Vertex AI (Gemini) and OpenAI. Also includes a Streamlit and a Gradio demo.

## Contents
- `notebook_colab.ipynb` — full Colab notebook (recommended)
- `src/rag_pipeline.py` — reusable script to create vector store and run queries
- `src/app_streamlit.py` — Streamlit demo to query the RAG system
- `src/evaluation.py` — evaluation suite (precision@k, ROUGE, sample outputs)
- `docs/evaluation_report.md` — template report

## Quickstart (Colab)
1. Open `notebook_colab.ipynb` in Google Colab.
2. Upload `kaggle.json` (Kaggle API token) and run the Kaggle download cell, or upload `mtsamples.csv`.
3. Set up the LLM backend: OpenAI (set `OPENAI_API_KEY`) or Vertex AI (set `GOOGLE_APPLICATION_CREDENTIALS`).
4. Run notebook cells sequentially.

## Demo deployment
- Streamlit Cloud: Run the link using `(https://6f40ccea813f4b72b1.gradio.live/)`. Requires setting secrets for API keys.

## Evaluation
- Use `` to compute retrieval and generation metrics on a set of 30+ queries.

## License & Acknowledgements
Dataset: Kaggle — tboyle10/medicaltranscriptions.
