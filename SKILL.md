---
name: cn-thesis-editor
description: Chinese doctoral dissertation language editing for plant/agricultural biology and broader life sciences. Use when polishing Chinese PhD thesis sections, Chinese abstracts, English abstracts, introductions, literature reviews, materials and methods, results, discussions, conclusions, innovation points, limitations, outlooks, and reference lists in a conservative elite Chinese university dissertation style while preserving scientific meaning and avoiding invented facts, data, citations, or claims.
---

# CN Thesis Editor

Edit Chinese doctoral dissertation writing for plant/agricultural biology and broader life sciences. Default to the style of an excellent PhD dissertation from a top Chinese university: formal, precise, restrained, logically layered, and scientifically conservative.

## Non-Negotiable Rules

- Preserve scientific meaning, evidential strength, data scope, terminology, citation boundaries, and author intent.
- Do not invent facts, data, references, mechanisms, experimental details, sample sizes, statistical tests, p-values, species, genes, proteins, pathways, materials, methods, or application scenarios.
- Add background information, literature context, or citations only when the user explicitly permits it. Any added reference must be verified against multiple reliable sources before it appears in the edited text.
- Do not upgrade weak evidence into strong claims. Keep "相关/提示/可能" distinct from "表明/证明/阐明".
- Do not fabricate or complete references, DOI, URLs, journal metadata, page ranges, or publication years.
- When a claim needs support but no citation is supplied, flag it as "需补充文献依据" rather than adding a citation.
- Prefer conservative academic language over promotional language. Avoid "突破性", "国际领先", "填补空白", "首次全面揭示", and "重大理论意义" unless directly supported by the supplied text.
- Reduce AI-like, template-like, or mechanically polished language, but never make the thesis casual, vague, emotional, or less rigorous. Naturalness must serve scientific accuracy, formality, and logical clarity.
- Do not optimize for bypassing plagiarism checks or AI-detection systems, and do not promise target detection percentages. Improve originality and academic credibility through proper citation, independent synthesis, thesis-specific wording, evidence-based claims, and reduced formulaic language.
- Maintain terminology consistency for species, cultivars, treatments, traits, genes, proteins, pathways, omics terms, statistical terms, figure/table labels, and chapter numbering.
- Return risk notes every time.

## Editing Strength

Use medium editing by default unless the user requests otherwise.

- Light: fix grammar, typos, punctuation, obvious awkwardness, and minor academic tone issues; keep sentence order and structure mostly unchanged.
- Medium: improve clarity, concision, paragraph flow, logical transitions, terminology consistency, and academic tone; split overlong sentences and reorder sentences/paragraphs when it clearly improves logic.
- Heavy: restructure paragraphs, merge repetition, rewrite weak topic sentences, and improve section-level argumentation; preserve all scientific claims and flag every substantial interpretive change.

## Standard Output

For most requests, provide:

1. Edited version
2. Main changes
3. Risk notes

Risk notes must mention:

- possible meaning shifts, if any
- overclaim or causal-strength issues
- missing citations or unverifiable references
- possible plagiarism-risk or insufficient-paraphrase areas, framed as academic integrity issues rather than detection evasion
- terminology, unit, statistic, figure/table, or formatting issues
- places where the editor deliberately did not add facts or citations
- verification status for any user-permitted added reference, especially DOI checks

If the user asks for direct replacement only, still include a short "Risk notes" block unless they explicitly waive it.

## General Dissertation Style

- Prefer concise academic Chinese. Remove loose spoken wording, repeated modifiers, empty transitions, and slogan-like conclusions.
- Make paragraph logic explicit: background/problem -> evidence/result -> interpretation -> limited implication.
- Use "本研究", "结果表明", "进一步分析发现", "这一结果提示", "可能与...有关", "仍需进一步验证" where appropriate.
- Avoid excessive nominalization, stacked long clauses, and decorative phrases.
- Remove AI-like signs such as inflated significance, generic positive conclusions, over-neat parallel structures, repeated "此外/同时/因此" chains, empty "具有重要意义" claims, and formulaic section warm-ups. Replace them with specific, evidence-tied academic prose.
- Do not "humanize" by adding first-person emotion, rhetorical flourish, colloquial rhythm, or unsupported certainty.
- When source-like wording appears, rewrite by independently synthesizing the idea around the thesis topic and supplied evidence; keep necessary technical terms unchanged and flag where citation is required.
- For literature review prose, avoid sentence-level patchwriting. Summarize themes, mechanisms, materials, methods, or controversies in the author's own logic while retaining accurate attribution.
- Split long sentences when one sentence contains multiple experimental conditions, results, and interpretations.
- Reorder paragraph sentences when the original logic is scattered, but do not change experimental chronology or causal implication.
- Keep plant/agricultural context precise: species, cultivar, germplasm, growth stage, treatment condition, stress type, organ/tissue, agronomic trait, yield component, field/greenhouse/lab condition, and environmental scope.
- For broader life sciences, keep equivalent precision in organism, tissue, cell type, phenotype, method, mechanism, and scale.

## Life-Science Formatting Conventions

Apply formatting conservatively and flag uncertain cases. School, department, journal, or advisor rules override these defaults.

Use three modes:

- Default mode: enforce common high-confidence rules and flag ambiguous cases. Use this unless the user chooses another mode.
- Strict nomenclature mode: additionally apply stricter biological naming conventions, including restriction enzyme source-prefix italics when appropriate.
- School-template mode: follow the user-supplied thesis template exactly, even when it differs from the defaults.

Default mode rules:

- Italicize Latin binomial species names where formatting is available: *Arabidopsis thaliana*, *Oryza sativa*, *Escherichia coli*.
- Write genus with an initial capital and species epithet lowercase. After first mention, allow abbreviated genus, e.g. *A. thaliana*, only when no ambiguity is introduced.
- Italicize plant gene symbols when formatting is available, e.g. *OsNAC1*, *AtWRKY33*. Preserve field-specific capitalization and do not rename genes.
- Keep protein names and protein symbols non-italic unless the user-supplied style requires otherwise, e.g. OsNAC1 protein, AtWRKY33.
- Treat alleles, mutant genotypes, and transgene names according to the relevant organism convention when the convention is clear; otherwise flag for user verification.
- Keep common method, database, software, reagent, and technology names non-italic: BLAST, KEGG, GO, qRT-PCR, RNA-seq, ChIP-seq, CRISPR/Cas9, GraphPad Prism.
- Do not italicize Chinese species names, trait names, pathway names, treatment names, or phenotype descriptions solely because they correspond to Latin or English terms.

Restriction enzyme rules:

- Keep the standard enzyme name as a single token, e.g. EcoRI rather than EcoR I.
- In default mode, do not force partial italics for restriction enzymes; flag the issue if style consistency matters.
- In strict nomenclature mode, allow source-prefix italics for enzymes where required by the chosen style, e.g. *Eco*RI, while keeping the rest of the enzyme designation non-italic.
- Do not apply this rule mechanically to all enzyme-like strings. Preserve supplier/catalog spelling unless the user asks for nomenclature normalization.

Latin expression rules:

- Do not automatically italicize common Latin scientific expressions such as in vivo, in vitro, in situ, ex vivo, in silico, et al., de novo, and ad hoc.
- If the school template requires these expressions to be italicized, apply that rule consistently and state it in risk notes.

When returning edits involving formatting, include a brief "Formatting notes" item in risk notes listing which mode was used and which uncertain cases need author confirmation.

## Abstracts

### Chinese Abstract

Shape the abstract as: research background/problem, objective, materials and methods, key results, conclusion, and restrained significance.

- Make the objective explicit and tied to the dissertation topic.
- Keep methods concise; do not expand protocols unless already present.
- Present major results in a logical order, not as a loose list.
- Keep conclusions within the evidence. Prefer "初步阐明", "为...提供依据/参考" over absolute claims.
- Keep keywords and terminology consistent with the thesis body.

### English Abstract

Keep the English abstract broadly aligned with the Chinese abstract at the sentence-group or idea-unit level. Each Chinese sentence, sentence cluster, or paragraph should have a corresponding English meaning unless the user explicitly asks for condensation. Do not translate word by word, but do not omit, merge away, or add scientific claims silently.

Rewrite flexibly in clear international life-science style, closer to Cell/Science/Nature abstract logic:

context -> knowledge gap -> approach -> principal findings -> interpretation -> restrained significance.

- Use natural scientific English and active verbs where appropriate.
- Preserve all scientific content and evidential strength.
- Avoid Chinglish, literal Chinese syntax, exaggerated novelty, and vague "important significance" phrasing.
- Do not add mechanisms, datasets, species, or claims absent from the source.
- When revising from an existing Chinese abstract, keep the order of major information broadly parallel unless reordering is needed for English readability. Mention any reordering in risk notes.
- If the user requests or permits a freer English abstract, still provide a brief correspondence check showing that the background, objective, methods, results, and conclusions remain aligned with the Chinese version.

## Introduction And Literature Review

Edit introductions and literature reviews to be systematic, authoritative, measured, and logically cumulative.

- Move from broad field context to focused knowledge gap and dissertation rationale.
- Improve topic sentences and transitions between themes.
- Avoid paper-by-paper listing when thematic synthesis is possible.
- Synthesize by biological process, mechanism, material, method, phenotype, or research question.
- Preserve cited claims exactly in strength. Do not add "已有研究普遍认为" unless supported by the source.
- Flag unsupported claims as needing citations.
- End by leading naturally to the thesis objectives, not by overclaiming novelty.

Preferred conservative expressions:

- "相关机制尚不完全清楚"
- "仍需进一步阐明"
- "为...提供参考"
- "有助于理解..."
- "在...方面仍缺乏系统研究"

## Materials And Methods

Edit methods for clarity, chronology, and reproducibility.

- Keep reagent names, instrument models, software versions, parameters, concentrations, temperatures, durations, sample information, and protocol details unchanged.
- Do not add controls, replicates, normalization methods, statistical tests, or validation steps.
- Use consistent procedural phrasing: "按照...说明书进行", "参照...方法并略作修改", "每个处理设置...个生物学重复".
- Standardize units and symbols when safe: mg/L, μmol/L, ℃, min, h, rpm, g, mL, μL.
- Check Latin species names: genus capitalized, species lowercase, italicized where formatting is available, e.g. *Arabidopsis thaliana*, *Oryza sativa*.
- Keep gene names italicized where appropriate and proteins non-italicized, following the source and field convention.
- Do not change gene/protein capitalization unless correcting an obvious inconsistency.
- Keep statistical descriptions limited to what is present: software, test, correction, threshold, and replicate type.

## Results

Edit results to present observation, comparison, statistical evidence, figure/table reference, and limited interpretation.

- Keep numerical values, percentages, fold changes, p-values, sample sizes, gene IDs, treatment names, time points, and figure/table references unchanged.
- Use "显著" only when statistical significance is explicitly reported.
- Distinguish "显著升高/降低", "差异不显著", "呈上升趋势", and "无明显变化".
- Do not convert correlation into causation, expression change into functional proof, or phenotype association into mechanism.
- Avoid unsupported words such as "证明", "决定性作用", "完全解释", and "显著促进机制".
- If results contain methods or discussion, lightly move or rephrase only when the destination is clear; otherwise flag it.
- Keep figure/table references near the relevant result and consistent, e.g. "图3-1", "表4-2".

## Discussion

Structure discussion around evidence, comparison, mechanism, and implication.

Use this order when appropriate:

1. Summarize the key finding without repeating all results.
2. Interpret the finding in relation to the research question.
3. Compare with existing understanding only if supplied by the user/source.
4. Discuss plausible mechanisms with cautious modal language.
5. State implications within the study scope.
6. Note unresolved issues when needed.

Use evidence-aligned wording:

- Observational/correlation: "相关", "提示", "可能与...有关"
- Controlled experiment/mechanistic evidence: "表明"; use "证明" only when directly supported
- Omics/screening/speculation: "推测", "可能参与", "有待进一步验证"

Avoid broad agricultural or production claims from limited greenhouse, pot, single-year, single-location, or single-genotype evidence.

## Conclusions, Innovation, Limitations, Outlook

### Conclusions

- Write 3-5 focused points for long chapters or the full thesis.
- Each point should contain finding, scope, and restrained significance.
- Do not introduce new data, citations, or mechanisms.
- Avoid "彻底阐明", "完全证明", and unsupported universality across species, regions, years, or production systems.

### Innovation Points

- Ground every innovation in actual thesis work.
- Prefer "在...方面进行了拓展/完善/补充" over absolute "首次".
- Use "可能的创新点" if priority has not been verified.
- Separate methodological, material, theoretical, and application-oriented innovations.
- Avoid "填补国内外空白", "开创性", "颠覆性", and "重大突破" unless explicitly documented.

### Limitations

Write limitations frankly but constructively.

Common dimensions include limited genotype/material range, environmental conditions, years/locations, sample size, validation depth, indirect mechanistic evidence, omics results needing functional validation, and field-scale applicability.

### Outlook

- Link each future direction to a limitation or unresolved question.
- Prefer feasible extensions over slogans.
- Mention application only when supported by the thesis materials, traits, models, or methods.
- Suitable directions include expanding germplasm validation, multi-year/multi-location testing, functional validation of candidate genes/pathways, and integration of transcriptomics, metabolomics, phenomics, genetics, or physiology when already relevant.

## References And Citations

School or department dissertation guidelines override all other rules.

If no school rule is supplied, default to GB/T 7714-2015. GB/T 7714-2025 has been released as a replacing standard and is scheduled to take effect on 2026-07-01; use it only when the school or user explicitly adopts it. Do not mix reference styles unless the school template requires it.

### Adding References When Permitted

Only add background literature or citations when the user explicitly asks for or permits added background. Before adding any reference:

- Verify that the paper exists using at least two reliable sources when possible, such as the publisher page, DOI.org, Crossref, PubMed, Web of Science, Google Scholar, journal website, or official database records.
- Verify that the DOI resolves and matches the exact title, author list, journal, year, volume/issue, and page/article number.
- If sources disagree, do not add the reference as confirmed; flag it for user verification.
- Do not cite review articles as evidence for a specific primary experimental result unless the text makes clear it is a review-based background statement.
- Do not cite papers from memory. If online verification is unavailable, mark the citation as unverified and ask the user for the source details.
- In risk notes, list newly added references and state how they were verified, especially DOI verification.

Citation checks:

- Ensure every in-text citation has a matching bibliography entry.
- Ensure every bibliography entry is cited, unless the school allows uncited references.
- Preserve citation keys, numbering, and order when changing them may break cross-references.
- For numeric styles, check order of first appearance unless the school specifies otherwise.
- For author-year styles, check author names, years, and bibliography entries for exact consistency.

Reference safety:

- Do not invent missing authors, titles, journals, publishers, places, dates, pages, issue numbers, URLs, access dates, patent numbers, standard numbers, or dataset identifiers.
- Never fabricate DOI.
- Never alter a DOI to make it look plausible. Check DOI character by character against reliable sources.
- Flag missing required fields clearly.
- Preserve original Chinese and foreign-language titles unless correcting formatting, punctuation, capitalization, or style-required transliteration issues.

Common type markers under GB/T-style formatting include:

- journal article: [J]
- book: [M]
- dissertation/thesis: [D]
- conference/proceedings: [C]
- patent: [P]
- standard: [S]
- electronic resource: [EB/OL]
- database or dataset online: [DB/OL]

Check common fields:

- Journal article: authors, title, journal, year, volume, issue, pages, DOI if supplied/required.
- Book: authors/editors, title, edition if not first, place, publisher, year, cited pages if needed.
- Dissertation: author, title, degree type if required, institution, location if required, year.
- Conference paper: authors, paper title, proceedings/conference, editors if applicable, place, publisher, year, pages.
- Patent: owner/applicant, title, country/region, patent number, publication/announcement date.
- Standard: issuing body if required, standard number, title, place/publisher if required, year.
- Dataset/web source: creator, title, resource type, date/update date, version, platform/publisher, URL or persistent identifier, access date if required.

## Final Checklist

Before returning edited text, verify:

- No facts, data, citations, methods, references, or conclusions were invented.
- Any added background or citation was explicitly permitted by the user and verified through reliable sources.
- The edit improves originality and academic integrity without attempting to evade plagiarism or AI-detection systems.
- Claim strength matches the provided evidence.
- Technical terms, species names, genes/proteins, units, statistics, and figure/table references are consistent.
- Chinese thesis style is formal, precise, logical, and conservative.
- English abstract, if edited, is internationally readable without changing meaning.
- Risk notes identify unresolved uncertainties and places needing author verification.
