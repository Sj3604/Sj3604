<h1 align="center">Hi, I'm Shagun 👋</h1>
<h3 align="center">AI/ML Engineer · Generative AI · Agentic RAG · Multi-Agent Systems</h3>

<p align="center">
  Building production-grade Generative AI systems — from retrieval architectures to autonomous, multi-agent workflows.
</p>

---

### 🔭 What I Work On

I design and build GenAI systems from the ground up — favoring solid, production-grade implementations over quick patches. My focus areas:

- **Retrieval-Augmented Generation (RAG)** — Graph RAG, Hybrid RAG, Multi-Query RAG, Corrective RAG (CRAG), Self-RAG, and comparative retrieval strategy design
- **Agentic AI** — currently deep in this space: building autonomous, tool-using agents and multi-agent workflows that plan, act, and self-correct rather than just retrieve-and-answer
- **Multi-Agent Orchestration** — task decomposition, parallel fan-out, and distributed execution for agent workflows
- **Knowledge Graphs & LLM Infrastructure** — entity resolution, graph extraction, and scalable ingestion pipelines for GenAI applications
- **Distributed Systems** — queue-based, workload-separated architectures for ML/LLM pipelines

---

### 🧭 Currently Exploring

I'm actively deepening my work in **Agentic AI** — moving beyond single-shot RAG pipelines into systems where agents plan, decompose tasks, call tools, and coordinate with each other. My orchestrator project below is the core of this exploration: a ground-up rewrite of how task decomposition and distributed multi-agent execution should work.

---

### 🚀 Featured Projects

#### 🧠 Agentic Graph RAG System
A local-first, agentic Graph RAG system built from scratch (Windows-native, no Docker/WSL) with a two-pipeline architecture — Data Pipeline → Memory Pipeline — feeding a **KuzuDB** knowledge graph.
- Rewrote entity resolution with a three-tier strategy (in-batch matching, cross-document lookup, auto-registration)
- Migrated knowledge graph storage from MongoDB to embedded KuzuDB with native Cypher queries
- ~500x retrieval speedup via a cached NumPy embedding matrix and batched graph expansion
- Built an MCP server + `smart_query` tool with dual-axis query classification and domain-specific agent routing
- Audited and hardened a multi-modal NeMo Curator + nv-ingest production pipeline (PII redaction, OCR engine cleanup)
- **Stack:** FastAPI, Celery/RabbitMQ, MongoDB Atlas, KuzuDB, spaCy, Qwen3, NeMo Curator, nv-ingest, PaddleOCR-VL

#### 🤖 Multi-Agent Orchestrator *(active — agentic AI focus)*
A standalone, ground-up rewrite of a multi-agent orchestration module for complex, autonomous task execution.
- HTN/DAG-based task decomposition — breaking high-level goals into agent-executable subtasks
- Parallel fan-out via LangGraph's `Send()` API for concurrent agent execution
- Distributed execution with Celery and swappable checkpointers for stateful, resumable agent runs
- Designed to closely interoperate with the Agentic Graph RAG system below, giving agents grounded, graph-based retrieval as a tool

#### 🔍 Corrective & Self-RAG Implementations
Built CRAG (Corrective RAG) and Self-RAG pipelines, each in both LangGraph-orchestrated and plain-Python control-flow versions.
- **Stack:** LangGraph, Groq, ChromaDB

#### 🕸️ Multi-Strategy RAG Comparison System
A LangChain-based system combining Graph RAG (Neo4j Aura), Hybrid RAG (BM25 + dense + RRF), and Multi-Query RAG for head-to-head retrieval strategy evaluation.
- **Stack:** LangChain, Neo4j Aura, Mistral

---

### 📚 RAG & GenAI Deep Dives

Across these projects, I've worked hands-on with the full spectrum of modern RAG design:

| Pattern | What it solves | Where I've built it |
|---|---|---|
| **Graph RAG** | Multi-hop reasoning over entity relationships | Agentic Graph RAG (KuzuDB), Multi-Strategy RAG (Neo4j) |
| **Hybrid RAG** | Combining lexical + semantic recall | Multi-Strategy RAG (BM25 + dense + RRF) |
| **Corrective RAG (CRAG)** | Self-correcting retrieval on low-confidence results | Standalone LangGraph implementation |
| **Self-RAG** | Reflective, on-demand retrieval decisions | Standalone LangGraph implementation |
| **Multi-Query RAG** | Query expansion for broader recall | Multi-Strategy RAG system |
| **Agentic RAG** | Retrieval as a tool inside autonomous agent loops | Agentic Graph RAG's MCP `smart_query` layer |

---

### 🛠️ Tech Stack

**Languages & Runtime:** Python · Windows 11 (native) / WSL2 when needed
**AI/ML:** LangGraph · LangChain · spaCy · Qwen3 · Mistral · Groq
**Data & Retrieval:** KuzuDB · Neo4j Aura · MongoDB Atlas · ChromaDB · BM25 + Dense Hybrid Search
**Pipelines & Infra:** NeMo Curator · nv-ingest · PaddleOCR-VL · Celery · RabbitMQ · FastAPI
**Tooling:** `uv` for Python package management

---

### 💡 Philosophy

I favor **working code over explanation** and **iterative implementation over upfront specification** — building systems that hold up under real production conditions, not just demos.

---

<p align="center"><i>Open to discussing agentic RAG architectures, multi-agent systems, and distributed AI infrastructure.</i></p>
