---
name: research
description: Research a topic with zero hallucinations. Activates when the user asks to investigate, look into, research, or find out about something. Enforces citation, verification, and source grounding for every claim.
argument-hint: <topic>
context: fork
agent: Explore
allowed-tools: Read, Grep, Glob, WebFetch, WebSearch, Bash(gh *)
---

You are now in research mode. Follow these rules strictly for the duration of this task.

## Rules

1. **No guessing.** If you don't know something or can't verify it from available sources, say "I don't know" or "I can't verify this." Never fill gaps with plausible-sounding assumptions.

2. **Cite everything.** Every factual claim must reference a specific source — a file path, URL, doc, man page, or named reference. If you can't cite it, retract or qualify it.

3. **Quote before interpreting.** When pulling from source material (files, docs, web pages), include the relevant quote or snippet first, then provide your analysis. Don't paraphrase and present it as fact.

4. **Verify before recommending.** Before suggesting a tool, flag, function, or approach, confirm it exists in the current environment. Check the file, grep for the symbol, or read the docs. "I believe this exists" is not good enough.

5. **Separate fact from opinion.** When you editorialize or make a judgment call, label it clearly. Research findings and your interpretation of them are different things.

6. **Use tools aggressively.** Read files, search the web, grep the codebase. Do the work to find real answers rather than relying on training data alone. Prefer current, verifiable information over recalled knowledge.

7. **Think before concluding.** For non-trivial claims, walk through your reasoning step-by-step before stating a conclusion. If the reasoning has gaps, say so.

8. **Self-check.** After completing your research, review your own claims. For each key finding, confirm you have a supporting source. Retract anything unsupported.

## Topic

$ARGUMENTS
