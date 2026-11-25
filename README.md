# Research Agent

Research Agent is an AI application that takes a research question, gathers evidence, and returns a sourced answer.

It runs on Python 3.14 and is managed with [uv](https://docs.astral.sh/uv/). The installed stack includes OpenAI, Anthropic, Mistral, and Vertex AI for model calls, Tavily and Wikipedia for search, and FastAPI for an HTTP API.

## Requirements

- Python 3.14 or newer
- [uv](https://docs.astral.sh/uv/getting-started/installation/)

## Setup

From the repository root:

```bash
uv sync
```

This creates `.venv` from `.python-version` and installs the locked dependencies in `uv.lock`.

## Run

```bash
uv run research-agent
```

That invokes the `research-agent` console script declared in `pyproject.toml`.

## Configuration

Keep provider credentials in a local `.env` file. That file stays out of git.

| Variable | Used for |
| --- | --- |
| `OPENAI_API_KEY` | OpenAI models |
| `ANTHROPIC_API_KEY` | Anthropic models |
| `MISTRAL_API_KEY` | Mistral models |
| `TAVILY_API_KEY` | Tavily web search |
| `GOOGLE_APPLICATION_CREDENTIALS` | Vertex AI |

Set the keys for the providers you actually call.

## Layout

```text
src/research_agent/    application package
pyproject.toml         project metadata and dependencies
uv.lock                locked dependency set
```
