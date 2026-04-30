# Nove Requirements

This repository provides one reusable subagent and five supporting skills for requirements engineering (for Codex and Claude Code).
It supports step-by-step, traceable requirements analysis and specification workflows.

## What Is Included

- 🤖 `requirements-engineer`: subagent that guides requirements analysis and spcification work step by step
- 🧩 `context-modeling`: skill for defining the system boundary and external actors
- 🧩 `use-case-modeling`: skill for deriving actor goals and use cases
- 🧩 `domain-modeling`: skill for identifying domain concepts and relationships
- 🧩 `system-responsibility-modeling`: skill for describing system responsibilities
- 🧩 `requirement-specification`: skill for writing functional and non-functional requirements

Repository structure:

```text
codex/
  agents/
    requirements-engineer.toml
  skills/
    context-modeling/
    use-case-modeling/
    domain-modeling/
    system-responsibility-modeling/
    requirement-specification/
claude-code/
```

## What the Subagent and Skills Generate

Through iterative interaction with the user, the `requirements-engineer` subagent and skills produce approved artifacts in the following structure:

```text
requirements-analysis-<task-name>/
  context-model.md
  use-case-model.md
  domain-model.md
  system-responsibility-model.md
  requirements-specification/
```

## Quick Start

### Common (Clone)

1. Clone this repository.
2. Move to the repository root.

```bash
git clone https://github.com/nove-ai-lab/Nove-Requirements.git
cd Nove-Requirements
```

### for Codex

#### Global install (`~/`)

```bash
mkdir -p ~/.codex
cp -R codex/. ~/.codex/
```

#### Project-local install (`<project-dir>/`)

```bash
mkdir -p <project-dir>/.codex
cp -R codex/. <project-dir>/.codex/
```

#### Usage

Spawn `requirements-engineer` subagent, and describe your development goal.
The `requirements-engineer` subagent will orchestrate five skills.

```bash
cd <project-dir>
codex
Spawn requirement-engineer subagent
I want to develop a team task management web app. Analyze and Specify requirements.
```

Or use one skill directly based on your current needs:
   - `$context-modeling`
   - `$use-case-modeling`
   - `$domain-modeling`
   - `$system-responsibility-modeling`
   - `$requirement-specification`

```bash
cd <project-dir>
codex
$context-modeling Perform context modeling for a team task management web app.
```





### for Claude Code

It will be updated later.

