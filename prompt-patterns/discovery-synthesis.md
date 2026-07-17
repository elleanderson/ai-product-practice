# Pattern: Discovery Synthesis

**Job:** Turn a pile of raw discovery material — interview notes, support tickets, survey verbatims — into candidate insights a product team can interrogate, without the AI inventing the conclusions for you.

**When to use:** After 5+ interviews or 50+ tickets, when patterns probably exist but reading everything twice isn't happening. **When not to use:** As a substitute for having attended the interviews. Synthesis of material you never engaged with produces confident summaries of things you can't defend.

## The pattern

```
You are assisting a product team with discovery synthesis. You will be given raw
research material. Your job is to surface candidate patterns, NOT conclusions.

Rules:
1. Every pattern you propose must cite at least two distinct sources from the
   material (quote a short fragment + its source label).
2. Separate OBSERVATIONS (what people said/did) from INTERPRETATIONS (what it
   might mean). Label each explicitly.
3. Note counter-evidence: for each pattern, search the material for anything
   that contradicts it and report what you find, including "none found".
4. List what's MISSING: questions this material cannot answer.
5. Do not recommend solutions. That is the team's job, later.

Material follows:
[PASTE MATERIAL]
```

## What good output looks like

- Patterns with citations you can check in seconds
- A visible observation/interpretation boundary (this is the anti-hallucination seam — if it blurs, stop trusting the output)
- A counter-evidence section that occasionally kills a pattern you liked
- A "missing" list that becomes your next round's discussion guide

## Known failure modes

- **Frequency ≠ importance.** The model weights what's mentioned often, not what's felt deeply. One devastating churn story can matter more than nine mild grumbles; only a human who was in the room knows which is which.
- **Coherence bias.** Given messy material, the model will find *a* story. Run it twice with the material shuffled; if the patterns change order dramatically, they're weaker than they read.
- **Vocabulary flattening.** Customers' odd word choices are often the insight. Synthesis normalises language — go back to verbatims before naming anything.
- **The citation shortcut.** Under length pressure the model may cite two sources that don't quite say what the pattern claims. Spot-check one citation per pattern, every time. The day you stop checking is the day it drifts.

## Field note

The counter-evidence rule (#3) earns its place the first time it saves you from presenting a pattern your stakeholder can refute from memory. It also changes team behaviour: people start asking "what's the counter-evidence?" of *human* analysis too — which was the point all along.

