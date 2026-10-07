# Ai-Sithum — SK AI

Ai-Sithum is the GitHub home for the SK AI local-first, Sinhala-first multimodal AI project.

## Project status

The repository is being upgraded from the original AI Studio placeholder into a reproducible software project. The reference implementation contains:

- SK-LLM: decoder-only Transformer with RMSNorm, RoPE, SwiGLU, GQA, KV cache and weight tying
- Sinhala + English + code tokenizer
- Agent orchestration, planning, verification and tool routing
- Local coding/build analysis and project generation
- Audio, music, image and video pipelines
- Android and Windows project generators
- Local document/vision/RAG components
- React/Vite workbench
- Offline-first operation with explicit permission gates for PC/tool actions

## Engineering principles

1. Sinhala-first user experience and language handling.
2. Offline-first by default; network access must be explicit.
3. Permission-gated PC control; missing or ambiguous permission fails closed.
4. No hidden execution, persistence, privilege escalation or credential handling.
5. Keep model/provider adapters replaceable.
6. Never claim a model size or capability unless the corresponding weights and tests actually exist.

## Model tiers

The reference project defines configurable SK-LLM tiers including a small local CPU checkpoint and larger optional tiers. A configuration targeting billions of parameters is not proof that those weights have been trained or installed.

## Development

Preserve the existing module boundaries: `agents/`, `tools/`, `core/`, `model/`, `tokenizer/`, `coding/`, `audio/`, `android/`, `configs/`, and `src/`.

## Security

See [SECURITY.md](SECURITY.md). All consequential tool execution must pass through the permission boundary and default to deny.

## License

Apache-2.0 for project code unless a bundled dependency or model artifact states otherwise.
