# 🔍 RAG Boilerplate - Retrieval-Augmented Generation Starter Kit

An open-source, plug-and-play LangChain-based RAG system that enables businesses to build domain-specific LLM apps using their internal documents with semantic search and natural language querying.

## 🚀 Features

### 📥 Multi-format Document Ingestion
- **Supported Formats**: PDF, CSV, TXT, DOCX
- **Embedding Pipeline**: LangChain + Qdrant
- **Metadata Tagging**: Document source, upload date, category

### 🔎 Semantic Search Engine
- Natural language query input
- Hybrid search: metadata filter + semantic match
- Returns top-K chunks with source reference

### 🤖 Chat & Q&A Agent
- **Frontend**: Streamlit interface for live Q&A
- **API**: FastAPI endpoint for LLM Q&A (POST /query)
- Shows source documents + confidence score

### 🗃️ PostgreSQL Metadata & User Access
- User management (Admin, Viewer)
- Logs user queries and file uploads
- Policy-based access control

### 🚀 Deploy Anywhere
- Dockerized build
- Terraform scripts for infrastructure
- One-click deployment to DigitalOcean, AWS, or Azure

## 🧱 Tech Stack

- **Vector Store**: Qdrant
- **Backend**: FastAPI (Python)
- **LLM Agent**: LangChain + OpenAI (optionally local LLM)
- **Frontend**: Streamlit Web UI
- **Database**: PostgreSQL (for metadata & auth)
- **File Storage**: Local / S3-compatible (optional)
- **Deployment**: Docker + Terraform
- **Hosting**: DigitalOcean / AWS / Azure

## 📁 Project Structure

```
rag-boilerplate/
├── backend/                 # FastAPI with LangChain endpoints
│   ├── ingest.py            # File ingestion & embedding
│   ├── query.py             # Q&A endpoint using LangChain
│   └── main.py
├── ui/                      # Streamlit frontend for Q&A
│   └── pages/
├── vectorstore/            # Qdrant client logic
├── db/                     # PostgreSQL models & migrations
├── terraform/              # Infra as code setup
├── tests/
├── .env.template
└── README.md
```

## 🚀 Quick Start

### Prerequisites
- Python 3.9+
- Docker & Docker Compose
- PostgreSQL
- OpenAI API Key

### 1. Clone & Setup
```bash
git clone <repository-url>
cd rag-boilerplate
cp .env.template .env
# Edit .env with your API keys and database config
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Start Services
```bash
docker-compose up -d
```

### 4. Access the Application
- **Streamlit UI**: http://localhost:8501
- **FastAPI Docs**: http://localhost:8000/docs
- **Qdrant Dashboard**: http://localhost:6333

## 🔐 Authentication Options

### Open Source Tier
- Email + token-based auth
- MIT-licensed starter repo
- Working PDF/CSV RAG with UI
- Community contribution model

### Techvisory Premium Services
- Hosted RAG Portal for clients
- Branded frontend + enterprise SSO
- Document auto-ingestion from email or drive
- LangChain agent customization
- Advanced analytics dashboard
- Support & API access

## 📈 Impact

- Empowers SMEs to launch private, secure RAG apps quickly
- Accelerates AI adoption in regulated sectors
- Provides enterprise-grade document intelligence

## 🛠️ Development

### Running Tests
```bash
pytest tests/
```

### Adding New Document Types
1. Extend the ingestion pipeline in `backend/ingest.py`
2. Add corresponding tests
3. Update the UI to handle new formats

### Customizing the LLM Agent
Modify `backend/query.py` to customize the LangChain agent for your specific domain (medical, legal, insurance, etc.).

## 📄 License

MIT License - see LICENSE file for details.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

## 📞 Support

- **Open Source**: GitHub Issues
- **Premium**: Contact Techvisory for enterprise support

---

**Deployment URLs:**
- Self-hosted: `https://yourdomain.com/rag`
- Techvisory Cloud: `https://rag.techvisory.io` 
