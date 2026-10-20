# Hardware-Aware Test Generation for Embedded C with LLMs — A Systematic Review

> **Status:** Unregistered systematic review (PRISMA 2020 format, no compliance claim). No bibliographic database search is documented, and no quality-assessment instrument was applied.

## Overview

Embedded C correctness depends on the hardware the code drives — registers, interrupts, DMA and timing — which software-level test harnesses never exercise. This review synthesises how large language models (LLMs) are used for **hardware-aware test generation in embedded C**, joining two literatures that have not previously met:

1. Non-LLM firmware re-hosting and fuzzing
2. LLM-driven test generation

The review is organised around **nine research questions**.

## Methodology at a Glance

| Item | Detail |
|---|---|
| Reporting format | PRISMA 2020 (no compliance claim) |
| Registration | None |
| Database search | Not documented |
| Records screened | 105 registered records |
| Exclusions | 59 |
| Inclusions | 46 |
| Unique studies | 28 (29 reports) |
| LLM-construct studies | 13 — these denominate every LLM-population statement |
| Per-question datasets | N = 4–8 (derived gap analysis: N = 6) |
| Quality assessment | None applied |
| Quantitative meta-analysis | Not possible on the source evidence |

Each research question was answered from **its own verified dataset**. Every "zero" reported below is bounded to that verified dataset and **licenses no prevalence claim**.

## Key Findings

### Test types are bimodal
- Unit tests: **2/4**
- HIL / system-level: **2/4**
- Integration and regression: **0/4**
- Only **1/4** emits C test code

### Prompting and input strategies
- Zero-shot prompting: **6/7**
- Retrieval-augmented generation (RAG): **5/7**
- Agentic workflows: **4/7**
- Hardware-specification categories as model input: **0/8** across eleven categories

### Hardware awareness
- Dependency handling is *delegated, not generated* (**5/6**); behaviourally faithful doubles: **0 of 27** configurations
- LLM-driven interrupt/timing test generation: **0/6**
- Execution is emulator-bound (**6/6**); real hardware as primary target: **0/6**
- Loops close universally (**5/5**) — but only on software signals

### Evaluation practice
Each of the following is **0/4**:
- Real hardware
- HIL
- Fault seeding
- Fault exposure
- Human evaluation
- Common benchmark
- Baseline
- Quantified metric
- Evaluation environment

### Study-set overlap
**14 of 28** pairwise study-set overlaps are zero. No study is simultaneously:
- LLM-based
- Test-generating
- Embedded-C-source-level
- Hardware-aware

### Author-acknowledged gaps
- Hardware-free validation: **5/6**
- Narrow advisory LLM capability: **5/6**
- Peripheral dependence: **4/6**

## Interpretation

The structure indicates a **pre-paradigm intersection**, not a failing literature. The absence of studies combining LLM-based, test-generating, embedded-C-source-level and hardware-aware approaches marks an open research frontier rather than a deficiency in existing work.

## Repository Contents

```
.
├── Abstract.txt        # Review abstract (source of this README)
└── README.md           # This file
```

## Citation

If you reference this review, please cite the accompanying abstract. *(Add full citation details here.)*

## License

*(Add license information here.)*
