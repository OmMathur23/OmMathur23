# Hey, I'm Om.

Started out just exploring CS broadly, ended up falling into Machine Learning and never really left. That pulled me into Deep Learning, and lately I've been trying to understand how modern AI systems actually work under the hood instead of just calling APIs.

Right now I'm deep in Transformers, NLP, and LLMs — worked through the theory (attention mechanisms, GPT-style architectures) and now I'm building actual retrieval-grounded apps on top of that, backend and all.

### Things I've built

- **DocuChat** — full-stack RAG app for chatting with your own documents. FastAPI backend with async SQLAlchemy + Postgres, JWT auth (Argon2 hashing), Alembic migrations, and a from-scratch RAG pipeline (chunking, embeddings, Chroma vector store) behind a Streamlit frontend

- **WhatsApp Document Validator** — WhatsApp-integrated KYC bot (Django, Flask, PaddleOCR, WhatsApp Cloud API) hitting 91% accuracy across 50+ Aadhaar/PAN documents. Containerized with Docker, automated the Meta Business Account setup; deployed via ngrok/Render

- **Document OCR API** — Flask API for structured field extraction from scanned IDs (Aadhaar, PAN, DL, Passport, cheques), with orientation correction and PDF-to-image preprocessing. Built in Aadhaar digit masking that cut compliance violations.

- **Diabetes Risk Prediction** — end-to-end ML pipeline on 229K CDC BRFSS records (AdaBoost, XGBoost, soft-voting ensemble), SMOTE to handle a 6.2:1 class imbalance across 27 engineered features, ROC-AUC of 0.8156. Calibrated the decision threshold to 0.208 for 88% diabetic-class recall; co-authored an IEEE-style paper on it

- **Silmarillion RAG** — RAG chatbot over Tolkien's *The Silmarillion*, built from scratch with no LangChain/LlamaIndex: sentence-aware chunking (345 chunks, 99.4% clean boundaries), 768-dim Gemini embeddings in Chroma with cosine similarity, retry/backoff across all 345 embedding calls with zero data loss, grounded top-5 retrieval + generation with source citations, deployed on Streamlit

- **Character-level GPT** — a from-scratch transformer implementation, trained on and generating Silmarillion-style text

- **Reimplemented Micrograd**

> Learning by building.
