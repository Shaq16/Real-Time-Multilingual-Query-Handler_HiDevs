🚀 Real-Time Multilingual Query Handler

A robust Retrieval-Augmented Generation (RAG) system that breaks language barriers.
This application allows users to ask customer support questions in any language, automatically:

Detects the language

Translates user input to English

Searches a custom multilingual knowledge base

Generates an accurate response

Translates the answer back to the user’s preferred language

📸 Application Screenshots
1. Main Interface

A simple chat UI where users ask questions in their native language.
<img width="1919" height="939" alt="image" src="https://github.com/user-attachments/assets/96db269b-4bf2-45c1-82fa-b74c40f6b3ad" />
2. Multilingual Response Example

The system detects Hindi → translates → retrieves context → answers → translates back to Hindi.

✨ Features

🌍 Language Agnostic — Supports 7+ languages (Spanish, French, Hindi, Chinese, Arabic, German, etc.)

⚡ Ultra-Fast Inference — Powered by Groq Llama-3.3 models via Groq API

🔎 RAG Pipeline — Uses ChromaDB + sentence-transformer embeddings to return accurate answers

🔄 Real-Time Translation — Automatic translation of user queries and responses

📖 Transparent Debug Info — Shows detected language, translated text, and context documents

🧠 Chat Memory — Maintains conversation history for follow-up questions

🏗️ Modular Code Structure — Easy to update, extend, and maintain

🖥️ Streamlit UI — Clean and responsive frontend

🧰 Tech Stack
Frontend

Streamlit

Backend

Python 3.10+

Groq API (Llama-3.3-70b-versatile)

Sentence-Transformers (all-MiniLM-L6-v2)

ChromaDB (Vector Search)

LangChain (Orchestration)

📂 Project Structure
multilingual-query-handler/
│
├── data/
│   ├── raw/            # Raw text files for knowledge base
│   ├── processed/      # Cleaned data
│   └── chunks/         # Chunked text
│
├── src/
│   ├── config.py           # API keys & model configs
│   ├── data_collection.py  # PDF/Text/Web loaders
│   ├── preprocessing.py    # Cleaning pipeline
│   ├── chunking.py         # Splitting text into chunks
│   ├── embeddings.py       # Embedding & vector store management
│   ├── translation.py      # Translation logic using Groq
│   └── query_engine.py     # Core RAG logic
│
├── ui/
│   └── app.py              # Streamlit chat frontend
│
├── tests/
│   ├── test_translation.py
│   ├── test_query.py
│   └── test_pipeline.py
│
├── main.py                 # Build knowledge base pipeline
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation

🛠️ Installation & Setup
1. Clone the Repository
git clone https://github.com/your-username/Real-Time-Multilingual-Query-Handler.git
cd Real-Time-Multilingual-Query-Handler

2. Create Virtual Environment
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows

3. Install Dependencies
pip install -r requirements.txt

4. Add API Keys (.env)

Create a .env file:

GROQ_API_KEY=your_key_here
MONGODB_URI=your_mongo_uri

🧩 Building the Knowledge Base

Run the pipeline to clean → chunk → embed → store data:

python main.py

💬 Run the Chat Interface
streamlit run ui/app.py


Then open the displayed URL to start chatting.

🧠 How the System Works

1. Input Detection
Auto-detects language using Groq models.

2. Translation to English
Ensures knowledge base consistency.

3. Vector Search (RAG)
Uses ChromaDB + embeddings.

4. Answer Generation
LLM constructs the final response.

5. Translate Back to User Language
Ensures localized output.

🧪 Running Tests
pytest tests/

🤝 Contributing

Pull requests are welcome!
Feel free to improve translations, model selection, or add features.

📜 License

This project is licensed under the MIT License.

🌟 Acknowledgments

Groq for blazing fast inference

LangChain & Sentence-Transformers

Streamlit for UI simplicity
