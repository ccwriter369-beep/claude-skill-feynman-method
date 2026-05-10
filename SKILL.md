---
name: feynman-method
version: 0.1.0
---

# Feynman Method — Think From Scratch, Not From Memory

## Purpose

Apply 6 concrete thinking checks before making major decisions, evaluating plans, or building on existing work. Detect cargo cult process (correct form, no substance), tautological explanations (labels masquerading as understanding), and blank-book artifacts (things that received approval without being read). Based on Richard Feynman's documented problem-solving methods.

## When to Use

- Before committing to an architecture, plan, or approach
- When evaluating someone else's work, benchmark, or recommendation
- When a proposed solution feels right but you can't explain why
- When you encounter "best practices" or "industry standard" as justification
- When debugging a system failure that everyone says shouldn't be failing
- When an answer comes too quickly and too confidently

## When NOT to Use

- For straightforward execution of a well-understood task
- When the user wants speed over depth (use direct implementation)
- For creative/generative work where constraints would limit exploration

## The 6 Checks

### Check 1: The Rephrase Test

Take any key claim, explanation, or requirement. Restate it using completely different words, without the original terminology. If the meaning collapses or becomes circular, the original was a label, not understanding.

**Test:** "Without using the word [X], explain what [X] actually does."

**Example:**
- Claim: "We need prompt caching for performance"
- Rephrase: "We need to store the unchanging prefix of our API calls so the provider skips re-processing the same tokens on every request, reducing latency and cost"
- If you can't produce the rephrase, you don't understand the claim well enough to build on it

### Check 2: The Blank Book Test

Before building on, reviewing, or approving any artifact (plan, skill, architecture doc, benchmark result), actually open it and read it. Do not rate based on title, source, or reputation.

**Test:** "Have I personally verified that this contains what it claims to contain?"

**Example:**
- A skill with three reference files titled "MLOps Production Patterns", "LLM Integration Guide", and "RAG System Architecture" — all containing identical boilerplate text. Anyone who checked the titles would think it had comprehensive coverage. Anyone who opened the files would see it was empty.
- Apply to: benchmark scores (did they actually run on this model?), code reviews (did someone read the code?), architecture docs (does the implementation match?)

### Check 3: Estimate Before Calculate

Before running any formula, tool, benchmark, or automated process, make a rough guess at what the answer should be. If the result differs from your estimate by more than an order of magnitude, investigate the process, not your intuition.

**Test:** "Before I run this, what do I expect the answer to be, roughly?"

**Example:**
- Before running an eval suite: "I expect this agent to succeed on about 60% of tasks" — if it reports 95%, something is probably wrong with the eval, not right with the agent
- Before estimating API costs: "20 requests/day at ~1000 tokens each, so maybe $2/day" — if the bill says $200/day, investigate before optimizing

### Check 4: Tautology Detection

When an explanation uses a single word or phrase as its entire justification, demand the mechanism. Replace the label with a step-by-step description of what physically happens.

**Test:** "Can I describe the mechanism without using the label word?"

**Tautology patterns:**
- "It failed because of a race condition" — What specific sequence of events, in what order, caused what state to be wrong?
- "We need microservices for scalability" — What specific bottleneck exists, and how does splitting this particular service remove it?
- "Best practices say to do X" — What specific failure does X prevent, and have we verified that failure is possible in our system?

### Check 5: The 12 Problems Method

Maintain a persistent list of open problems — not tasks, not goals, problems. Real questions you keep circling back to. Test every new technique, tool, or idea against this list.

**Application:** When encountering a new tool, framework, or technique, ask: "Does this connect to any of my open problems?" Connections between unrelated fields are where breakthroughs come from. A spinning plate in a cafeteria connected to electron orbits.

### Check 6: The From-Scratch Question

When encountering existing process, convention, or "the way we do things," ask: "If we were starting from scratch today, with everything we now know, would we build it this way?"

**Test:** "What would we do if this didn't already exist?"

**Cargo cult indicators:**
- Process steps that no one can explain the purpose of
- Tools chosen because "everyone uses them" rather than because they solve a specific problem
- Metrics tracked because they were always tracked, not because they drive decisions
- Rituals that look like the successful version but produce no results (bamboo headphones)

## Applying the Checks

Run checks in this order for maximum efficiency:

1. **Blank Book Test** first — no point analyzing something empty
2. **Rephrase Test** — verify you understand what you're looking at
3. **Tautology Detection** — strip labels from explanations
4. **Estimate Before Calculate** — set expectations before measuring
5. **From-Scratch Question** — challenge inherited assumptions
6. **12 Problems** — connect to your persistent open questions

Not every situation needs all 6. The Blank Book Test and Rephrase Test are fast and catch the most common failures. Use all 6 for high-stakes decisions.

## Additional Resources

- `references/cargo-cult-patterns.md` — Common cargo cult patterns in software engineering, AI/ML, and organizational process
