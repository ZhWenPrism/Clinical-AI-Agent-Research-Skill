# Clinical AI Agent Research Skill

A portable research skill for rigorous work in clinical decision support, diagnostic and prognostic modeling, multimodal patient data, medical machine learning, retrieval-augmented generation, and single- or multi-agent systems.

The skill defines a leakage-safe research workflow from question formulation and cohort design through model evaluation, reporting, and reproducibility. It is designed for research planning and analysis; it does not provide patient-specific diagnosis, treatment, triage, or dosing advice.

## Coverage

- Clinical question, cohort, endpoint, index-time, and prediction-horizon definition
- Patient- and site-level data splitting with explicit leakage controls
- Multimodal modeling across clinical, imaging, waveform, pathology, and molecular data
- Baseline, ablation, calibration, uncertainty, subgroup, and external-validation planning
- RAG and agent evaluation, including tool failure, recovery, auditability, latency, and cost
- Manuscript, reporting-guideline, figure, and reproducibility preparation

## Platforms

The same skill can be installed for Codex and Claude Code.

| Platform | Invocation |
|:---|:---|
| Codex | `$clinical-ai-agent-research` |
| Claude Code | `/clinical-ai-agent-research` |

## Installation

Clone the repository, then run the installer for the required platform. Git is required.

### Windows

```powershell
git clone https://github.com/ZhWenPrism/Clinical-AI-Agent-Research-Skill.git
Set-Location Clinical-AI-Agent-Research-Skill
.\install.ps1 -Target Codex
```

Use `-Target ClaudeCode` or `-Target All` for the other supported targets.

### macOS and Linux

```bash
git clone https://github.com/ZhWenPrism/Clinical-AI-Agent-Research-Skill.git
cd Clinical-AI-Agent-Research-Skill
./install.sh --target codex
```

Use `--target claude` or `--target all` as needed. Both installers can deploy the pinned supporting skills listed in `upstream-skills.lock.json`; pass the documented skip-dependencies option to install only this skill.

## Repository structure

```text
clinical-ai-agent-research/
├── SKILL.md                              # routing rules and core workflow
├── agents/openai.yaml                    # agent metadata
└── references/
    ├── clinical-evaluation.md            # clinical prediction evaluation
    ├── multimodal-and-agent-evaluation.md
    ├── reporting-and-figures.md
    └── upstream-provenance.md
```

`DEPLOYMENT_PROMPTS.md` contains deployment prompts, while `SECURITY.md` defines the project security and disclosure policy.

## Research boundary

Clinical data and unpublished material require explicit authorization and appropriate privacy controls. Patient-level data should be processed locally, with only the minimum necessary schema or aggregate diagnostics exposed to external services. All clinical outputs remain research artifacts subject to qualified human review.

