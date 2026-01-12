# n8n RAG

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

Import **RAG.json** file to your n8n workflows

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

## Docling Setup

Install Docling

```bash
uv tool install docling
```
