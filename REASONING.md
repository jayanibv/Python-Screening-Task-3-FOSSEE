## Required Reasoning Answers

**What makes a model suitable for high-level competence analysis?**

It needs strong Python understanding, reliable instruction-following, and enough context length to connect code symptoms to underlying concepts. It should generate probing questions that surface reasoning (e.g., invariants, mutation vs. immutability, recursion base cases) rather than propose full solutions. Models tuned for code with instruct variants tend to do better at pedagogical, dialog-style outputs.

**How would you test whether a model generates meaningful prompts?**

Pair unit-test signals and a question-specific rubric with a prompt template that asks for concept checks, not fixes. Have instructors rate each generated prompt on clarity, relevance to the detected misconception, and whether it’s likely to trigger a useful self-explanation. Track “no solution leakage” and reject prompts that reveal the final fix. A small annotated set helps quantify relevance and correctness.

**What trade-offs exist between accuracy, interpretability, and cost?**

Larger models can diagnose more subtle conceptual gaps but raise compute costs. Instruction-tuned, code-focused open models strike a good middle ground: they can run locally (lower recurring cost), and their rubric-grounded outputs are easier to interpret. The main trade-off is that careful prompt and rubric design is needed to stabilize quality, which adds a bit of setup effort.

**Why choose Code Llama – Instruct/Python? Strengths and limitations.**

Chosen because it’s open, code-optimized, instruction-tuned, and friendly to longer contexts. 
1. Strengths: solid Python performance, good at dialog-style probing, and works well with test-driven, rubric-anchored prompting. 
2. Limitations: variability without clear templates; benefits significantly from question-specific rubrics and a simple unit-test harness to provide concrete signals. Baselines like StarCoder or analysis models like CodeBERT can be referenced for comparison, but they’re generally less conversational for pedagogy.
