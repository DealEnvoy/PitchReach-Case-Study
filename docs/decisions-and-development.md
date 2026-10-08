# Decisions, iteration and AI-assisted development

[Case study](../README.md) · [Architecture](architecture.md) · [Validation](validation.md)

These are retrospective explanations supported by the inspected implementation and project records. They are not invented quotations or a claim that every technical decision was personally implemented by Isaac.

## Product and engineering trade-offs

| Decision | Product reason | Cost or limitation |
|---|---|---|
| Withhold national scores and heatmaps | Sparse research cannot justify a complete geographical rating | A less expansive beta, with no universal ranking |
| Make unknown and unavailable states explicit | Missing, stale or unsupported evidence must not look like a measured zero | More states to explain and test |
| Compare equivalent measured venue sets | Unequal measurement coverage must not distort a comparison | Some comparisons are refused until sufficient equivalent measurements exist |
| Track provenance at field level | A category classification does not verify a venue, entrance or recruitment rule | More curation and conflict-resolution work |
| Resolve postcodes from a same-origin reference | Ordinary lookup need not send a full postcode to an external geocoder | Snapshots need maintenance; hosting still sees district requests |
| Keep account records separate from scenarios | Adult membership and consent do not require a persistent child-search database | No saved household/player workflow in the inspected design |
| Hold ordinary tester journeys server-side | Provider suitability and release conditions need evaluation before broader use | Testers cannot yet exercise journeys |
| Provide a directory beside the map | Research should remain inspectable when map rendering fails | Accessibility still requires dedicated assessment |

A distance-led directory is already useful if it labels straight-line proximity accurately. A national rating or larger spatial backend is a possible later direction, but neither is required merely to make the portfolio appear more sophisticated.

## Iteration: a zero score that exceeded the evidence

### The problem

An earlier assessment returned a practical-access score of `0/100` when none of a small researched venue sample fell inside a chosen travel budget. The sample count could be correct while the implied overall conclusion was unsupported.

That differs from a second case in which all route measurements fail or are excluded: then even the reachable sample count cannot be known.

### The behavioural correction

The corrected contract retains a zero sample count only when usable measurements show that no researched venue meets the budget. It withholds the broader practical score and explains that no sample falls within budget. When there are no usable routes, the relevant counts are unavailable instead. National opportunity remains withheld.

| Same controlled scenario | Earlier behaviour | Corrected behaviour |
|---|---|---|
| Seven researched venues; each 180 minutes away; a 60-minute budget | Practical score shown as zero | Practical score withheld; explicit no-sample-within-budget state |
| Reachable venues in the measured sample | Zero | Zero, retained as a scoped sample observation |
| Meaning supported by the evidence | Presentation could suggest no overall opportunity | Limited sample result, without a national conclusion |

### How the change was checked

On 7 October 2026, an assistant ran a deterministic offline fixture against the historical pre-correction source, the first retained correction and the audited baseline. The clock and scenario were controlled and no real journey provider was called. The earlier source failed the intended assertion; both corrected versions passed.

An existing regression also renders the actual assessment card and checks that the misleading zero-score presentation is absent. This is domain/component evidence, not a fresh end-to-end browser test. The historical screenshots in this repository show the surrounding interface, **not** this synthetic failing/passing scenario.

Other retained regressions cover unsupported pathways, stale inputs, null route durations, equivalent comparison denominators and reduced-report behaviour. No conversion gain, accuracy percentage or football outcome is inferred from these fixes.

## Human contribution and AI-assisted workflow

Isaac originated the parent-facing problem, defined the audience and comparison brief, selected the brand and domains, and directed AI-assisted product development. His evidenced contribution is product ownership: framing the problem, specifying intended behaviour, authorising development and keeping the release aligned with the available evidence.

| Contribution | Attribution and limits |
|---|---|
| Problem, audience and product direction | Isaac Adekunle |
| Brand and domain choices | Isaac Adekunle |
| Retained implementation history | Commits recorded under Codex; this does not prove personal handwritten implementation by Isaac |
| Specification, implementation and review roles | Separate artifacts are retained; not proof that every release received a different model's or human's independent review |
| 7 October audit, test reruns and case-study documentation | Assistant-executed under Isaac's instructions |

The reconstructable process is to translate the user problem into explicit scope and states, develop against those constraints, turn review findings into testable behaviours, reproduce defects against historical source, and document release evidence and remaining gaps.

**AI-assisted building is distinct from AI inside the product.** The inspected runtime uses curated research and deterministic rules. No runtime LLM inference, model training or autonomous academy verification is claimed.

A future research-extraction assistant would require source-linked evaluation, conflict handling and human review. It remains a possible development direction, not an implemented feature. The strongest next contribution evidence would be a recorded walkthrough in which Isaac explains the architecture, reproduces a meaningful scenario and documents a change he personally reviews or implements.
