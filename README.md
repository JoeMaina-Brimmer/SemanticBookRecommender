Semantic Book Recommender — README
A small project that builds a semantic book recommender using OpenAI embeddings, LangChain for retrieval, pandas / numpy for data analysis, and a Gradio dashboard for interactive use. The pipeline ingests a Kaggle books/dataset, preprocesses it, builds vector embeddings, stores them in a vector store, and exposes a conversational / search-style recommender through a Gradio UI.
Project overview
This repo demonstrates how to build a content-based, semantic book recommender — instead of relying on metadata or co-purchases only, it uses natural language embeddings of book descriptions, or other text to find semantically similar books. You can ask natural-language queries (e.g., "a book about romance") and get recommended books that match the semantics of that request.
Features
Ingest Kaggle book dataset (metadata, descriptions)
Preprocess (clean, filter, chunk long descriptions)
Build embeddings for items with OpenAI embeddings
Store embeddings in a vector store (Chroma)
HuggingFace transformers all-MiniLM-L6-v2 
Use LangChain for similarity search
Light-weight analytics with pandas/numpy (top genres, tone distributions)
Interactive Gradio UI for query → recommendations

Create virtual env and install:
python -m venv venv
source venv/bin/activate       
pip install -r requirements.txt

Environment variables
Create a .env file or set these in your environment:
OPENAI_API_KEY — your OpenAI API key

If you use a .env file, use python-dotenv to load it in scripts:
OPENAI_API_KEY=sk-xxxx
HUGGINGFACEHB_API_TOKEN=your_kaggle_user