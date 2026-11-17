# Trauma Transfusion

**An Agent Skill for teaching, massive hemorrhage protocol review, and transfusion quality audits.**

[Português](README.md) · [Installation](#installation) · [Workflow](#review-workflow) · [Skill instructions](SKILL.md)

Use the skill to locate and cite evidence, flag decisions that need local validation, and tailor the deliverable to three use cases.

| Use case | What the skill helps produce |
| --- | --- |
| Teaching | Evidence summaries, study comparisons, and fictional simulation cases |
| Protocol review | A comparison of documented practice, guideline recommendations, and proposed changes |
| Quality audit | Measures with a defined population, numerator, denominator, data source, and timestamps |

> [!IMPORTANT]
> This skill supports education and review. In clinical care, follow the current institutional protocol and involve the trauma and transfusion teams according to the local workflow.

## Review workflow

The workflow follows a request from the initial question to a referenced deliverable and items for local validation.

![Review workflow with paths for teaching, protocol review, and quality audit](assets/review-workflow.svg)

## Installation

### Agents with terminal access

With Node.js and npm available, run this command from your project directory. The installer offers compatible agents.

```bash
npx skills add jocielle-tech/transfusao-no-trauma --skill transfusao-no-trauma
```

To install the skill for all agent targets recognized by the CLI in the project:

```bash
npx skills add jocielle-tech/transfusao-no-trauma --skill transfusao-no-trauma --agent '*' -y
```

Add `-g` to install at user scope. To target one agent, replace `'*'` with its identifier.

| Agent | `--agent` identifier |
| --- | --- |
| OpenAI Codex | `codex` |
| Claude Code | `claude-code` |
| Cursor | `cursor` |
| GitHub Copilot | `github-copilot` |
| Gemini CLI | `gemini-cli` |
| Google Antigravity | `antigravity` |
| OpenCode | `opencode` |
| Windsurf | `windsurf` |
| Cline | `cline` |
| Roo Code | `roo` |
| OpenClaw | `openclaw` |

See the [current agent list](https://github.com/vercel-labs/skills/blob/main/docs/agents.md) and the [CLI reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md).

### Manual installation or upload

```bash
git clone https://github.com/jocielle-tech/transfusao-no-trauma.git
```

Copy the `transfusao-no-trauma` folder into the skill directory recognized by your agent. Project-level examples include `.agents/skills/` for Codex and `.claude/skills/` for Claude Code. For Claude on the web or desktop, ZIP the skill folder and upload it under **Customize → Skills** if your account supports uploads. Discovery and activation vary by product. [Agent Skills specification](https://agentskills.io/specification) · [Claude guide](https://support.claude.com/en/articles/12512180-use-skills-in-claude)

## Example prompts

Include the setting, audience, and desired format in your request. For protocol reviews and audits, provide available documents and de-identified data.

**Prepare a teaching session**

> Use the transfusao-no-trauma skill to plan a 30-minute session for residents on prehospital transfusion. Summarize the evidence, cite sources, and propose three discussion questions. Answer in English.

**Review a protocol**

> Compare the activation and cessation criteria in the attached protocol with the ACS guideline. Show documented practice, recommendations, proposed changes, and items for the transfusion service to validate. Identify missing information.

**Plan an audit**

> Propose measures for time from activation to first transfusion and the disposition of issued blood components. Define the population, numerator, denominator, data source, and timestamps.

**Create a simulation**

> Create a fictional trauma hemorrhage case for a team discussion. Include information revealed in stages, participant questions, references, and points that depend on the local protocol.

## Clinical source

American College of Surgeons Trauma Quality Programs. *Best Practices Guidelines for Transfusion in Trauma*. November 2026. Verify the applicable edition and page references before relying on thresholds, physiological targets, doses, or compatibility details. [ACS guideline index](https://www.facs.org/quality-programs/trauma/quality/best-practices-guidelines/) · [November 2026 PDF](https://www.facs.org/media/4y2arm2q/acs-tqp-best-practices-for-transfusion.pdf)
