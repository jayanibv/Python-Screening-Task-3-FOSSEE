# **Research Plan**

## Approach and evaluation
The plan starts by surveying open-source, code-focused models that can both read Python and follow instructions to produce rubric-aligned, probing prompts—without leaking solutions. The shortlist focuses on instruction-tuned, code-specialized models with solid Python performance and longer context windows, like Code Llama – Instruct/Python, plus a small baseline (e.g., StarCoder or CodeBERT for analysis-only scenarios). The evaluation harness is lightweight: take CS1/CS2-style problems with unit tests, ingest student submissions, and ask the model to 
1) Identify likely misconceptions (e.g., off-by-one, shadowing, mutable default args, early returns, misuse of recursion),
2) Generate probing, concept-focused questions (not fixes), and
3) Provide rubric-anchored formative feedback with criteria like correctness, reasoning, style, and edge cases.

## Testing and validation
Validation happens in two phases. Offline: measure misconception detection against an annotated set (precision/recall), check prompt usefulness with short instructor ratings (clarity, relevance, likelihood of eliciting self-explanation), and add a simple “no-solution-leak” check. Instructor-in-the-loop: run on a small batch of prior submissions and compare model prompts/feedback to instructor expectations, then iterate on prompt templates and rubric specificity. Decision-making favors models that balance accuracy, instruction-following, and interpretability via rubric-grounded outputs, while being feasible to run locally at low cost.
