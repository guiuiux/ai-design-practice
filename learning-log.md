# Git & Version Control Study Log

## Core Concept
**Git is the story of my project.** It creates timelines that allow me to work in a non-destructive way—I can always revert, branch, or explore without losing the original state.

## Fundamental Workflow

### Three-Step Process
1. **Stage** — Add changes to the staging area
2. **Commit** — Lock in those changes with a message
3. **Branch** — Create isolated lines of work

## Mental Model

### Repository Structure
- **`main`** — Base project (stable, tested)
- **Feature branches** — Experimental work, isolated from main
- **Merge when ready** — Only integrate features back to main when confident

### Why This Matters
- **Non-destructive work** — Nothing is permanent until committed
- **Safety for learning** — Especially critical when not yet proficient with tools/agents
- **Training ground** — Safe to experiment with AI workflows before scaling to production code

## Local → Remote

### Local Repository
- Stored in `.git/` folder on my machine
- Full history locally tracked

### Remote Repository (GitHub)
- Created new project on GitHub
- Local repo now connected to remote
- Can push/pull changes between local and remote

## Key Principle
**Always branch before experimenting.** Keep main clean and stable while exploring on feature branches. Only merge back when the feature is solid and tested.

### Best findings
I realized that for my experimental projects I don't need to create a repo in Github, I can start a local repo, do local commits, if the project grows, I can take it to cloud.

## Working with Claude Code

### Branch-First Rule
**Always create a branch before letting Claude do any work.** Claude should never create or edit files while on `main`.

### Workflow
1. **Check branch** — Make sure you're not on `main`
2. **Branch first** — Create a feature branch before any file work begins
3. **Then let Claude work** — Only after branching is confirmed

### Why This Matters
- Keeps `main` clean and stable
- All AI-assisted work stays isolated until reviewed
- Easy to discard or revise without affecting the base project

### Prompting — Be Specific, Not Vague

Tested two approaches while building a navbar component.

**Vague prompt:**
> "make a navbar"

Claude delivered something functional, but generic. No context about the file, the stack, the content, or the look — so the output required follow-up corrections.

**Specific prompt:**
> "Create a navbar in navbar.html. It should have 3 links: Home, Work, Contact. Use only HTML and CSS, no frameworks. Fixed to the top of the page. Background color #1a1a1a, white text, clean and minimal with microinteractions."

First output matched the intent. No back-and-forth needed.

**Why it worked — the prompt covered all five layers:**

| Layer | What it answers |
|---|---|
| **Context** | Standalone file (`navbar.html`), no framework |
| **Task / Action** | Create a navbar |
| **What it contains** | 3 links: Home, Work, Contact |
| **Constraints** | HTML and CSS only, fixed to top |
| **Visual specs / Output** | `#1a1a1a` background, white text, minimal, microinteractions |

**Key takeaway:** The more specific the prompt, the closer the first output is to the intended result. Vague prompts produce generic outputs. Treat Claude like a skilled collaborator — give it the full brief, not just the task title.

---

*Updated: March 16, 2026*
