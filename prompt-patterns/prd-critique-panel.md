# Pattern: PRD Critique Panel

**Job:** Stress-test a PRD (or one-pager, or opportunity brief) before humans spend a meeting on it — so the meeting starts at the interesting disagreements instead of the missing sections.

**When to use:** Any document about to consume more than three people's hour. **When not to use:** As the approval step. The panel finds weaknesses; it does not confer judgement, context, or accountability. A document no human has challenged is unreviewed, whatever the AI said.

## The pattern

Run three passes — separate conversations, not one mega-prompt (roles bleed into each other in a single pass):

```
PASS 1 — THE ENGINEER
Read this PRD as a sceptical senior engineer who will build it. List: every
ambiguity you'd have to guess about; every edge case unaddressed; every place
"just" hides complexity. Rank by how expensive the guess is if wrong.

PASS 2 — THE CUSTOMER
Read this PRD as the customer it describes. In first person: what problem do I
have, does this actually solve it, what does it assume about me that might be
false, and at what moment would I abandon this flow?

PASS 3 — THE EXECUTIVE
Read this PRD as an executive with 4 minutes. What is being promised, what
will it cost, how will we know it worked, and what is conspicuously not said?
If the success metric is missing, vague, or unfalsifiable, say so bluntly.
```

## What good output looks like

- Pass 1 produces the questions engineering would have asked in sprint 2 — moved to day 0
- Pass 2 occasionally reveals the PRD solves the org's problem, not the customer's (the most valuable failure it catches)
- Pass 3's "conspicuously not said" list is usually the real review agenda

## Known failure modes

- **Politeness creep.** Models soften critique over a long conversation. Fresh conversation per pass, always.
- **Checklist theatre.** The panel finds *structural* weakness, not *strategic* wrongness. It cannot know the market moved or that a rival shipped last week. Currency is your job.
- **Author gaming.** Teams learn to write PRDs that pass the panel. Fine — that was the point — but rotate the personas quarterly (add "the support lead", "the regulator", "the finance partner") or the writing optimises for three critics instead of reality.
- **False confidence on numbers.** The executive pass will accept plausible-looking metrics. It checks that a success metric *exists and is falsifiable*, not that the target is sane.

## Field note

The panel's real product is meeting quality. When the mechanical critique arrives with the document, the humans in the room are freed to argue about the only things worth their salary: is this the right problem, and is now the right time.

