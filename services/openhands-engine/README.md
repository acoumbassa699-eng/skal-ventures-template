# SKAL Ventures Agent Engine

This directory contains configuration for the SKAL Ventures agent runtime engine.

## Quick Start

### Using Docker

```bash
docker run -d \
  --name skal-agent-engine \
  -p 3000:3000 \
  ghcr.io/acoumbassa699-eng/skalventures-engine:latest
```

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `LLM_API_KEY` | API key for LLM provider | Yes |
| `LLM_BASE_URL` | Base URL for LLM API | No |
