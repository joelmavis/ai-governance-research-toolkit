---
name: learning-assistant
description: Turn a book, chapter, academic paper, research report, or course material into a structured, source-bounded learning note for later research. Use when the user wants to understand and retain a provided learning material; do not use for web research, content creation, or final research conclusions.
---

# Learning Assistant

Create a structured learning note from a provided PDF, Markdown, or text material. The goal is to extract, understand, connect, and retain knowledge without replacing the user's intellectual judgment.

## Inputs

Require a source material. An optional current research question may guide emphasis, but must not change what the source says.

Supported v1.0 inputs are books or chapters, academic papers, research reports, and course handouts or transcripts in PDF, Markdown, or text format. Run scripts/prepare_material.py first when a local file needs text extraction or a type candidate. If extraction fails, report the exact limitation and ask for readable text; do not infer from a filename or external knowledge.

## Workflow

1. Read the material before drafting. Identify the material type, central question, claims, stated evidence or method, concepts, disagreement, and limits.
2. Classify one primary domain and, only when genuinely useful, one secondary domain from references/output-contract.md.
3. Distinguish throughout between the author's claim, source-supported evidence, and the skill's explicitly labelled inference.
4. Connect the material to the user's supplied research question or selected domain. This explains possible usefulness; it is not a conclusion.
5. Produce exactly the seven sections and frontmatter in templates/learning-note.md. Do not add executive summaries, scores, web links, content ideas, or extra sections.
6. Run scripts/validate_note.py on the saved note and correct structural failures before delivery.

## Source and judgment rules

- Treat the supplied material as the authority. Do not silently fill gaps with model knowledge.
- If an external fact is necessary, label it **外部补充：** and state that it is not from the material. Do not use external research in v1.0 unless the user explicitly requests it.
- If evidence, method, metadata, or a claim is not adequately described, write **材料中未充分说明。**
- Do not collapse disagreement. When relevant, state A认为…；B认为…；作者倾向于… and identify whose position is whose.
- Core claims must be complete propositions, not topic labels. Limit claims, concepts, and follow-up questions to five, five, and three respectively.
- 我的判断候选 may contain only provisional, source-connected possibilities and must retain **待用户 / 研究负责人验证**. Never present it as the user's view or a final conclusion.

## Boundaries

This skill does not search the web, rank paper quality, generate an evergreen note, build a knowledge graph, sync databases, or turn research into public content. It does not decide what is true beyond the supplied material.

## Tests

Before changing the skill, run python3 -m unittest discover -s tests. The three source-dependent acceptance cases are in tests/cases/README.md; run them only with lawfully available source material.
