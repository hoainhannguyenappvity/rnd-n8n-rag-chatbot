# RAG Chatbot using n8n with Qdrant, Ollama, and AI Agent

This repository contains an n8n workflow that implements a Retrieval-Augmented Generation (RAG) chatbot using Qdrant as the vector database, Ollama for embeddings, and an AI Agent for enhanced interactions.

## n8n Setup

Install **n8n** via npm

```bash
npm i -g n8n
```

### Start

Change directory to your project folder and run below command in **Command Prompt**

```bash
set NODES_EXCLUDE="[]" && set N8N_COMMUNITY_PACKAGES_ENABLED=true && set NODE_FUNCTION_ALLOW_EXTERNAL=uuid && set N8N_RESTRICT_FILE_ACCESS_TO="./" && n8n
```

### Import Workflow

Import **RAG.json** or **RAG Embedding Gemma.json** file to your n8n workflows

Configure the credentials for Qdrant, Ollama, and AI Agent model

## Qdrant Setup

Install Qdrant via Docker

```bash
docker pull qdrant/qdrant:latest
```

Run the Qdrant container

```bash
docker run -d --name qdrant -p 6333:6333 qdrant/qdrant:latest
```

Verify the Qdrant container is running

```bash
docker ps
```

You should see the `qdrant` container listed in the output.

## Ollama Docker Setup

Pull the Ollama Docker image

```bash
docker pull ollama/ollama:latest
```

Run the Ollama container

```bash
docker run -d --name ollama -p 11434:11434 ollama/ollama:latest
```

Verify the Ollama container is running

```bash
docker ps
```

You should see the `ollama` container listed in the output.

Pull the embeddinggemma model

```bash
docker exec -it ollama ollama pull embeddinggemma
```

Verify the model is downloaded

```bash
docker exec -it ollama ollama list
```

You should see `embeddinggemma` listed in the output.

## Docling Setup (Optional)

Install Docling tool via [uv](https://github.com/astral-sh/uv)

```bash
uv tool install docling
```

## Publish Workflow (Optional)

You can publish workflow to your own n8n instance by following the [n8n documentation](https://docs.n8n.io/workflows/publish/).

## Example Questions

Here are some example questions you can ask the RAG chatbot about the MOMENTUM True Wireless 4 Earbuds:

- What are the key features of the MOMENTUM True Wireless 4 Earbuds?
- How long does the MOMENTUM True Wireless 4 Earbuds take to fully charge the earbuds and case?
- How to connect the MOMENTUM True Wireless 4 Earbuds to a device?
- How to accept or reject calls using the MOMENTUM True Wireless 4 Earbuds?
- ... and many more!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
