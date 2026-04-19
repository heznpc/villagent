# Research Decisions Log

Records non-obvious choices with rationale. Append-only; don't rewrite history.

Format: `## YYYY-MM-DD -- <short title>` with **Context**, **Decision**, **Why**.

---

## 2026-04-19 -- Repository restructure to DDD-style layout

**Context**: Pre-paper state. Root had TODO, review, and docs/research-direction.md. No paper/, no manuscript, no gitignore.

**Decision**: Adopt full portfolio layout even though paper/ is empty. The research-direction.md seed moves to planning/drafts/ since it is an outline-like planning artifact (will be superseded by paper/main.tex when writing begins). docs/ is removed; its single file belongs in planning/drafts/.

**Why**: Uniform structure means the paper can be added by creating paper/main.tex without further reorganization. The seed doc is properly bounded as a draft form of the future paper.
