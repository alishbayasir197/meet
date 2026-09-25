---
name: python-uv-starter
description: Scaffold a new Python project with uv (backend folder, hello world, dependency sync). Use whenever the user wants to start, init, bootstrap, or set up a Python project, backend, API, or script with uv, or mentions "uv init", "uv run", "uv sync", or a Python starter/boilerplate - even if they don't say "uv" explicitly.
---

# Python uv Starter

Bootstraps a minimal Python project using [uv](https://docs.astral.sh/uv/).

## Steps

1. Create the project (default folder name is `backend`; use the user's name if given):

   ```bash
   uv init backend
   cd backend
   ```

2. Replace the generated `main.py` with the hello world template bundled in this skill:

   ```bash
   cp <skill-path>/scripts/hello.py main.py
   ```

3. Run it:

   ```bash
   uv run main.py
   ```

   Expected output: `Hello, world!`

4. Install / sync dependencies from `pyproject.toml`:

   ```bash
   uv sync
   ```

## Adding packages

```bash
uv add fastapi uvicorn      # example
uv sync
uv run main.py
```

## Notes

- If `uv` is missing, install it first: `curl -LsSf https://astral.sh/uv/install.sh | sh` (or `pip install uv`).
- `uv init` creates `pyproject.toml`, `.python-version`, `README.md`, and `main.py`. Do not delete `pyproject.toml`; `uv sync` depends on it.
- Commit `uv.lock` (created on first `uv sync`/`uv run`) for reproducible installs.
