## Python Screening Task 3: Evaluating Open Source Models for Student Competence Analysis

This repository contains a short, focused submission for the screening task: a two‑paragraph research plan, the required reasoning answers, and brief setup notes to make review painless. The plan centers on evaluating an open-source, instruction‑tuned, code‑specialized model (Code Llama – Instruct/Python) for analyzing student Python code and generating probing prompts that assess conceptual understanding without revealing solutions.

# What’s inside

RESEARCH_PLAN.md — Two paragraphs covering the approach to identify/evaluate models, how applicability would be validated, and the decision‑making rationale.

REASONING.md — Direct answers to the required questions: suitability for competence analysis, how to test prompt meaningfulness, trade‑offs, and model choice with strengths/limitations.

REFERENCES.md — Links to model cards, official repos, and key papers that inform the approach (Code Llama model cards/prompt formats; rubric‑guided evaluation research).

# How to review

Start with RESEARCH_PLAN.md to see the evaluation approach and the validation plan at a glance.

Open REASONING.md for the bullet answers the task requires, including trade‑offs and the final model choice.

Use REFERENCES.md to jump to the model cards and papers if you want to verify details or prompt formats quickly.

# Setup notes (lightweight)

No code execution is required for this submission; the plan describes a lightweight harness using unit tests, rubric‑anchored prompts, and instructor ratings for validation, which is standard for evaluating instruction‑tuned code models in an educational setting.

If you later prototype, the Code Llama instruct variants provide clear prompt formats and can run locally or via common platforms; use the instruct/chat templates as documented in the model cards and official guidance for stable results.

# Model focus and rationale.

Code Llama – Instruct/Python is open, instruction‑tuned, and optimized for code understanding/generation, including Python‑specialized variants and longer context support, making it a strong fit for competence‑oriented, rubric‑guided prompting.

Prompting guidance and instruct formats are documented by Meta and platform partners, which helps ensure consistent, safe, non‑leaking prompts during analysis and question generation.
