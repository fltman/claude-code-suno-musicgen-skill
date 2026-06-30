# Suno Music Generation Skill for Claude Code

[![Support me on Patreon](https://img.shields.io/badge/Patreon-Support%20my%20work-FF424D?style=flat&logo=patreon&logoColor=white)](https://www.patreon.com/AndersBjarby)

A Claude Code skill and subagent that turn song ideas into Suno-ready packages: a 300-character style description plus tagged lyrics formatted for Suno AI music generation.

## What it does

- **`suno-music` skill** — generates a Suno song package: exactly 300 characters of style description (genre, instruments, vocals, tempo, mood) and structure/vocal-tagged lyrics (`[Intro]`, `[Verse]`, `[Chorus]`, `[Male Vocal]`, etc.).
- **`suno-songwriter` agent** — a proactive songwriter/producer subagent that writes the lyrics and style, and can optionally drive Chrome to navigate to Suno and fill in the fields (you click Create/Download).

## Setup

Drop the contents into your Claude Code config:

- Skill: `skills/suno-music-skill/SKILL.md` → `~/.claude/skills/` (or a project `.claude/skills/`)
- Agent: `agents/suno-songwriter.md` → `~/.claude/agents/` (or a project `.claude/agents/`)

Then ask Claude to write a song and it will use the skill automatically.

## Tech

Claude Code skill (`SKILL.md`) + subagent definition (Markdown frontmatter).
