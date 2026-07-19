# Discovery synthesis

A prompt pattern for synthesising a round of customer interview debriefs. Companion to [The Discovery Interview Kit](https://andersonco.uk/discovery-kit.html); it assumes your debriefs follow the kit's shape (said, did, surprised, contradicted).

The point of using a model here is speed across volume, not judgement. The pattern is built to keep the judgement with you.

## The prompt skeleton

Paste your debriefs (all of them, verbatim, including the awkward ones), then:

> You are assisting with customer discovery synthesis. Using ONLY the debrief notes provided, produce:
>
> 1. OBSERVATIONS: things stated or demonstrated in the notes, each with the interview references that support it. Quote only text that appears verbatim in the notes. Minimum two sources per observation; single-source items go in a separate list called ANECDOTES.
> 2. CONTRADICTIONS: places where interviews disagree with each other, or where what someone did contradicts what they said.
> 3. COUNTER-EVIDENCE: anything in the notes that undermines the following hypothesis: [state your hypothesis]. If none exists, say "none found in the notes".
> 4. GAPS: what these notes cannot tell us, and which questions in the next round would close each gap.
>
> Do not produce recommendations, solutions, or interpretations of motive. Do not use any knowledge beyond the notes. Where the notes are thin, say so rather than smoothing over it.

Then, and only in a second pass after you have read the first output against the source notes:

> Given the observations and contradictions above, list candidate INTERPRETATIONS, each labelled with which observations support it and what evidence would falsify it.

## Why the rules are shaped this way

- **Two sources per observation** enforces the same rule a human synthesiser should follow: one vivid interview is an anecdote wearing a trench coat.
- **Verbatim quotes only** is the check against invented customers. Spot-check every quote against the notes; a model that has started paraphrasing has started authoring.
- **Counter-evidence as an explicit section** counters the model's instinct to be agreeable about your hypothesis. Asking for it by name roughly doubles the chance of getting it.
- **Interpretations in a second pass** keeps observation and interpretation from blending, which is the failure that quietly poisons roadmaps.

## Documented failure modes

- **Confabulated quotes.** The most dangerous, because they sound exactly like your customers. Spot-check quotes against source before anything travels.
- **Frequency worship.** Models count well and weigh badly: nine mild grumbles will outrank one devastating churn story unless a human re-weights. Weighting stays with whoever was in the room.
- **Smoothing.** Contradictions get averaged into mush. If the CONTRADICTIONS section comes back empty across eight interviews, be suspicious of the synthesis, not proud of the consistency.
- **Hypothesis sycophancy.** Even with the counter-evidence instruction, phrasing your hypothesis warmly biases the read. State it coldly, or have a colleague state the rival hypothesis and run the pattern twice.
- **Scope creep into recommendation.** The model will offer solutions if allowed a millimetre. The decisions section of your synthesis belongs to the team, on the record, in the kit's closing format.

## The rule that governs the pattern

The model reads the pile; you keep the judgement. If a finding would change a roadmap decision, someone re-reads the underlying debriefs before it does.

---

Free to use and share, with attribution. Part of [AI Product Practice](../README.md) by [Elle Fitz Anderson](https://andersonco.uk).
