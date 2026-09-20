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

#### 🎥 Video-to-Transcript RAG System
A pipeline that takes a video URL, transcribes it into both Hindi and English using the **Sarvam AI** API (alongside other supporting APIs), and feeds the transcript into a RAG system — so users can ask natural-language questions about the video's content instead of watching it end-to-end. Built for meeting recall and fast video/content understanding.
- Video URL → audio extraction → bilingual (Hindi/English) transcription via Sarvam AI
- Transcript chunked and indexed into a RAG store for question-answering over the video's content
- Designed around real use cases: meeting summaries and Q&A, general video comprehension
- **Stack:** Sarvam AI (transcription), RAG/vector retrieval, LLM for Q&A

#### 🤖 Multi-Agent Orchestrator *(active — agentic AI focus)*
A standalone, ground-up rewrite of a multi-agent orchestration module for complex, autonomous task execution.
- HTN/DAG-based task decomposition — breaking high-level goals into agent-executable subtasks
- Parallel fan-out via LangGraph's `Send()` API for concurrent agent execution
- Distributed execution with Celery and swappable checkpointers for stateful, resumable agent runs

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
| **Graph RAG** | Multi-hop reasoning over entity relationships | Multi-Strategy RAG (Neo4j) |
| **Hybrid RAG** | Combining lexical + semantic recall | Multi-Strategy RAG (BM25 + dense + RRF) |
| **Corrective RAG (CRAG)** | Self-correcting retrieval on low-confidence results | Standalone LangGraph implementation |
| **Self-RAG** | Reflective, on-demand retrieval decisions | Standalone LangGraph implementation |
| **Multi-Query RAG** | Query expansion for broader recall | Multi-Strategy RAG system |
| **Transcript RAG** | Q&A grounded in transcribed audio/video content | Video-to-Transcript RAG System (Sarvam AI) |

---

### 🛠️ Tech Stack

**Languages & Runtime:** Python · Windows 11 (native) / WSL2 when needed
**AI/ML:** LangGraph · LangChain · spaCy · Qwen3 · Mistral · Groq · Sarvam AI
**Data & Retrieval:** Neo4j Aura · ChromaDB · BM25 + Dense Hybrid Search · Vector RAG stores
**Pipelines & Infra:** Celery · RabbitMQ · FastAPI
**Tooling:** `uv` for Python package management

---

### 💡 Philosophy

I favor **working code over explanation** and **iterative implementation over upfront specification** — building systems that hold up under real production conditions, not just demos.

---

<p align="center"><i>Open to discussing RAG architectures, multi-agent systems, and distributed AI infrastructure.</i></p>
