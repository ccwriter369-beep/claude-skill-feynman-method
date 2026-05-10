# Feynman Method — Claude Code Skill

A Claude Code skill that applies Richard Feynman's documented problem-solving methods before making decisions, evaluating plans, or building on existing work.

## What It Does

Runs 6 concrete thinking checks that catch the most common failure modes in software development:

| Check | Catches |
|-------|---------|
| **Blank Book Test** | Artifacts rated by title/reputation without being read |
| **Rephrase Test** | Labels masquerading as understanding |
| **Tautology Detection** | Explanations that use the label word as the explanation |
| **Estimate Before Calculate** | Results accepted without a prior expectation to test against |
| **From-Scratch Question** | Inherited process nobody can explain the purpose of |
| **12 Problems Method** | New tools evaluated in isolation from real open problems |

## Install

```bash
npx claude-skills add https://github.com/ccwriter369-beep/claude-skill-feynman-method
```

Or manually copy `SKILL.md` into `.claude/skills/feynman-method/SKILL.md` in your project.

## Usage

```
/feynman-method
```

Invoke before committing to an architecture, evaluating someone else's work, or when a solution feels right but you can't explain why.

## When to Use It

- Before committing to an architecture, plan, or approach
- When evaluating a benchmark, recommendation, or "best practice"
- When a proposed solution feels correct but you can't articulate why
- When debugging a system failure that everyone says shouldn't be failing
- When an answer comes too quickly and too confidently

## The Bamboo Headphones Problem

Feynman's cargo cult science lecture described Pacific islanders who built bamboo runways and headphones after WWII — correct form, no substance. The planes never came.

The same pattern runs through software: cargo cult testing (coverage metrics without correctness checks), cargo cult architecture (12 microservices for 50 requests/day), cargo cult agile (the ceremony happens, nothing changes).

See [`references/cargo-cult-patterns.md`](references/cargo-cult-patterns.md) for a full catalog of patterns in software engineering, AI/ML, and organizational process.

## Origin

Generated from a YouTube transcript using the [`transcript-to-skill`](https://github.com/ccwriter369-beep/claude-skill-transcript-to-skill) pipeline, then forgotten about. Discovered by accident — browsing the skill list while stuck on a difficult problem, applied it, it worked. Used consistently since. The two checks that come up most in practice: **Blank Book** (catching when you're about to build on something you haven't actually verified) and **Tautology Detection** (stripping labels from bug explanations to find the actual mechanism).

## License

MIT
