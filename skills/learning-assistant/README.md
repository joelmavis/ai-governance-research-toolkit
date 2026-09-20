# Learning Assistant

Learning Assistant turns a book, chapter, academic paper, research report, or course material into a structured learning note for later research.

它用于把学习材料沉淀为可复习、可检索、可继续用于研究的知识资产；不替读者形成最终观点。

## What it is for

It preserves the useful layer between raw highlights and an over-compressed summary:

Source material → structured extraction → research connection → reusable learning note

It identifies the material's question, claims, evidence, concepts, disagreements, and open questions. It then records bounded connections to a research direction.

## Who it is for

- Students and researchers reading books, papers, and reports.
- Policy, governance, technology, and international-affairs researchers building a long-term knowledge base.
- Professionals retaining what a course, report, or transcript actually argues before applying it.

It is general-purpose: the reader's research question is optional and can come from any field.

## Inputs

v1.0 accepts a provided book or chapter, academic paper, research or policy report, or course handout/transcript in PDF, Markdown, or plain-text form. An optional second input is the question the reader is trying to answer.

## Output

Every note uses one stable Markdown schema with seven sections:

1. Core question
2. Up to five core claims
3. Evidence and method stated in the source
4. Up to five core concepts
5. Bounded research relevance
6. Up to three follow-up questions
7. Candidates for concept notes, case notes, and provisional judgments

The skill selects one primary and, only when useful, one secondary domain: International Relations & IPE; European Politics; Technology Politics & Technological Sovereignty; AI Governance & AI Safety; or AI Industry & Infrastructure.

## How to use it

Install or copy this directory to your Codex skills directory, then ask:

Use $learning-assistant to read this paper. My current question is: How can technological dependence become state power? Create the structured learning note in English.

Or:

Use $learning-assistant to turn the attached report into a structured learning note in Chinese.

The output language follows the user's request. Keep source terminology in its original language where precision matters.

## Research safeguards

- Source first: the provided material is the authority.
- Clear boundaries: author claims, source evidence, skill inference, and external additions are not mixed.
- Missing information is labelled 材料中未充分说明。
- Disagreement is retained rather than flattened.
- Any 我的判断候选 is marked 待用户 / 研究负责人验证.

## Deliberate limits in v1.0

It does not search for supplementary sources, score material quality, write public content, build a knowledge graph, sync databases, or create final evergreen notes.

## Status

v1.0 is ready for source-bound pilot use. Three acceptance cases cover a paper, book chapter, and AI governance report; each requires a legally available original source and human comparison against it.
