# Sanctum Suite

Privacy-first AI productivity tools that run on **your** machine with **local** models. Data stays
on-device; the suite selects and runs different local models per task.

This is the umbrella/index repo. Each tool lives in its own repository under
[github.com/TheAIHorizon](https://github.com/TheAIHorizon).

## Apps

| Tool | What it is | Repo |
|------|-----------|------|
| **SanctumWriter** | Local-first markdown editor with an AI writing companion (Ollama / LM Studio). Works offline. | [TheAIHorizon/SanctumWriter](https://github.com/TheAIHorizon/SanctumWriter) |
| **SanctumWriterPro** | SanctumWriter plus optional commercial models via OpenRouter/OpenAI/Anthropic/Google/xAI (bring your own key). | [TheAIHorizon/SanctumWriterPro](https://github.com/TheAIHorizon/SanctumWriterPro) |
| **Galatea** | Local voice AI companion with vision — speech in/out, webcam understanding, RAG memory. | [TheAIHorizon/Galatea](https://github.com/TheAIHorizon/Galatea) |
| **Consilium** | Multi-LLM council — query several models at once, compare, and evaluate side by side. | [TheAIHorizon/Consilium](https://github.com/TheAIHorizon/Consilium) |
| **SanctumKanban** | Self-hosted team kanban board. *(Private repo)* | TheAIHorizon/SanctumKanban |
| **ProcessPulse** | Educator writing-assessment tool — analyzes student thinking, not just output. *(Private repo)* | TheAIHorizon/ProcessPulse |

## The Sanctum Engine

The suite is moving onto a shared, local, egress-free model-serving engine — hardware-aware model
selection, task routing, and a memory-budgeted load/unload lifecycle behind one OpenAI-compatible
local API — so every app shares the hard parts instead of each hardcoding Ollama. The engine is
developed separately (`sanctum-engine`).

## Privacy model

Non-Pro builds are designed to be **structurally incapable of external egress** — the code to reach
a cloud provider is simply absent, not merely disabled. Pro builds (e.g. SanctumWriterPro) add an
optional, clearly-separated cloud module that you enable with your own API keys.

## License

**Polyform Noncommercial License 1.0.0** ([LICENSE](LICENSE)) — the standard license across the
Sanctum suite. Free for personal, educational, research, and other noncommercial use; commercial use
requires a separate license from the copyright holder. This is a **source-available** license, not
an OSI "open source" license: you can read and audit the code, but reuse is limited to noncommercial
purposes. Each app repository carries the same license.
