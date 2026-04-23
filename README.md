# Agentics NZ Showcase

A curated collection of projects built by the Agentics NZ community using AI agents.

## Categories

- [Built with AI Agents](#built-with-ai-agents) — Applications, tools, and projects created using AI agents
- [Tools for AI Agent Development](#tools-for-ai-agent-development) — Primitives, libraries, and infrastructure that help build AI agents

---

## Built with AI Agents

Projects in this section are full applications, products, and prototypes built *using* AI agents as part of the development workflow.

---

### Sad Salaryman

![Sad Salaryman](screenshots/sad-salaryman.png)

A gamified object scanning app where you earn "burden" as an unpaid intern.

**Description:** Turn your life into a corporate simulation. Scan everyday objects to earn burden, track your progress through corporate ranks, and climb from Unpaid Intern to Contractor.

**Stack:** TBD

**Builder:** [Waylon Kenning](https://kenning.co.nz)

**Links:**
- 🌐 Live: [sadsalaryman.com](https://sadsalaryman.com)

---

### InsureScan NZ

![InsureScan NZ](screenshots/insurescan.png)

AI-powered home contents valuation for insurance.

**Description:** Identify, value, and catalog your home contents in minutes with AI. Snap photos of items, get instant NZ pricing with GST included, and export professional PDF inventories for insurance claims.

**Stack:** TBD

**Builder:** [Waylon Kenning](https://kenning.co.nz)

**Links:**
- 🌐 Live: [insurescan.website](https://insurescan.website)

---

### Scenia

![Scenia](screenshots/scenia.png)

IT Portfolio Planning & Visualisation.

**Description:** Map initiatives across time, sequence dependencies, track costs, and report on progress. A visual timeline tool for IT portfolio planning with conflict detection, critical path analysis, and budget visualisation.

**Stack:** React, TypeScript, Vite, Tailwind, IndexedDB (Dexie)

**Builder:** [Waylon Kenning](https://kenning.co.nz)

**Links:**
- 🌐 Live: [scenia.website](https://scenia.website)
- 🐙 GitHub: [waylonkenning/scenia](https://github.com/waylonkenning/scenia)

---

### Iris

![Iris](screenshots/iris.png)

Integrated Repository for Information & Systems — a web-based architectural modeling tool.

**Description:** Create, manage, and version architectural entities, relationships, and diagrams in a repository-first system where entities are the source of truth and diagrams are projections. Supports Simple View, UML, ArchiMate, and sequence diagrams with an interactive knowledge graph, collections and sets, audit logging, and full keyboard accessibility (WCAG 2.2 AA).

**Stack:** SvelteKit, Svelte 5, @xyflow/svelte, Tailwind CSS v4, FastAPI, SQLite / Supabase (PostgreSQL), Argon2id + JWT auth

**Builder:** [Chris Barlow](https://github.com/cgbarlow)

**Links:**
- 🌐 Live: [Iris UAT](https://iris-uat.chrisbarlow.nz/)
- 🐙 GitHub: [cgbarlow/iris](https://github.com/cgbarlow/iris)

---

### Guild Hall

![Guild Hall](screenshots/guild-hall.png)

A quest-based engagement platform that reframes community participation around adventure rather than obligation.

**Description:** Game Masters design quests with objectives, deadlines, and difficulty levels. Community members accept quests from a Bounty Board, submit evidence to complete objectives, and earn points and skill tier progression. Built on the philosophy that "obstacles are expected" on quests, whereas goals frame struggle as failure.

**Stack:** Next.js 15, React 18, TypeScript, Tailwind CSS, shadcn/ui, Supabase, TanStack Query, React Hook Form, Zod, Vitest, Netlify

**Builder:** [Chris Barlow](https://github.com/cgbarlow)

**Links:**
- 🌐 Live: [guildhall.agentics.org.nz](https://guildhall.agentics.org.nz)
- 🐙 GitHub: [cgbarlow/guild-hall](https://github.com/cgbarlow/guild-hall)

---

### Matariki Stellar Navigator

![Matariki Stellar Navigator](screenshots/matariki.png)

An interactive web experience celebrating Matariki, the Māori New Year.

**Description:** Explore the nine stars of the Matariki cluster through an interactive navigator that pairs traditional stories and cultural significance with a guided star-finding experience. Built with respect for Māori culture and traditions.

**Stack:** JavaScript, HTML, CSS, Netlify

**Builder:** [Chris Barlow](https://github.com/cgbarlow)

**Links:**
- 🌐 Live: [matarikinav.netlify.app](https://matarikinav.netlify.app)
- 🐙 GitHub: [cgbarlow/matariki](https://github.com/cgbarlow/matariki)

---
### SPAFW37 (Simple Python Application Framework for Python 3.7 - pronounced "Spafoo 37")

A lightweight Python 3.7 framework for CLI application development, constructed using Copilot Coding Agent.

**Description:** A framework for constructing simple Python command line utilities through declaring parameters and commands as Dicts, and linking them to executor functions:

```python
# Define parameters
params = [
    {
        PARAM_NAME: 'name',
        PARAM_DESCRIPTION: 'Name to greet',
        PARAM_ALIASES: ['--name', '-n'],
        PARAM_DEFAULT: 'World',
    }
]

# Define command action
def greet():
    name = spafw37.get_param('name')
    print(f"Hello, {name}!")

# Define commands
commands = [
    {
        COMMAND_NAME: 'greet',
        COMMAND_DESCRIPTION: 'Greet someone',
        COMMAND_ACTION: greet,
    }
]

# Register and run
spafw37.add_params(params)
spafw37.add_commands(commands)

if __name__ == '__main__':
    spafw37.run_cli()
```

**What's the Agentic angle?**

Because:

1. It was developed almost *entirely* by writing requirements in GitHub tickets, and assigning them to GitHub Coding Agent, or by using Agentic workflows in CoPilot Chat
2. Because in doing so it was used to debug, diagnose, and develop the initial constraints, rules and workflows for CoPilot that have formed the basis for *all* my subsequent AI work
3. Because it continues to be useful as a way to produce lightweight Python tools that can be used by Claude Skills and Plugins to consolidate their scripting requirements and provide a common interface schema, instead of ad-hoc scripts spread out all over the place

The meat for us is actually in the `features/` folder and the `.github/prompts` folder:

- `.github/prompts` contains the workflow prompts for planning features in a way that builds an implementation plan across multiple cumulative steps
- `features/` contains plans created using those prompts, used as input for the final step of the workflow to produce working implementation, tests and documentation, with the plan file serving as an as-built for the application.

Note that these workflows are effectively a museum piece now - when a plan reaches a certain size, it explodes the context and becomes unworkable. But they're the springboard from which other work flows.

**Stack:** GitHub CoPilot Chat, GitHub Copilot Coding Agent

**Builder:** [Ciara Norrish](https://github.com/minouris)

**Links:**
- 🌐 Live: [https://pypi.org/project/spafw37/](https://pypi.org/project/spafw37/)
- 🐙 GitHub: [https://github.com/minouris/spafw37](https://github.com/minouris/spafw37)

## Tools 

Projects in this section are libraries, frameworks, and tooling that help creators.

---

### Campaign Mode

![Campaign Mode](screenshots/campaign-mode.jpg)

Assemble a party of AI advisors with genuinely different perspectives.

**Description:** A plugin system for Claude Desktop and Claude Code CLI that frames collaborative problem-solving as a quest. Six animal-based agents provide distinct viewpoints while three NPC characters (Gandalf, Guardian, Dragon) offer mentorship, progress evaluation, and adversarial testing — helping surface blind spots and stress-test ideas before they matter. Built on the Six Animals framework with Markdown-based persistence for campaign state.

**Stack:** Claude Desktop / Claude Code plugin, Markdown persistence (`.campaign/quest.md`), CC-BY-SA-4.0

**Builder:** [Chris Barlow](https://github.com/cgbarlow)

**Links:**
- 🐙 GitHub: [cgbarlow/campaign-mode](https://github.com/cgbarlow/campaign-mode)

---

### Machine Dream

![Machine Dream](screenshots/machine-dream.jpg)

A continuous AI cognition platform that lets models learn from experience and consolidate knowledge across sessions.

**Description:** Uses Sudoku as a research testbed to implement a learning loop where AI plays puzzles, makes mistakes, "dreams" (consolidates experiences into patterns), and improves over time — with no external hints or deterministic fallbacks. Implements the GRASP Loop (Generate → Review → Absorb → Synthesize → Persist) with three clustering algorithms: FastCluster, DeepCluster, and LLMCluster.

**Stack:** TypeScript, Node.js 20+, SQLite, OpenAI-compatible APIs (LM Studio, OpenAI, Anthropic, Ollama, OpenRouter)

**Builder:** [Chris Barlow](https://github.com/cgbarlow)

**Links:**
- 🐙 GitHub: [cgbarlow/machine-dream_AG](https://github.com/cgbarlow/machine-dream_AG)

---

### ADR (WH(Y) Method)

![ADR](screenshots/adr-why.webp)

An enhanced Architecture Decision Record format for AI-assisted development teams.

**Description:** Addresses structural inconsistency and the conflation of decision rationale with implementation details in existing ADR practice. Provides standardised templates, dependency tracking between decisions, and governance metadata so humans and AI agents can capture and maintain architectural choices with clarity. Language-agnostic and designed to integrate with ADR tooling via options like `adr new --mode=enhanced`.

**Stack:** Markdown specification, language-agnostic templates

**Builder:** [Chris Barlow](https://github.com/cgbarlow)

**Links:**
- 🐙 GitHub: [cgbarlow/adr](https://github.com/cgbarlow/adr)

---

### MNEMOS

![MNEMOS](screenshots/mnemos.png)

A containerised, contract-governed memory and retrieval service for AI-native applications.

**Description:** MNEMOS provides a unified, domain-agnostic memory layer featuring TurboQuant 4-bit compression, forensic PostgreSQL audit ledgers, configurable semantic routing tiers, and a conditional Cross-Encoder reranking lane. It abstracts away brittle embeddings and database glue code into a robust REST API and Python SDK, built primarily as an appliance for autonomous agents requiring persistent, scalable cognition.

**Stack:** Python, FastAPI, Qdrant, PostgreSQL, pgvector, Docker, CUDA, BAAI/bge-base

**Builder:** MNEMOS Contributor

**Links:**
- 🐙 GitHub: [ro0TuX777/MNEMOSv2](https://github.com/ro0TuX777/MNEMOSv2)

---

## Adding Your Project

To add a project to the showcase:

1. Fork this repository
2. Add your entry to the appropriate section using the format below
3. Submit a pull request

### Entry Format

```markdown
### Your Project Name

![Your Project Name](screenshots/your-project.png)

One-paragraph description of what it does.

**Description:** A longer description if needed.

**Stack:** Tech stack (e.g. React, Python, Claude API)

**Builder:** Your name or company

**Links:**
- 🌐 Live: https://...
- 🐙 GitHub: https://github.com/...
```

### Screenshot Guidelines

- Max dimensions: 1200px wide
- Format: PNG or JPG
- File name: `{project-name}.png` in the `/screenshots` folder
- Add the image reference right after your project title
