Research Program: 1 (Human-Controlled AI Systems)
Status: Concept note
Relationship to other work: Companion to Ploidy — Ploidy resets at the session level (context), Villagent resets at the entity level (configuration).

# Villagent

This is a concept note, not a finished paper. No manuscript exists yet; only a seed document and an experiment skeleton.

> 에이전트 구성(프롬프트 + 메모리 + 도구 연결)의 비가역적 소실을 "죽음"으로 정의했을 때,
> 그 죽음을 부여하면 에이전트 집단의 역학이 어떻게 달라지는가?

**Operational definition of death:** the irreversible loss of an agent's configuration — system prompt, memory structure, and tool surface — even when the underlying model weights are unchanged. Two agents on the same base model with different configurations are different entities; replacing one configuration with another is what Villagent calls death, as distinct from Ploidy's session-context reset.

The seed document is in [planning/drafts/research-direction.md](planning/drafts/research-direction.md).

## Currently implemented

- Seed document (`planning/drafts/research-direction.md`) — Korean, derived from Ploidy follow-up planning.
- Repository skeleton (`paper/`, `experiments/`, `literature/`, `planning/`).
- Project-level `CLAUDE.md` describing scope and conventions.

## Planned

- MVP multi-agent population experiment with configuration mortality as the manipulated variable.
- Comparison against Ploidy's session-level reset as the baseline epistemic intervention.
- English translation of the seed document when a manuscript draft begins.

## Design intent

- **Entity-level, not session-level.** Ploidy already covers context reset. Villagent isolates what changes when the configuration itself is destroyed, not just its memory.
- **Configuration as identity.** Prompt + memory schema + tool wiring defines the agent, not the base model — so swapping configurations on the same weights is a meaningful mortality event.
- **Concept-note discipline.** No manuscript writing until an experiment exists. The seed doc and TODO live in `planning/`, deliberately separate from `paper/`.

## Non-goals

- Anthropomorphic claims about agent suffering, awareness, or moral status.
- A general theory of agent populations — the scope is the specific intervention of configuration mortality.
- Publishing a manuscript before any empirical work has been run.

## Repository structure

```
villagent/
  paper/                      Domain (empty; manuscript not yet written)
  experiments/                Application (skeleton; MVP population experiment planned)
  literature/                 Reading notes, gap analysis
  planning/                   TODO, review, decisions log
    drafts/
      research-direction.md   Seed doc (Ploidy follow-up planning)
```
