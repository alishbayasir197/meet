# OpenChat

## Stack

* *web:* Next.js 16, React 19, TypeScript, Tailwind CSS 4, shadcn/ui
* *api:* FastAPI, Python 3.13, uv, Ruff, pytest
* *Local AI:* Ollama at http://localhost:11434, default model qwen3.5:2b
* *Cloud AI fallback:* OpenAI, Anthropic, Gemini
* *web:* web/
* *api:* api/

## Commands

### web

powershell
cd web
npm install
npm run dev


Port: 3000

### api

powershell
cd api
uv sync
uv run fastapi dev


Port: 8000

Add api package:

powershell
uv add <package>


Add web package:

powershell
npm install <package>


Run tests:

powershell
cd api
pytest


## Rules

* *Inspect existing code before changing it.*
* Follow existing project patterns; avoid unnecessary rewrites.
* Keep web, backen…