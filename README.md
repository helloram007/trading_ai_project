# trading_ai_project
This is my AI Algos and project that is used to build my Tradingview Pinesscripts and MT4/5 Scripts for better automation of everyday analysis.

# AI Project Template

A modular, scalable 4-folder directory structure designed for AI applications (solo, enterprise, autonomous agents, and RAG). 

> **Core Principle:** Four folders. Four jobs. Zero confusion.

---

## 📁 Directory Structure

```text
ai-project/
├── prompts/              # Every prompt treated as versioned code
│   ├── system/           # High-level persona & system instruction prompts
│   ├── tasks/            # Task-specific or workflow prompts
│   └── tools/            # Tool-calling & function specification prompts
│
├── data/                 # Data inputs consumed by the AI
│   ├── raw/              # Unprocessed source documents, datasets, or context
│   └── processed/        # Cleaned, chunked, or vectorized data
│
├── agents/               # Configurations, logic, and operational capabilities
│   ├── skills/           # Specific task routines and modular capabilities
│   └── tools/            # Custom API integration code and tool executions
│
└── evals/                # Verification, benchmarks, and performance metrics
    ├── tests/            # Test suites and expected output assertions
    ├── traces/           # Execution logs and agent run histories
    └── scorecards/       # Accuracy, latency, cost, and alignment metrics


🛠️ Folder Breakdown
1. prompts/ — Versioned Prompt Files
    Treat prompts with the same rigour as source code. Avoid hardcoding text strings into application logic.
     - system/: Baseline system prompts establishing role, tone, and guardrails.
     - tasks/: Goal-oriented templates for specific pipeline steps or sub-tasks.
     - tools/: Prompt templates specifically structured for schema definition and tool invocations.

2. data/ — Inputs and Context
    Houses all data processed by LLMs, RAG pipelines, or agent workflows.
     - raw/: Source files (PDFs, Markdown, JSON, CSVs) before any transformation.
     - processed/: Vector embeddings, pre-parsed documents, or structured JSON outputs ready for retrieval.

3. agents/ — Agent Configurations and Skills
    Defines how autonomous agents behave and what actions they can perform.
     - skills/: Multi-step workflows and procedural reasoning logic assigned to agents.
     - tools/: API connectors, database lookup scripts, and external tools callable by agents.

4. evals/ — Quality & Performance Proof
    Ensures system outputs are deterministic, accurate, and safe.
     - tests/: Unit and integration test scenarios testing model response against expected ground truth.
     - traces/: Detailed run-logs showing full step-by-step reasoning steps and tool calls.
     - scorecards/: Metric tracking across versions (e.g., accuracy rates, token usage, latency).

🚀 Quick Start Setup
    To replicate this structure in a new directory, run:

```bash
mkdir -p ai-project/{prompts/{system,tasks,tools},data/{raw,processed},agents/{skills,tools},evals/{tests,traces,scorecards}}
