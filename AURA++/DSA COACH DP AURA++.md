Markdown<div align="center">

# ⚡ DSA AI COACH ⚡
### *Next-Gen Agentic Mentor for Data Structures & Algorithms*

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![LangGraph](https://img.shields.io/badge/Orchestration-LangGraph-FF6F00?style=for-the-badge)](https://langchain-ai.github.io/langgraph/)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![Streamlit](https://img.shields.io/badge/Frontend-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io)
[![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://postgresql.org)
[![Ollama](https://img.shields.io/badge/LLM-Qwen2.5--Coder-black?style=for-the-badge&logo=ollama&logoColor=white)](https://ollama.ai)

*Ditch generic chatbots. Experience an interactive DSA mentor that **thinks, adapts, remembers, and guides**.*

---

</div>

> 💡 **Why DSA AI Coach?**
> Traditional platforms force you to jump between separate tabs for problems, hints, code analysis, and solution guides. **DSA AI Coach brings everything into a unified, stateful AI agent pipeline.**

---

## 🧠 Project at a Glance

### 🛑 The Problem
Traditional DSA learning platforms isolate key components:
* ❌ Isolated Problem Sets
* ❌ Static / Instant Solution Spoilers
* ❌ Zero Contextual Code Debugging
* ❌ Stateless Session Loss

### 🚀 The Agentic Solution
Driven by **LangGraph**, the system intelligently routes student queries to specialized tools, providing adaptive, step-by-step guidance.

```text
 ───▸ [ Student ]
          │
          ▼
   [ Streamlit UI ] ───▸ [ FastAPI Backend ]
                                │
                                ▼
                      ┌──────────────────┐
                      │  DSA Agent Core  │
                      │   (LangGraph)    │
                      └────────┬─────────┘
                               │
     ┌──────────────┬──────────┼──────────┬──────────────┐
     ▼              ▼          ▼          ▼              ▼
 [Problem]       [Hint]     [ RAG ]    [Code]        [Memory]
   Tool           Tool       Tool     Analysis         Tool
                               │         │              │
                           (Qwen LLM) (Qwen LLM)   (PostgreSQL)
✨ Key Capabilities & FeaturesCapabilityPowered ByDescription🎯 Smart Problem SelectorProblem ToolSelects topic/difficulty-tailored problems without repeating solved ones.💡 Progressive HintsHint Tool3-tier progressive hint system (Concept ➔ Strategy ➔ Near-Solution).🔍 Context-Grounded RAGRAG Tool + QwenRetrieves deep explanations using Hybrid BM25 + Vector Search (RRF).💻 Intelligent Code ReviewCode ToolPinpoints logic bugs, edge cases, space/time complexity, and optimization hints.🧠 Stateful Student MemoryPostgreSQL + pgvectorTracks history, status, current problem, hints used, and retry counts.🛠️ The 5 Core ToolsPlaintext ┌───────────────────┐      ┌───────────────────┐      ┌───────────────────┐
 │   1. Problem Tool │      │    2. Hint Tool   │      │    3. RAG Tool    │
 │  Selects target   │ ───► │ 3-Tier progressive│ ───► │ Context-grounded  │
 │  DSA challenges   │      │   guidance hints  │      │   explanations    │
 └───────────────────┘      └───────────────────┘      └───────────────────┘
                                                                 │
 ┌───────────────────┐      ┌───────────────────┐                │
 │  5. Memory Tool   │      │ 4. Code Analyzer  │                │
 │ Persistent State  │ ◄─── │ Debugs, reviews & │ ◄──────────────┘
 │  (PostgreSQL)     │      │ optimizes code    │
 └───────────────────┘      └───────────────────┘
1️⃣ Problem ToolDynamically queries the curated problem bank:JSON{
  "topic": "dynamic_programming",
  "difficulty": "medium",
  "exclude_ids": ["dp_001", "dp_002"]
}
2️⃣ Hint ToolDelivers structured, progressive learning support:🟢 Level 1: Broad conceptual direction.🟡 Level 2: Specific algorithmic / pattern strategy.🔴 Level 3: Near-solution logic (without giving away code).3️⃣ RAG ToolGrounded explanation pipeline using Hybrid Semantic Retrieval & Local LLMs:Plaintext  [ Docs ] ➔ [ Loader ] ➔ [ Chunking ] ➔ [ Hybrid Search (BM25 + Semantic) ]
                                                        │
  [ Grounded Output ] ◄── [ Qwen LLM ] ◄── [ RRF Context Builder ]
4️⃣ Code Analysis ToolEvaluates student submissions for:Syntax & Logic ErrorsEdge Case VulnerabilitiesTime ($O(N)$) & Space ($O(1)$) ComplexitiesRefactoring Guidance5️⃣ Memory ToolMaintains dynamic session updates in PostgreSQL:YAMLSession ID: "sess_8820"
Current Problem: "Coin Change (dp_003)"
Topic: "dynamic_programming" | Difficulty: "medium"
Hints Used: 1 / 3
Attempts: 1
Status: "in_progress"
⚡ LangGraph Orchestration & Decision EngineThe router intelligently handles fast paths vs. multi-step reasoning via a ReAct Decision Gate.Plaintext                          [ START ]
                              │
                              ▼
                         [ Router ]
                              │
   ┌─────────────┬────────────┼────────────┬─────────────┐
   ▼             ▼            ▼            ▼             ▼
[PROBLEM]     [HINT]       [CODE]        [RAG]       [DIRECT]
   │             │            │            │             │
   └─────────────┴─────┬──────┴────────────┴─────────────┘
                       ▼
                 [ Memory Tool ]
                       │
             [ ReAct Decision Gate ]
               /                 \
        (Single Step)      (Multi-Step Planning)
             │                       │
             ▼                       ▼
         [ FINAL ]              [ Planner ] ──► [ Next Tool ] ──► [ FINAL ]
⚡ Performance Optimization: Simple queries bypass multi-turn reasoning and instantly return results, significantly reducing execution latency when running local LLMs.📚 Knowledge Base & Covered TopicsCurrent DP Knowledge Bank coverage includes 20 core problems:Plaintext 📂 knowledge_base/documents/
 ├── 01. House Robber               ├── 11. Minimum Path Sum
 ├── 02. Climbing Stairs            ├── 12. Word Break
 ├── 03. Coin Change                ├── 13. Longest Common Subsequence
 ├── 04. Longest Inc. Subsequence   ├── 14. Edit Distance
 ├── 05. Partition Equal Subset     ├── 15. Maximum Subarray
 ├── 06. 0/1 Knapsack               ├── 16. Target Sum
 ├── 07. Unbounded Knapsack         ├── 17. Interleaving String
 ├── 08. House Robber II            ├── 18. Distinct Subsequences
 ├── 09. Decode Ways                ├── 19. Palindromic Substrings
 └── 10. Unique Paths               └── 20. Matrix Chain Multiplication
🏗️ Technical StackPlaintext🛠️ CORE ENGINE & INFRASTRUCTURE
 ├── Language:       Python 3.10+
 ├── Frameworks:     FastAPI (Backend) | Streamlit (Frontend)
 ├── Orchestration:  LangGraph (Stateful Graph Workflows)
 ├── LLM / Local:    Qwen 2.5 Coder via Ollama (1.5b / 7b)
 ├── Vector Database: PostgreSQL + pgvector
 ├── Embeddings:     all-MiniLM-L6-v2
 └── Search Engine:  Hybrid BM25 + Semantic Search + RRF
📂 System File ArchitecturePlaintext📁 dsa-ai-coach/
 ├── 📂 agents/               # LangGraph state management & router logic
 ├── 📂 api/                  # FastAPI web server entry points
 ├── 📂 chunking/             # Recursive chunking strategy
 ├── 📂 dashboard/            # Streamlit frontend app
 ├── 📂 knowledge_base/       # Raw DSA knowledge Markdown files
 ├── 📂 problems/             # Problem Bank database scripts
 ├── 📂 rag/                  # RAG context builder & prompt definitions
 ├── 📂 tools/                # Specialized Agent Tools (RAG, Hint, Code, Memory)
 ├── 📜 ingest.py             # Knowledge base ingestion script
 ├── 📜 requirements.txt      # Project dependencies
 └── 📜 .env.example          # Environment variable template
🚀 Quickstart & Installation1. Clone & Setup EnvironmentBash# Clone the repository
git clone [https://github.com/your-username/dsa-ai-coach.git](https://github.com/your-username/dsa-ai-coach.git)
cd dsa-ai-coach

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
2. Configure Local LLM (Ollama)Bash# Pull lightweight model for high-speed routing & response
ollama pull qwen2.5-coder:1.5b

# (Optional) Pull heavy model for advanced code review
ollama pull qwen2.5-coder:7b
3. Launch ServicesBash# Terminal 1: Launch FastAPI Backend Engine
uvicorn api.main:app --reload --port 8000

# Terminal 2: Launch Interactive Frontend Interface
streamlit run dashboard/app.py
🔄 Interaction Flow BlueprintPlaintext 🟢 Student Request
    └─► "Give me a medium DP problem"
 
 🔵 Agent Action
    ├─► Router selects: PROBLEM
    ├─► Problem Tool retrieves: "Coin Change"
    └─► Memory updates: { problem_id: "dp_003", status: "in_progress" }

 🟡 Student Action
    └─► "Give me a hint"

 🔵 Agent Action
    ├─► Router selects: HINT
    ├─► Hint Tool fetches: Hint Level 1
    └─► Memory updates: { hints_used: 1 }
🔮 Roadmap & Future Enhancements[ ] 🔐 User Auth: Student login profiles & authentication.[ ] 📊 Analytics Dashboard: Topic mastery metrics & visual progress graphs.[ ] 🧪 Code Sandbox: Interactive code runner with automated test suites.[ ] 🔄 Spaced Repetition: Re-suggest previously failed problems over time.[ ] 🐳 Dockerization: Complete containerized deployment setup.DSA AI Coach • Empowering developers to master algorithms through intelligent AI mentoring.
