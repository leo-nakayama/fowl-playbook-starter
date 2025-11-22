# FOWL Playbook Starter

### *A framework for executable reasoning, structured thinking, and reflective computing.*

FOWL Playbooks are small YAML files that encode reasoning pipelines.

You write your thought process as code:

```
context → logic operators → structured outputs → Observation Report
```

The goal is to turn intuition into repeatable, auditable reasoning.

This project provides:

* lightweight reasoning modules (Four Causes, TradeoffLens, Naikan)
* a simple YAML playbook syntax
* a runner script that executes playbooks
* cheat sheets and “how to design your first playbook” guides
* a set of example playbooks you can extend immediately

FOWL is **not** a language model; it is a *human reasoning framework* expressed in YAML.

---

## Why YAML?

Because YAML is:

* precise enough for structured logic
* flexible enough for human intuition
* diff-friendly (Git)
* readable enough for philosophical reflection

FOWL Playbooks unify:

* engineering thinking
* philosophy (Aristotle)
* decision analysis (tradeoffs)
* self-reflection (Naikan)
* logical pipelines

---

## Quick Start

### 1. Clone

```bash
git clone https://github.com/leo-nakayama/fowl-playbook-starter
cd fowl-playbook-starter
```

### 2. Run an example playbook

```bash
python tools/dsl-run.py playbooks/minimal_four_causes.yaml -o out/result.md
```

### 3. Edit playbooks

Try modifying:

```
context:
  idea: "Should I start a new project?"
```

or add your own operator chain.

---

## Folder Overview

* `modules/` – reasoning modules (AristotleFourCauses, Naikan, TradeoffLens)
* `playbooks/` – executable YAML pipelines
* `tools/dsl-run.py` – minimal runner
* `docs/` – guides & cheat sheets
* `out/` – generated Observation Reports

---

## Example Output

When you run a playbook, the runner produces a structured report:

```
[Module] AristotleFourCauses  
[Function] Deduction  
[InputData] "Why do some projects stall?"
[DetectedPatterns]
  - unclear ownership
  - mismatched incentives
  - insufficient material conditions
[Trade-offs]
  - speed vs clarity
  - autonomy vs oversight
[Micro-Playbook]
  - clarify owner
  - re-check incentive alignment
  - ensure prerequisites exist
```

---

## FOWL Thinking Pipeline

```text
[1. Context Layer]
      │
      ▼
Raw Facts / Events / Ideas
      │
      │ (MaterialCause)
      ▼
────────────────────────────────────────────
[2. Logic Layer: call]
      │
      ├─ O_decompose (AristotleFourCauses)
      ├─ O_surfaceAxes (TradeoffLens)
      ├─ O_detectShadowLine (PoliticalDynamics)
      └─ O_selfReflect (SyntheticNaikan)
             …
      │
      │ (EfficientCause)
      ▼
────────────────────────────────────────────
[3. Structured Outputs]
      │
      ├─ causes.yaml
      ├─ axes.yaml
      ├─ shadow.yaml
      └─ reflections.yaml
      │
      │ (FormalCause)
      ▼
────────────────────────────────────────────
[4. Observation Report]
      │
      ▼
Patterns / Trade-offs / Telos / Micro-Playbook
(FinalCause)

```

## Who Is This For?

* engineers who want structured thinking
* creators who want to externalize intuition
* professionals who want reflective decision-making
* researchers exploring human reasoning frameworks
* anyone who thinks better with abstraction + structure

---

## Philosophy: Reasoning as Code

FOWL treats thinking as something that can be:

* version controlled
* improved iteratively
* audited
* replayed
* shared

It is a “Reflective Computing” approach—where you can literally read and analyze your own thought processes.

---

## License

MIT (recommended for public sharing).

---

> Leo Nakayama
