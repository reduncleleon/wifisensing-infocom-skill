# Wi-FiSensing INFOCOM Skill

A Codex skill for drafting, revising, and critiquing INFOCOM-style Wi-Fi sensing papers.

This skill distills narrative structures, section blueprints, and writing patterns from a local corpus of representative Wi-Fi sensing systems, including `AutoLoc`, `DuTrack`, `Secur-Fi`, `UNI-FI`, and `WSTrack`. It is designed for research on CSI-based sensing, device-free tracking, localization, multimodal Wi-Fi fusion, unified sensing frameworks, and secure wireless sensing.

## What It Does

`wifisensing-infocom-skill` helps authors write wireless sensing papers with the deployment-driven style commonly seen in INFOCOM Wi-Fi sensing work. Instead of producing generic academic prose, it emphasizes:

- practical deployment motivation
- physical intuition behind wireless or multimodal signals
- clear challenge-solution decomposition
- named mechanisms tied to concrete system modules
- commodity-device validation and quantitative evaluation

The goal is to help a paper read like a coherent system contribution: the application motivates the gap, the gap exposes technical challenges, each challenge maps to a concrete mechanism, and the evaluation validates the system under realistic conditions.

## When To Use It

Use this skill when writing or revising papers about:

- CSI-based device-free sensing
- indoor tracking or localization
- Wi-Fi Doppler, AoA, ToF, or phase-based sensing
- multimodal Wi-Fi sensing with acoustic or other sensors
- calibration-free or low-effort sensing systems
- unified frameworks for wireless sensing tasks
- secure or privacy-preserving wireless sensing

It is especially useful for drafting or improving:

- abstracts
- introductions
- preliminaries
- basic idea or system overview sections
- system design sections
- implementation and evaluation sections
- contribution bullets
- paper framing and reviewer-facing logic

## Repository Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── corpus-patterns.md
    └── section-blueprints.md
```

- `SKILL.md` defines the skill behavior, workflow, writing rules, and output expectations.
- `references/corpus-patterns.md` summarizes the recurring narrative and technical patterns from the reference paper corpus.
- `references/section-blueprints.md` provides compact templates for common paper sections.
- `agents/openai.yaml` contains an agent configuration for using the skill with OpenAI-compatible agents.

## Core Writing Pattern

The skill encourages a front-half paper structure like this:

1. Start from a practical deployment scenario, such as smart homes, health monitoring, privacy, or ubiquitous services.
2. Explain why Wi-Fi sensing is attractive, especially compared with cameras, wearables, or dedicated infrastructure.
3. Identify one sharp deployment gap, such as calibration effort, drift, limited devices, weak signals, poor scalability, or sensing security.
4. Reduce the gap to two or three mechanism-level challenges.
5. Pair each challenge with a named insight, model, algorithm, or pipeline.
6. Close the story with prototype implementation and quantitative results on commodity devices when available.

## Example Prompts

```text
Use the Wi-FiSensing INFOCOM skill to rewrite this introduction in an INFOCOM-style challenge-solution structure.
```

```text
Draft an abstract for a CSI-based indoor localization system that does not require manual calibration.
```

```text
Critique this system design section and identify whether each module is tied to a deployment challenge.
```

```text
Turn these technical ideas into three parallel contribution bullets for an INFOCOM submission.
```

## Design Principles

This skill follows several constraints to keep the writing faithful to practical Wi-Fi sensing papers:

- Preserve the user's actual technical contribution instead of forcing it to mimic an unrelated reference paper.
- Tie signal features, equations, and modules to physical or systems constraints.
- Prefer two or three strong challenges over a long list of weak claims.
- Keep contribution bullets parallel: model or theory, method or system, implementation or evaluation.
- Do not fabricate prototype, commodity-device, or quantitative claims when they are not supported by the user's work.
