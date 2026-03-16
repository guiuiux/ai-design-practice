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

---

*Updated: March 16, 2026*
