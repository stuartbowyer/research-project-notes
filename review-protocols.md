# A Short Guide to Review Protocols

A protocol is a pre-commitment: it states what you will do before you do it, so your results cannot quietly reshape your methods. It is also a contract you will be marked against, because everything you promise will be checked against what you deliver. I have written this mainly for review protocols (scoping and systematic reviews), but the principles, which are to justify choices, be explicit, and commit only to what you can deliver, apply to any study protocol.

## Frame the question properly

- **Use the right framework.** For scoping reviews use PCC (Population, Concept, Context), the JBI-recommended structure. It avoids the awkward not-applicable comparator that PICO forces on non-comparative questions. Keep PICO for effectiveness questions.
- **Phrase the question so the literature can answer it.** A review sees what studies report, not what is true. Build that into the wording: "to what extent do X demonstrate Y, based on reported indicators in the current literature?"
- **Justify the review type.** "Scoping" is a design choice, not a hedge. Say what it is about the field (heterogeneity of methods, immaturity, breadth) that makes a scoping review the right tool rather than a full systematic review.

*Further reading: [JBI Manual for Evidence Synthesis](https://synthesismanual.jbi.global/), [PRISMA-ScR](https://www.equator-network.org/reporting-guidelines/prisma-scr/), and [PRISMA-P](https://www.equator-network.org/reporting-guidelines/prisma-protocols/) for the protocol itself.*

## Search strategy

- **Keep terms consistent across databases.** Adapt the syntax per interface, never the substance. And avoid near-duplicates: PubMed and MEDLINE are almost identical, so pick one and say why.
- **Include preprint servers deliberately.** If arXiv or medRxiv is in scope, it appears in the source list, the interface list and the search, not just one of them.
- **Prefer sensitivity over convenience.** A clause that shrinks the results to a comfortable number usually costs you relevant work, because fields name themselves inconsistently. Test the string with and without the clause; if the larger return is screenable, screen it.
- **Check for MeSH (and equivalent index) terms** alongside free-text terms.
- **Validate the search, and say how.** Known key papers must be returned. Describe the validation plainly (a test screening round, a set of known papers checked) rather than by niche terminology, and if you ran an initial screen to refine the terms, report it.

## Eligibility criteria

- **Explicit, and mirroring your PCC or PICO.** Exclusion criteria are not just negations of the inclusions; if one is, cut it.
- **Decide the ambiguous cases in advance.** A study spanning an included and an excluded setting, or a method demonstrated in your domain and another: where do they go?
- **Language limits are a limitation, not a quality filter.** Restricting to English is defensible pragmatism; claiming it improves quality is contentious. State it as a limitation.
- **Justify the time window** rather than asserting it.

## Extraction and synthesis

- **List every extraction field explicitly**, as a table with the name, its definition, and why it is collected. "Study characteristics will be extracted" is not a plan, and a vague field ("regulatory considerations") extracts vaguely.
- **Be honest about the reviewer model.** One person extracting and a second checking is achievable, and worth stating plainly. Blinded, fully independent dual extraction is a large promise; make it only if you can resource it. If you claim dual screening, plan to report agreement (Cohen's κ or similar).
- **Plan symmetric treatment for parallel constructs.** If you will assess two dimensions, pre-specify the same summary, stratifications and tests for both, or state why the asymmetry is deliberate.

## Scope realism

The most common failure I see in protocols is promising too much.

- **Every commitment costs.** Contacting authors for missing data is slow and low-yield; analysing every conceivable aspect takes time you do not have; anything that depends on other people responding is not under your control. Often the strongest choice is a plain "we will not contact authors".
- **Cut at protocol stage, not at write-up.** An honest, smaller commitment reads better than a broken large one, and the marker only ever sees the broken one.
- **Put slack in the timeline.** Screening always takes longer than planned, and anything headed for publication needs months for review and revisions.

## Registration and deviations

- **Pre-register.** [OSF](https://osf.io/registries) for scoping reviews; [PROSPERO](https://www.crd.york.ac.uk/prospero/) for systematic reviews of health outcomes.
- **Include an amendments statement:** "Any deviations from this protocol will be documented and justified in the final manuscript." Then actually document them.
- **Deviations honestly reported are normal science.** Silent drift between what was registered and what was done is what reviewers and markers punish.
