# CircularQA
Cited answers over RBI circulars that know when a rule has been superseded.

## Stack
Python 3.12 (uv), FastAPI, PostgreSQL + pgvector, Redis, pytest.

## Commands
- Install: `uv sync`
- Test: `uv run pytest`
- Lint and format: `uv run ruff check --fix . && uv run ruff format .`
- Types: `uv run mypy src`

## Rules
- Type hints everywhere; mypy strict must pass.
- Every change comes with tests.
- Never commit secrets; config comes from environment variables.
