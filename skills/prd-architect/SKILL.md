---
name: prd-architect
description: Drafts comprehensive, measurable, and execution-ready Product Requirements Documents (PRDs) for design and engineering teams. Trigger this skill whenever the user requests a PRD, product specification, application/feature requirements document, or MVP planning.
---

# PRD Architect

## Role & Objective
Act as a **Senior Product Manager** and **System Architect** experienced in shipping global digital products. Your mission is to convert raw ideas, short briefs, or feature lists into clear, unambiguous, execution-ready Product Requirements Documents (PRDs) suitable for immediate UI/UX design and engineering handoff.

## Workflow

### 1. Evaluate User Input
Check whether the following baseline context is provided:
- Product name or core concept
- Problem statement & target audience
- Target platform(s) (Android, iOS, Web, Desktop, or Cross-platform)
- Core features & monetization model (if applicable)

**Clarification Rules
rm -f CONTRIBUTING.md && \
cat <<'EOF_PRD_SKILL' > README.md
# PRD Architect Skill

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Format: SKILL.md](https://img.shields.io/badge/Format-Agent%20Skill%20(SKILL.md)-green.svg)](#installation)

An open, portable **Agent Skill** (`SKILL.md`) that turns AI coding agents and chat assistants into a **Senior Product Manager & System Architect**. It transforms rough product ideas, feature lists, or short briefs into structured, unambiguous, and execution-ready **Product Requirements Documents (PRDs)**.

---

## Key Features

- **Dual Output Modes:** Supports both **Full PRD (10 sections)** for complete engineering/design handoff and **One-Page MVP PRD (5 sections)** for rapid validation.
- **Smart Clarification Flow:** Asks targeted clarifying questions only when input is critically thin; otherwise fills minor gaps with explicitly tagged `[Assumption]` markers.
- **Precision Standards:** Enforces measurable Acceptance Criteria, MoSCoW prioritization tables, Non-Functional Requirements (NFRs), edge-case handling, and phased roadmaps.
- **Cross-Platform Ready:** Compatible with Agent Skill-enabled CLI/IDE tools (`SKILL.md`), Cursor (`.mdc`), Windsurf, GitHub Copilot, ChatGPT, Claude Projects, and Gemini Gems.

---

## Repository Structure

```text
prd-architect-skill/
├── README.md
├── LICENSE
├── .gitignore
├── skills/
│   └── prd-architect/
│       └── SKILL.md              # Agent Skill
├── adapters/
│   └── cursor/
│       └── prd-architect.mdc     # Ready-to-use Cursor Rule
└── templates/
    ├── full-prd-template.md      # Standalone 10-section PRD template
    └── mvp-prd-template.md       # Standalone One-Page MVP template
```

---

## Installation

### 1. Claude Code / Codex / Gemini CLI / Agent Skill-Compatible Tools
Copy the `prd-architect` skill folder into your agent's skills directory:

```bash
mkdir -p .claude/skills/prd-architect
cp skills/prd-architect/SKILL.md .claude/skills/prd-architect/SKILL.md
```

### 2. Cursor
Copy the pre-formatted rule file into your project's `.cursor/rules/` directory:

```bash
mkdir -p .cursor/rules
cp adapters/cursor/prd-architect.mdc .cursor/rules/prd-architect.mdc
```

### 3. Windsurf / GitHub Copilot
Append the content of `skills/prd-architect/SKILL.md` — excluding the top YAML frontmatter block (`--- ... ---`) — to your `.windsurfrules` or `.github/copilot-instructions.md`.

### 4. ChatGPT (Custom GPT / Projects), Claude Projects, or Gemini Gems
1. Open `skills/prd-architect/SKILL.md`.
2. Copy everything starting from `# PRD Architect` downward (omit the YAML header).
3. Paste into the **System Prompt / Instructions** field.

---

## Usage Examples

Once installed, simply prompt your AI assistant:

- **Full PRD:**
  > *"Create a full PRD for a cross-platform, ad-free audio sharing app with a 10 GB free tier and an unlimited monthly subscription tier."*
- **One-Page MVP PRD:**
  > *"Create a One-Page MVP PRD for an Android daily expense tracker built for university students."*

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.
