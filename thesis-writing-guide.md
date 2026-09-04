# A Short Guide to Writing a Research Thesis

This is the guidance I find myself giving most often when supervising research theses in clinical data science and AI. Most of it applies to any thesis that reports a study. It is ordered as the thesis reads, not as you will write it. The abstract comes first here but is written last.

A note on marking before anything else. Schemes differ between programmes, but their shape is consistent: methods, results and discussion carry most of the marks; the introduction is assessed on the clarity of your aims and the quality of your appraisal of the literature, not its length; the abstract is usually the highest marks per word in the document; and presentation and referencing are the cheapest marks to lose. Read your own programme's marking criteria before you write a word. They are the specification you are writing to.

---

## Chapter by chapter

### Abstract

- **Usually the highest marks per word in the thesis.** Give it real time, not the final hour.
- **Write it for an intelligent reader who has never met the project.** No internal shorthand, no undefined terms. The test is whether an outside clinician could follow every sentence on first read.
- **The shape:** the problem and who it affects, your approach, the main findings with numbers (and confidence intervals where relevant), and the significance. That is IMRaD order (introduction, methods, results and discussion); check whether your handbook wants it as a structured abstract with headings. Read some published abstracts in your area to calibrate the pitch.
- **Balance the four parts.** Background, approach, findings and significance each want roughly a quarter of the words. An abstract that spends half its length arriving at the aim has no room left to say what happened.

### Aims, objectives and research questions

The most common structural weakness, and the cheapest to fix early.

- **One aim, one sentence, standing alone.** Set it out as its own short paragraph in the introduction ("The aim of this research was to ...") so no reader can miss it. High level is fine, and naming the project's components in one sentence is fine.
- **Objectives are falsifiable tests, not a to-do list.** Each needs a verb with a measurable endpoint: "quantify", "measure", "test whether" and "validate" all pass; "investigate" and "explore" are un-falsifiable and will be criticised; "compare" only passes when you name the outcome and the direction you expect.
- **In qualitative work the test is answerable, not falsifiable.** In an interview or observational study, "explore" and "describe" are legitimate verbs when the objective names the population, the data and how you will analyse it. A comparison is fine when the design is explicitly comparative.
- **Apply the "no" test to every research question.** What result would have forced you to answer no? If nothing could, it is not a research question. Rewrite it until something could.
- **Frame questions at the level of the method, not the artefacts of your experiment.** A question tied to one arbitrary parameter choice is too narrow; a question that any outcome "answers" is too broad.
- **Commit only to what you can deliver.** An honest, smaller set of objectives reads better than an ambitious set you cannot finish.
- **The set must round-trip.** Each objective maps to a chapter or analysis, and the conclusion closes every one explicitly. An objective that never gets explored or answered is a marker's easiest criticism.

*Further reading: [Farrugia et al., Research questions, hypotheses and objectives, Can J Surg 2010](https://www.canjsurg.ca/content/53/4/278), including the FINER criteria (Feasible, Interesting, Novel, Ethical, Relevant).*

### Write the problem forward, not the methods backwards

A thesis assembled by describing each component of the pipeline in turn reads as a summary of itself rather than an argument for the work.

- **Say who this is for.** Which patient, clinician or service carries the problem, and what changes for them if the work succeeds? If nobody appears in your introduction at all, rebuild it from the problem.
- **The standard shape of an introduction:** general background and the high-level issue, then the specific problem you address, then aims and objectives, then a brief overview of your approach and the thesis structure.
- **Novelty alone is not a gap.** Plenty of unexplored ground is unexplored for good reason. Make the case on difficulty or consequence: what makes this hard, and what becomes possible once it is solved?

*Further reading: [Mensh & Kording, Ten simple rules for structuring papers, PLOS Comput Biol 2017](https://journals.plos.org/ploscompbiol/article?id=10.1371%2Fjournal.pcbi.1005619).*

### Appraise the literature, don't inventory it

- **Criticise, don't just report.** If every cited paper is summarised and none is appraised, the chapter reports the literature rather than analysing it. For each section, say what the cited work does not do, cannot show, or gets wrong.
- **Be precise about sources.** Quote specific findings, with numbers, and characterise the source correctly.
- **Size the field.** A quantified context (how much work exists, and how little of it addresses your niche) turns your gap from an assertion into evidence.
- **Reference every assertion.** Any sentence stating a fact about the world needs a citation, and prefer recent sources for fast-moving claims.

### Methods: justify every choice

The habit that costs the most marks is describing choices without defending them.

- **Every decision gets a reason or a reference.** Cohort definitions, inclusion codes, thresholds, hyperparameters, imputation, statistical tests, metrics, model choices. Go through the chapter, mark every decision you made, and attach a justification to each. "We did X" is never complete; "we did X because Y" is. Length tracks consequence: a conventional choice needs a citation rather than an argument, and a choice that would change the answer needs a paragraph. If a choice was genuinely arbitrary, say so and show it does not change the result.
- **Justify metrics against use.** Say why your chosen metrics give the information that matters for the intended use: which errors matter, to whom, and what performance would make the result genuinely useful.
- **Make it replicable.** Software and package versions, parameter search ranges, full search strings, data processing steps. Detail needed only to reproduce the work, rather than to understand it, goes to an appendix with a pointer sentence.
- **Understand and test any AI-generated analysis code.** The method it implements is your method now, and you will be questioned on it. "The tool wrote it" is not an answer an examiner accepts.
- **Write the governance sections plainly and truthfully.** Ethics and approvals, data access and credentialing, consent handling. If no formal process applied, say so. That is an acceptable answer; an invented one is not.
- **Use the reporting guideline for your study type, and say which you used:** [TRIPOD+AI](https://pubmed.ncbi.nlm.nih.gov/38626948/) for prediction models, or [TRIPOD-LLM](https://pubmed.ncbi.nlm.nih.gov/39779929/) if the model is generative; [PRISMA 2020](https://www.prisma-statement.org/prisma-2020-statement) for systematic reviews or [PRISMA-ScR](https://www.equator-network.org/reporting-guidelines/prisma-scr/) for scoping reviews; [STROBE](https://www.equator-network.org/reporting-guidelines/strobe/) for observational studies, extended by [RECORD](https://www.equator-network.org/reporting-guidelines/record/) when the data are routinely collected. The [EQUATOR Network](https://www.equator-network.org/) indexes the rest. If you pre-registered a protocol, state and justify every deviation.
- **No results in the methods.** Cohort counts, tuned parameter values and response rates are findings, and belong in results.

### Results: tables carry the numbers, text carries the argument

- **Open paragraphs with the finding, not the procedure.** "Delayed antibiotic administration was associated with higher 30-day mortality (OR = ..., p = ...)", not "a logistic regression was fitted, which showed ...". The test goes after the claim, often in parentheses.
- **Two or three numbers per claim; the rest live in the table.** A number belongs in prose only if the argument falls apart without it. If the reader has to reconcile text against table to follow you, restructure.
- **Denominators everywhere.** N and events for every analysis, at every horizon or subgroup. No reader should have to take an eligible population on trust.
- **Name your primary measure in the methods and use it consistently.** The reader should never wonder whether the denominator was chosen after the result.
- **Parallel analyses get parallel structure.** If you analyse two constructs, where possible give them symmetric subsections with the same treatment, or say why the asymmetry is deliberate.
- **Interpretation waits for the discussion.** A sentence explaining why a result occurred has leaked out of place.

*Further reading: [Gopen & Swan, The Science of Scientific Writing, American Scientist 1990, 78(6):550–558](https://www.usenix.org/sites/default/files/gopen_and_swan_science_of_scientific_writing.pdf), on how readers actually extract meaning from sentence structure.*

### Discussion: what the results mean, not what they say again

This is where depth of thinking is assessed, and it is usually the difference between a solid mark and a good one.

- **Structure it around your research questions.** One section per question: your answer first, then the evidence, then its edges. A section-by-section commentary on the results chapter is not a discussion.
- **Never open a paragraph by restating a table in prose.** A sentence that only repeats a result is doing nothing. Delete it.
- **Anchor your findings outside your own work.** Is your effect large or small for this kind of intervention? Is a null expected or surprising? A discussion that never checks whether its findings are surprising is incomplete.
- **State the strongest claim your evidence supports, plainly, and defend it.** Conceding every limitation while never saying what the thesis has shown reads as anxiety rather than rigour, and is a common pattern of AI writing.
- **Confront your hardest question.** Find the most awkward tension in your own results (two analyses that disagree, a bias you detected) and answer it on paper before an examiner asks it in person.
- **Strengths deserve their own passage.** Design decisions that protect the conclusions (held-out validation, pre-registered endpoints, honest negative results) are contributions. Claim them.
- **Limitations: each said once, honestly, with the direction that would resolve it.** Repeating a caveat three times weakens it rather than covering you.
- **Future work must be yours.** "Prospective multi-centre validation" fits almost every clinical ML project ever written. Name the specific next experiments your findings point to.

*Further reading: [Docherty & Smith, The case for structuring the discussion of scientific papers, BMJ 1999](https://pmc.ncbi.nlm.nih.gov/articles/PMC1115625/).*

### Conclusion

- **Close every aim and objective explicitly.** Anything promised in chapter one and absent here is a red flag.
- **No new material.** Synthesis only.
- **End on why the work matters, with as big a picture as plausible.** The same answer you opened with, now earned. What does the person you wrote the introduction for have, if this line of work succeeds, that they do not have today?

## Across the whole thesis

These apply throughout the thesis rather than to any one chapter. Read the next two sections before you write your discussion, not after it.

### Before you believe your own number

The rest of this guide is about writing a result up well. This section is about whether the result is real. These problems sit in the numbers rather than the sentences, so they survive a careful proofread.

- **Know what your denominator contains.** A proportion is a risk only if everything underneath it had a genuine chance of being an event. Runs that stopped early, records that failed a join, participants who dropped out: counted as non-events, they deflate the estimate, usually most in the cases you care about. Say how many hit any limit, and which way that pushes.
- **Check whether your test data ever touched training.** Cases from the training split, a reference cohort from the same partition, a feature computed after the outcome, a scaler fitted before the split. If the model could have memorised the answer, nothing downstream means what it appears to. Say so where the number is, not only in the limitations.
- **Ask whether your measure could have come out any other way.** A self-reported improvement rating collected straight after the intervention, a fixed presentation order, an outcome scored by whoever designed the thing being scored. These return a positive result whatever the intervention does. If you cannot picture the version that would have given a null, call the finding perceived rather than measured.
- **Show the headline survives your arbitrary choices.** A threshold, a window length, a replacement strategy: rerun the main result once under an alternative for each and report it in a sentence. It is cheap, it answers the obvious viva question, and now and again it saves you from an artefact.
- **Give every bias a direction.** "There may be selection bias" tells a reader nothing. Which way would it move the estimate, and does your claim still stand once it has? A bias you have signed is a limitation. One you have only named is an invitation.
- **One comparison is one comparison.** A single benchmark case, one seed, ten groups, one site: these support "in this case" and nothing wider. Sample size limits a methodological claim exactly as it limits a clinical one, and that holds for negative findings too.

*Further reading: [Kapoor & Narayanan, Leakage and the reproducibility crisis in machine-learning-based science, Patterns 2023](https://www.cell.com/patterns/fulltext/S2666-3899(23)00159-9).*

### Claims and precision

Calibrate every claim to the evidence behind it. The findings are no less interesting when stated carefully; they are just defensible.

- **Match verbs to evidence.** "The small evidence base suggests" and "where studied, patients tended to", not "the evidence shows" or "patients universally", when the base is a handful of heterogeneous studies.
- **Decimal places imply precision.** Report only what your sample size can substantiate. A percentage to one decimal place from 15 observations is a claim you cannot back.
- **Say what you measured, not the construct you wish you had measured.** If your labels came from diagnostic codes, the model predicts coding rather than disease. Name the outcome for what it is, and say what further validation a claim about the disease itself would need.
- **In non-randomised comparisons, name the alternative explanation.** An unadjusted difference between groups that differ at baseline is not an effect. Say so before the examiner does.
- **Hold one position across results, discussion and conclusion.** "Lower", "not significantly different" and "comparable" are three different claims. Pick the one your evidence supports and use it everywhere.

*Further reading: [Ken Hyland, Hedging in Scientific Research Articles, John Benjamins 1998](https://benjamins.com/catalog/pbns.54), and [Haber et al., Causal language and strength of inference (CLAIMS), PLOS ONE 2018](https://journals.plos.org/plosone/article?id=10.1371%2Fjournal.pone.0196346) on whether causal language matches the design.*

### When the main thing didn't work

Plenty of good theses report a result nobody wanted. The mark follows the quality of the reasoning, not the direction of the result.

- **Report the negative result properly.** State it as a finding, with its numbers and its uncertainty, in the form you would have used had it gone the other way. A finding moved to a late subsection reads as embarrassment and invites the examiner to look harder.
- **Show that it is a result and not a bug.** The diagnostic work is the contribution here: the sanity checks, the ablations, the deliberately easy case your pipeline does solve. Without them a null cannot be told apart from a mistake.
- **Reframe what the contribution is.** Often it is the method, the dataset or the failure analysis rather than the headline finding. Name it in the abstract and the conclusion so the reader is not left hunting for it.
- **Don't try to rescue it with a subgroup.** A result that appears only after slicing the data is a hypothesis for someone else's study. Say that, and say what testing it would take.
- **Say what you would do differently, and why.** You will be asked this in the viva, and a specific answer is the strongest one available to you.

### Figures and tables

- **Text in figures at an effective size of 11–12 pt** at final scale, consistent across figures and with the body text.
- **Export figures as vector files, not screenshots.** Save straight from the plotting library as PDF or SVG so the figure stays sharp at any size. A screenshot of a plot window is low resolution, and it shows at print size.
- **Units on axes, and tick precision that matches the data** (no decimal places on an integer count). Label panels (a), (b) and so on.
- **Captions live in the document, not baked into the image**, and should let the figure stand alone: explain every encoding, including what the numbers, colours and groupings mean.
- **Reference every figure and table from the text** that introduces it, placed at a natural break on or after that page.
- **One colour palette across the whole thesis.** Choose it once, and keep the same colour for the same group or condition in every figure. Check it stays readable in greyscale and for colourblind readers.
- **Design choices carry meaning.** Don't switch chart types or colour schemes between comparable plots without a reason, and flag artefacts (a partial final year in a time series, say) rather than letting the figure mislead.
- **Look at the finished figure, not just the settings that produced it.** Open it at print size and read it as a stranger would. Two series carrying the same label, a value label clipped by the axis, a panel cropped mid-content, comparable panels drawn on different scales so that a small effect and a large one are the same length: none of these are visible in the plotting code, and all of them are obvious on the page.

*Further reading: [Rougier, Droettboom & Bourne, Ten Simple Rules for Better Figures, PLOS Comput Biol 2014](https://journals.plos.org/ploscompbiol/article?id=10.1371%2Fjournal.pcbi.1003833).*

### References

- **Use a reference manager (Zotero or EndNote) from the first draft.** Retrofitting citations is slower and produces errors.
- **Numeric style (Vancouver or IEEE)** unless your handbook says otherwise. It also saves words against the limit.
- **Do a full reference check before submission:** every in-text citation present in the list, consistent ordering, no orphans. Markers do check.

### The final pass

Before sending any draft, to your supervisor or for submission, read it end to end yourself, in one sitting, and check:

- **Terminology.** One name per concept, used everywhere; abbreviations defined once, at first use (and in the abbreviations list if you keep one).
- **Repetition.** Anything said twice gets said once, in the right place.
- **Mechanics.** Tenses consistent; word count within limit (check exactly what your handbook counts); page breaks rather than blank lines; no duplicated or missing captions.
- **Appendices are genuinely supplementary:** material a reader might refer to, not overflow moved to dodge the word limit.
- **Plain language over ornament.** When you have reached for a Capitalised Named Framework or a stack of abstract nouns, ask whether a sentence with ordinary verbs says it better. If yes, use that. The contribution gets clearer, not less impressive. If a term is standard, cite it; if it is genuinely yours, say so and define it.

### Using AI

Your programme's policy on generative AI is binding, and it, not this guide, governs what you are permitted to use. What follows applies whatever it allows.

- **Never paste confidential data into a consumer AI tool.** That includes patient data, anything held under a data use agreement or credentialed access, and a collaborator's unpublished work. Check what your institution provides and what your data agreement permits before you upload any part of a draft.
- **You own every sentence.** You must be able to explain and defend every sentence of the thesis, in person, without notes. If you cannot explain a sentence out loud, it should not go in, however good it sounds. AI-assisted errors are still your errors.
- **Verify everything it gives you.** Check claims against sources, numbers against your own outputs, and citations against the actual papers. A citation you have not opened is a citation you cannot defend, and submitting one is an integrity problem, not a formatting one.
- **Ask it to find problems, not to write.** The tools are strong on spelling, grammar and punctuation, and there is little excuse now for sending a draft with errors a machine catches in seconds. Ask where the problems are and fix them yourself; a rewrite hands you sentences you may not be able to defend.
- **Declare it accurately.** Your acknowledgements must state what you personally did and what others, people or tools, did for you, and the statement must match the actual workflow. For publication the bar is external: tools cannot be authors, and their use must be disclosed in the methods rather than the acknowledgements. Check the target journal's own policy: most follow COPE or ICMJE, and ICMJE also asks for it in the cover letter.

*Further reading: [COPE: Authorship and AI tools](https://publicationethics.org/guidance/cope-position/authorship-and-ai-tools).*

---

## Further reading

- [Farrugia et al., Research questions, hypotheses and objectives (Can J Surg, 2010)](https://www.canjsurg.ca/content/53/4/278)
- [Mensh & Kording, Ten simple rules for structuring papers (PLOS Comput Biol, 2017)](https://journals.plos.org/ploscompbiol/article?id=10.1371%2Fjournal.pcbi.1005619)
- [Gopen & Swan, The Science of Scientific Writing (American Scientist, 1990, 78(6):550–558)](https://www.usenix.org/sites/default/files/gopen_and_swan_science_of_scientific_writing.pdf)
- [Docherty & Smith, The case for structuring the discussion of scientific papers (BMJ, 1999)](https://pmc.ncbi.nlm.nih.gov/articles/PMC1115625/)
- [Rougier, Droettboom & Bourne, Ten Simple Rules for Better Figures (PLOS Comput Biol, 2014)](https://journals.plos.org/ploscompbiol/article?id=10.1371%2Fjournal.pcbi.1003833)
- [Kapoor & Narayanan, Leakage and the reproducibility crisis in machine-learning-based science (Patterns, 2023)](https://www.cell.com/patterns/fulltext/S2666-3899(23)00159-9)
- [Ken Hyland, Hedging in Scientific Research Articles (John Benjamins, 1998)](https://benjamins.com/catalog/pbns.54)
- [Haber et al., Causal language and strength of inference in academic and media articles, CLAIMS (PLOS ONE, 2018)](https://journals.plos.org/plosone/article?id=10.1371%2Fjournal.pone.0196346)
- [EQUATOR Network reporting guidelines index](https://www.equator-network.org/), including [TRIPOD+AI](https://pubmed.ncbi.nlm.nih.gov/38626948/), [TRIPOD-LLM](https://pubmed.ncbi.nlm.nih.gov/39779929/), [PRISMA 2020](https://www.prisma-statement.org/prisma-2020-statement), [PRISMA-ScR](https://www.equator-network.org/reporting-guidelines/prisma-scr/), [STROBE](https://www.equator-network.org/reporting-guidelines/strobe/) and [RECORD](https://www.equator-network.org/reporting-guidelines/record/)
- [Mullins & Kiley, "It's a PhD, not a Nobel Prize": how experienced examiners assess research theses (Studies in Higher Education, 2002)](https://www.tandfonline.com/doi/abs/10.1080/0307507022000011507)
- [Golding, Sharmini & Lazarovitch, What examiners do: what thesis students should know (Assessment & Evaluation in Higher Education, 2014)](https://www.tandfonline.com/doi/full/10.1080/02602938.2013.859230)
- [COPE: Authorship and AI tools](https://publicationethics.org/guidance/cope-position/authorship-and-ai-tools)
