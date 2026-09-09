# No AI Slop

Remove 25 patterns of AI slop from your writing without flattening your personal voice.

https://github.com/user-attachments/assets/f3055450-78eb-4672-880a-88a4fa54bde9

## Problem

AI makes it easy to generate clean writing that all sounds the same. Even the best models keep producing lines like:

- “It’s not X. It’s Y.”
- “What nobody tells you is…”
- “The future isn’t coming. It’s already here.”

When you use AI to edit, it can also smooth away the vocabulary, cadence, humor, and imperfections that make the writing sound like you.

This is chkiss's fork of [yunyu/no-ai-slop](https://github.com/yunyu/no-ai-slop), which is itself a fork of [petergyang/no-ai-slop](https://github.com/petergyang/no-ai-slop).

From yunyu: punch sentences, vague significance verbs, stock-metaphor equations, anthropomorphized non-agents, and colon-plus-list elaborations.

Added here:

- **Explanatory tails.** A sentence that earns its place, followed by one that restates it, justifies it, or spells out its implication. Cutting is the fix, not shortening.
- **Directive tails.** A fact or quote followed by an instruction on how to react to it — "so don't apologize for it." The briefing-document version of the explanatory tail.
- **Spelled-out numbers.** Numerals for anything two digits or larger. A fraction in words is usually a percentage trying to get out.
- **Negative fragments.** Extends negative listing to a lone fragment appended for emphasis, while keeping one that rules something out the reader would otherwise assume.
- **Headings get the pass too.** Metadiscourse hides in headings, section labels and bold list lead-ins because it reads as structure. Added as workflow step 0, the most-skipped step.
- **A pass applies to a version, not a file.** Sections written after an earlier pass are where slop most reliably survives, so re-run on anything added since.

## How to install No AI Slop

The easiest way to install the skill is to paste this into ChatGPT, Claude Code, Codex, or your favorite coding agent:

```text
Install the /no-ai-slop skill globally from https://github.com/chkiss/no-ai-slop
```

You can also install it with `npx`:

```sh
npx skills add chkiss/no-ai-slop --skill no-ai-slop --global --yes
```

## How to use No AI Slop

### Edit your writing

```text
/no-ai-slop (your writing)
```

The skill removes the AI slop patterns, preserves your personal voice, and lists what it changed.

### Detect slop

```text
/no-ai-slop is this slop? (your writing)
```

The skill quotes every slop pattern it found without guessing whether AI wrote the text.

### Generate slop for fun

```text
Draft an AI slop post about (topic)
```

Use it to generate the most cringe AI slop possible as satire.

## The slop that this skill catches

25 patterns:

1. **Binary contrasts.** "It's not X. It's Y."
2. **Throat-clearing openers.** "Here's the thing," "Let me be clear"
3. **Faux-insight setups.** "What nobody tells you," "The part everyone misses"
4. **Colon reveals.** "The best part: it learns."
5. **Superficial analysis.** "...highlighting the team's commitment to innovation"
6. **Importance puffery.** "marks a pivotal moment," "a testament to"
7. **Vague significance verbs.** "X matters," "what really counts is X"
8. **Stock-metaphor equations.** "Speed is their superpower."
9. **Anthropomorphized non-agents.** "the roadmap wants to prioritize retention"
10. **Directive tails.** A fact, then an instruction on how to react to it.
11. **Interpretive metadiscourse.** "That last part matters more than it sounds."
12. **Weasel attribution.** "experts agree," "studies show"
13. **Fake-strong verbs.** "serves as a centralized hub"
14. **Synonym cycling.** "The agent handles your email. The assistant drafts replies."
15. **Negative listing.** "Not a X. Not a Y. A Z."
16. **Dramatic fragmentation.** "That's it. That's the whole thing."
17. **Punch sentences.** "It worked." "Nothing was lost."
18. **Explanatory tails.** A sentence, then a second one restating it.
19. **Spelled-out numbers.** "sixteen accounts" for "16 accounts"
20. **Robotic rhythm.** Repeated sentence shapes and stacked fragments.
21. **Rhetorical setups.** "What if I told you...", "Plot twist:"
22. **Fake-profound kickers.** "The future isn't coming. It's already here."
23. **Summary-recap endings.** "In conclusion," "Ultimately,"
24. **Formatting slop.** Emoji headings, decorative bold, bullets that should be prose.
25. **Em dashes.** Used as a default rhythm crutch.

It also checks the fundamentals: Lead with the point when that helps, use active voice, untangle hard-to-follow sentences, and prefer concrete details over abstractions.

## What’s inside

- [`SKILL.md`](skills/no-ai-slop/SKILL.md) contains the editing rules and workflow.
- [`eval.md`](skills/no-ai-slop/eval.md) contains the checks the skill runs on its work.
- [`.codex-plugin/plugin.json`](.codex-plugin/plugin.json) contains the ChatGPT and Codex plugin metadata.
- [`build_plugin.py`](scripts/build_plugin.py) builds and validates the plugin package.

No AI Slop is also available as a plugin in ChatGPT.

## License

MIT
