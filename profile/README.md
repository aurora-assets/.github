# Aurora Lens

Inference-time governance for large language models.

Aurora Lens is a runtime enforcement layer for LLM systems. It sits between the model and the application, evaluates whether output is admissible, and records the outcome in a structured audit trail.

It was built to address a persistent failure in deployed language systems: fluent output presented as legitimate knowledge under uncertainty, ambiguity, or missing evidence.

## What Aurora Lens does

Aurora Lens governs model output at runtime.

It intercepts responses before delivery, applies deterministic checks, and decides whether the output may pass, must be corrected, should be revised, or must be blocked.

Core properties:

- runtime admissibility enforcement
- refusal as a valid terminal outcome
- explicit handling of ambiguity and insufficient evidence
- structured intervention outcomes
- forensic audit records for governed inference
- model-agnostic deployment surface

## Why this exists

Most AI evaluation work happens before deployment or after failure.

Aurora Lens addresses the missing middle:

**inference-time governance**

The question is not whether a model can produce a plausible answer.

The question is whether that answer is legitimate under the available evidence, the present uncertainty, and the applicable policy constraints.

Aurora Lens treats that as an enforceable runtime problem.

## What makes it different

Aurora Lens is not a benchmark, not a monitoring dashboard, and not a prompt wrapper.

It is a governance layer.

Its purpose is to control what an LLM is permitted to say in live operation, and to leave behind a deterministic record of what happened and why.

## Public materials

- **PyPI package** — install and evaluate Aurora Lens
- **Technical overview** — architecture and system positioning
- **Empirical evidence** — governed vs. ungoverned failure cases
- **Research paper** — epistemic legitimacy as a governance layer for LLM systems
- **Acquisition overview** — consolidated public-facing asset summary

## Start here

- `acquisition-overview` — overview of the product, assets, and contact path
- PyPI — `pip install aurora-lens`

## Who this is for

Aurora Lens is relevant to teams building or evaluating LLM systems where unsupported output creates operational, legal, regulatory, or safety risk.

Typical contexts include:

- regulated workflows
- audit-sensitive environments
- enterprise AI deployment
- clinical, legal, and compliance-adjacent use cases
- systems requiring explicit refusal under uncertainty

## Architecture note

Aurora Lens is built on a deeper deterministic governance architecture for admissibility, refusal, and audit. That internal structure exists to make runtime decisions legible, enforceable, and reviewable.

The public product surface is Aurora Lens.

## Contact

For evaluation, technical discussion, licensing, or acquisition interest:

**Margaret Stokes**  
margaret.stokes.ai@gmail.com

## External links

- **PyPI:** https://pypi.org/project/aurora-lens/
- **Research:** https://zenodo.org/records/18719033
- **Website:** https://milamba.com/aurora-lens.html

Margaret Stokes — [milamba.com/aurora-lens.html](https://milamba.com/aurora-lens.html)
