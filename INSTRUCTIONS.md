# AI Standards — Shared Context for Your Engineering Organisation

## What Is This?

This is a **single, central repository** that holds all the AI-related knowledge your engineering teams need — coding guidelines, AI agent definitions, business context, and story-level details.

When anything in this repository is updated, the changes are **automatically pushed to every team's codebase** — no manual copy-pasting, no drift between teams.

Think of it as a **single source of truth** that keeps every squad aligned on how AI assistants behave, what coding standards they follow, and what business and technical context they operate with.

---

## How Does It Help?

| Benefit | Description |
|---|---|
| **Consistency** | Every team gets the same coding standards, agent behaviours, and guidelines — automatically. |
| **Squad-specific context** | Each squad (e.g. Inbound, Outbound) can have its own business context and stories, delivered only to the repos that need them. |
| **Zero manual effort** | Once set up, updates flow to all team repositories the moment a change is merged. No tickets, no reminders. |
| **Governance** | Changes go through a single review process — one approval updates every team at once. |
| **Onboarding** | New repositories or squads can be added in minutes by editing a single configuration file. |

---

## What Gets Shared?

- **AI Agent Definitions** — Reusable agent personalities and modes (code review, story writing, planning, etc.) that standardise how AI assistants work across the org.
- **Coding Guidelines** — Language and framework-specific standards (e.g. Java, Python, React, Angular, Go, Kotlin) plus core principles that apply everywhere.
- **Business & Technical Context** — Per-squad documents that give AI assistants the background they need to generate relevant, accurate output.
- **Story-level Details** — Active stories or epics per squad, so AI agents can work with up-to-date requirements.

---

## How It Works (Non-Technical Summary)

1. A team member updates a guideline, agent definition, or context document in this central repository.
2. The change is reviewed and merged through the normal pull-request process.
3. An automated process detects the change and distributes it to all configured team repositories.
4. Every team's AI assistants immediately start using the updated content — no action needed from individual developers.

---

## Prerequisites

Before setting this up in your organisation, ensure the following are in place:

### 1. GitHub Organisation
All participating repositories must live under the same GitHub organisation (or the automation must have cross-org access).

### 2. Repository Access Token
A **Personal Access Token** (or GitHub App token) with write access to all target repositories is required. Your platform or DevOps team can generate this and store it as a secret in this repository.

### 3. Repository List
Identify which repositories belong to which squad. You will need a mapping like:

- **Squad A** → repo-a-frontend, repo-a-backend
- **Squad B** → repo-b-frontend, repo-b-backend

### 4. Initial Content
Prepare the foundational content before rolling out:

- **Coding guidelines** your org wants all teams to follow.
- **Agent definitions** for the AI modes you want to standardise (e.g. code review, story creation).
- **Business context documents** per squad describing the domain each team works in.

### 5. A Maintainer
Assign one or two people (e.g. a Staff Engineer, Tech Lead, or Platform Engineer) to own this repository. They will review and merge changes, and onboard new squads or repos as the org grows.

---

## Adding a New Squad or Repository

To bring a new team on board, the maintainer updates the configuration file with:

- The new repository names.
- Which shared content they should receive.
- Any squad-specific context or story folders.

The next change merged to the main branch will automatically sync everything to the new repositories.

