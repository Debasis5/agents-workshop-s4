# Session 4 — Agent Tools & Communication
**MCP · A2A Protocol · LangChain Tools · Build Your Own MCP Server**

## Quick Start

> Requires **Python 3.10+** (3.11 recommended). LangGraph won't install on 3.9.

```bash
# 1. Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

# 2. Install all dependencies
pip install -r requirements.txt

# 3. Copy the env template and add your key
cp .env.example .env             # Windows: copy .env.example .env
# then open .env and paste your GROQ_API_KEY (free: https://console.groq.com/keys)

# 4. Verify setup
python verify_setup.py
```

## Folder Structure

```
s4_workshop/
│
├── README.md
├── requirements.txt
├── .env.example
├── verify_setup.py               ← run before the workshop
│
├── tools_lab/                    ← LAB 1: LangChain Custom Tools
│   ├── starter.py                ← fill in TODOs
│   └── solution.py               ← reference answer
│
├── mcp_lab/                      ← LAB 2: Build a Python MCP Server
│   ├── starter.py
│   ├── solution.py
│   └── claude_desktop_config.json  ← copy into Claude Desktop config
│
├── a2a_lab/                      ← LAB 3: A2A Agent Card + Task Routing
│   ├── starter.py                ← the A2A server
│   ├── client.py                 ← the A2A client
│   └── solution/
│       ├── server.py
│       └── client.py
│
└── homework/
    ├── hw1_mcp_server/           ← Build a useful MCP server
    │   ├── github_mcp_server.py  ← GitHub MCP (reference impl)
    │   └── starter.py            ← blank template for your own API
    ├── hw2_a2a_extended/         ← Full A2A task lifecycle
    │   └── solution.py
    ├── hw3_langchain_toolkit/    ← Custom LangChain Toolkit + LangGraph
    │   └── solution.py
    └── hw4_mcp_exploration/      ← MCP ecosystem exploration guide
        └── exploration_guide.md
```

## API Keys

| Key | Get it from | Used in |
|-----|-------------|---------|
| `GROQ_API_KEY` (free) | [console.groq.com/keys](https://console.groq.com/keys) | All labs (default) |
| `OPENAI_API_KEY` (paid, optional) | [platform.openai.com](https://platform.openai.com/api-keys) | Alternative to Groq |
| `GITHUB_TOKEN` | github.com/settings/tokens | HW1 GitHub MCP |
| `TAVILY_API_KEY` | app.tavily.com (free) | Optional search tool |

## Model
Default is Groq's `llama-3.3-70b-versatile` (free, fast). To use OpenAI instead, set `OPENAI_API_KEY` and change `OPENAI_MODEL_NAME=gpt-4o-mini` in `.env`.

## Series
S1 ✓ · S2 ✓ · S3 ✓ · **S4 ← you are here** · S5 RAG & Memory · S6 Production
