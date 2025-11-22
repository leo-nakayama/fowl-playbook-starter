# **FOWL Playbook Syntax Cheat Sheet**

A quick reference for designing FOWL reasoning pipelines.

---

## 1. Basic Structure

```yaml
name: <playbook_name>
description: "<short description>"

context:
  ... raw data / events / roles ...

call:
  - module: <ModuleName>
    op: <OperatorName>
    args:
      <key>: <value>
    save_as: <variable>

outputs:
  - <variables from call>

ObservationReport:
  module: ["AristotleFourCauses","TradeoffLens", ...]
  function: "Deduction"
  input: "outputs"
  format: "FOWL-Observation-Report-v1"
```

---

## 2. Design Philosophy

| Layer                 | Purpose                                           |
| --------------------- | ------------------------------------------------- |
| **context**           | MaterialCause: "What exists?"                     |
| **call**              | EfficientCause: "What logic will we apply?"       |
| **outputs**           | FormalCause: "How are results structured?"        |
| **ObservationReport** | FinalCause: "What insight does all this produce?" |

---

## 3. Operator Syntax

```yaml
- module: <Module>
  op: <Operator>
  args:
    key: value
  save_as: <output name>
```

* `args:` mirrors function parameters
* `save_as:` creates reusable variables
* multiple operators can run sequentially

---

## 4. Common Modules & Ops

### AristotleFourCauses

* `O_decompose`
* `O_tracechain`
* `O_telos_check`

### TradeoffLens

* `O_surfaceAxes`
* `O_frontier`
* `O_sensitivity`

### PoliticalDynamics

* `O_detectShadowLine`
* `O_dissolveShadowLine`
* `O_roleShield`

### SyntheticNaikan

* `O_selfReflect`
* `O_contributionMap`
* `O_blindSpotDetect`

---
