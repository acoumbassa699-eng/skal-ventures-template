# SKAL Ventures SKAL Agent Canvas

<p align="center">
  <img src="public/logo.svg" alt="SKAL Ventures Logo" width="200">
</p>

<p align="center">
  <strong>AI-powered developer control center for coding agents and automations.</strong>
</p>

<p align="center">
  Run AI coding agents with a visual interface across local, remote, and cloud backends.
</p>

---

## Overview

SKAL Ventures SKAL Agent Canvas transforms your coding agents into a self-hosted, always-on engineering team. It's a developer control center for starting conversations and automating everyday tasks.

## Features

- 🤖 **AI Agent Interface** - Visual chat interface for AI coding agents
- 💻 **Terminal Emulator** - Built-in terminal with full ANSI support
- 📁 **File Explorer** - Browse and manage project files
- ⚙️ **Backend Management** - Connect to multiple agent backends
- 🔧 **Settings** - Configure LLM providers and preferences

## Quick Start

### Option 1: With Docker Sandbox (Recommended)

```bash
export PROJECTS_PATH="$HOME/projects"
mkdir -p "$PROJECTS_PATH" "$HOME/.skalventures"

docker run -it --rm \
  -p 8000:8000 \
  -v "$HOME/.skalventures:/home/user/.skalventures" \
  -v "${PROJECTS_PATH}:/projects" \
  ghcr.io/acoumbassa699-eng/skalventures-agent-canvas:latest
```

### Option 2: From Source

```bash
git clone https://github.com/acoumbassa699-eng/skal-ventures-template.git
cd skal-ventures-template
npm install
npm run dev
```

## Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                   SKAL Ventures SKAL Agent Canvas                │
├─────────────────────────────────────────────────────────────┤
│  Frontend (React + TypeScript)                              │
│  ├── Chat Interface                                         │
│  ├── Terminal Emulator                                      │
│  ├── File Explorer                                          │
│  └── Settings Panel                                         │
└─────────────────────────────────────────────────────────────┘
                          │
                          │ REST / WebSocket
                          ▼
┌─────────────────────────────────────────────────────────────┐
│                   Agent Backend (VPS)                        │
├─────────────────────────────────────────────────────────────┤
│  ├── Agent Runtime                                          │
│  ├── Sandbox Environment                                    │
│  └── LLM Integration                                        │
└─────────────────────────────────────────────────────────────┘
```

## Documentation

- [Full Documentation](./docs/README.md)
- [Self-Hosting Guide](./docs/SELF_HOSTING.md)
- [Architecture](./docs/architecture.md)

## Tech Stack

- **Frontend**: React 19, TypeScript, Vite
- **Styling**: Tailwind CSS, HeroUI
- **Terminal**: xterm.js
- **Code Editor**: Monaco Editor
- **Backend**: Python (agent runtime)

## License

MIT
