# RAG AI Agent for SQL Database

A powerful local RAG (Retrieval-Augmented Generation) AI agent that enables natural language querying of SQL databases using LangChain and Ollama.

## Architecture

```
RAG AI Agent
├── Database Connection Layer
├── Schema Analysis & Vectorization
├── Query Processing Engine
├── LangChain RAG Pipeline
├── Ollama LLM Integration
└── User Interface
```

## Quick Start

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Configure your database connection in `config/database.yaml`

3. Start Ollama service:
   ```bash
   ollama serve
   ```

4. Pull required models:
   ```bash
   ollama pull llama3.1
   ollama pull nomic-embed-text
   ```

5. Initialize the database schema:
   ```bash
   python scripts/initialize_schema.py
   ```

6. Run the agent:
   ```bash
   python main.py
   ```

## Usage Examples

- "What are the sales last month?"
- "Show me the top 10 customers by revenue"
- "What's the average order value this quarter?"
- "Which products have the highest profit margins?"

## Project Structure

```
RAG/
├── src/
│   ├── agents/          # AI agent implementations
│   ├── database/        # Database connection and operations
│   ├── embeddings/      # Vector embeddings and storage
│   ├── llm/            # LLM integration (Ollama)
│   ├── rag/            # RAG pipeline components
│   └── utils/          # Utility functions
├── config/             # Configuration files
├── data/              # Sample data and schemas
├── scripts/           # Setup and utility scripts
├── tests/             # Test files
└── ui/                # User interface components
```

## Configuration

See `config/README.md` for detailed configuration options.

## License

MIT License
