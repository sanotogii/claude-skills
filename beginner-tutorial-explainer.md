---
name: beginner-tutorial-explainer
description: Write technical explanations as friendly, from-scratch, numbered-section tutorials in the style of a good Medium/blog post for beginners. Builds intuition first with a small concrete problem, then definition, then a worked numeric example, then code, then common mistakes, an interview-style answer, a memory analogy, and a short final summary. Use this skill whenever the user asks to explain, teach, or write a tutorial, guide, or "explain like a blog post" on any technical concept (machine learning, programming, math, data, systems, web, etc.), or says "explain X from scratch", "explain X to a beginner", "make a tutorial on X", or "explain it like [this style]", even if they never name the style.
---

# Beginner Tutorial Explainer

This skill makes explanations feel like a patient teacher walking a beginner through a concept step by step. The signature of the style: **start from a problem the reader can see, not from a definition**, use tiny numbers they can verify by hand, and keep every paragraph short enough to skim.

The goal is not to sound impressive. The goal is that a reader finishes with the right *intuition*, can reproduce the key calculation themselves, and knows the mistakes to avoid.

## Voice and tone

- Friendly and direct. Use "we", "let's", "notice", "imagine".
- Talk to a smart beginner. Never condescend, never assume prior jargon without defining it.
- Short sentences. Many paragraphs are a single line. White space is a feature.
- Flag the reader's likely misunderstanding and correct it gently ("This doesn't automatically mean X. It simply means Y.").
- Stay accurate. Use hedges like "usually", "generally", "approximately", "often" where the truth is not absolute. Beginner-friendly is not the same as oversimplified to the point of being wrong.
- Use rhetorical questions as pivots: "Why?" followed immediately by the answer.
- Draw attention to the key observation after an example: "Notice what happened."

## Structure

Follow this skeleton, adapting or dropping sections that don't fit the topic. Number the main sections (`1.`, `2.`, ...) and phrase headings as plain questions or concept names.

1. **Opening hook (no number).** Two to four short paragraphs. Mention what learners usually focus on, then pivot with "But before..." to the overlooked concept. State what the tutorial will cover in one sentence.
2. **What Is the building block?** Define any prerequisite term (e.g. "What is a feature?") using a small concrete table or snippet. Show the pain point inside the example itself, so the need for the main concept appears before it is named.
3. **What Is [Concept]?** One plain-language definition, then a before/after illustration.
4. **Why Do We Need It?** Motivate with a worked failure case using small numbers and visible arithmetic. End with the corrected interpretation ("simply measured in a larger unit", not "100 times more important").
5. **Overview of the main variants or techniques.** Show a small tree diagram when there are two or more options.
6. **Each variant, in its own section:** formula in a plain code block, a legend of what each symbol means, a worked example with tiny numbers, then the code (library API) for it.
7. **Explain the mechanics of the API or method.** Break the important calls into their own short sections ("What does `fit()` mean?"), with a conceptual flow diagram.
8. **The most important rule or pitfall**, labeled as such, with a Do / Don't code pair and a "Why?" explanation.
9. **Comparison** of the variants (compact table or side by side before/after).
10. **When to use / when not to use** (which algorithms, cases, or situations), with one line of reasoning each.
11. **Complete runnable example** that ties everything together, followed by a pipeline diagram.
12. **What happens in production / real life** if relevant.
13. **Common beginner mistakes.** Use "Mistake 1: ..." headings, with Wrong and Correct snippets where applicable.
14. **Interview question** with a model answer in a quote-style paragraph, plus a one-line example to back it up.
15. **Easy way to remember.** One everyday analogy (e.g. mixing units like km and cm).
16. **Final Summary.** Exactly this shape: "Remember these N points:" as a short numbered list (3 to 6 items, one line each), then one bolded-in-spirit **core intuition** sentence that reframes the whole topic.

If the user wants a shorter piece, keep the order but compress: hook, problem, definition, one worked example, one code block, mistakes, summary.

## Formatting conventions

- Put formulas, small data, step-by-step arithmetic, and diagrams in **plain code blocks** (no syntax highlighting needed). They read cleanly in any renderer.
- Draw flows with arrows on separate lines:

  ```
  Dataset
     ↓
  Train/Test Split
     ↓
  Fit on training data
     ↓
  Transform
  ```

- Draw taxonomies as simple ASCII trees (`├──`, `└──`).
- Align small value lists in code blocks so ranges are comparable at a glance (`Age        → 22–40`).
- Show arithmetic line by line, one operation per line, including the intermediate step and the final approximate result.
- Show before/after transformations as `Original` then `↓` then `Scaled` or equivalent.
- Use tables only for genuine comparisons or small datasets. Use headings as numbered questions, not decorative titles.
- Inline `code` for function names, parameters, and variable names.
- No emojis. Avoid long bullet-point walls; prefer short paragraphs and code blocks.

## Worked-example rules

- Pick numbers a reader can check in their head: 20/30/40, 20,000/50,000/80,000, 25 vs 35.
- Walk through every step. Say what to compute, show the computation, state the result, then say what it means.
- If you simplify (for instance, "suppose the standard deviation is approximately 8.16"), say that you are simplifying.
- Use one running scenario across the whole tutorial when possible (the same loan dataset, the same Age/Salary example) so the reader's mental load stays low.
- After an example that shows a problem, add the sentence that prevents the wrong takeaway.

## Code rules

- Complete, runnable snippets with imports at the top.
- Small, readable toy data inline rather than external files.
- Name variables conventionally and consistently (`X_train`, `X_test`, `y_train`).
- Show the right way and the wrong way for the key pitfall, side by side.
- Explain what the code does in plain words right before or after it, never leave a block unexplained.

## Content principles

- **Intuition before formalism.** The reader should feel the problem before seeing the formula.
- **One idea per section.** If a section teaches two things, split it.
- **Repeat the key rule in different forms.** The core rule can appear as prose, as a code pair, as a diagram, and in the summary. Repetition is deliberate here.
- **Name the pitfall, then explain why.** Don't just say "never do X". Say what breaks and why.
- **Connect to practice.** Include a real-world angle (deployment, production, an app scenario) so the concept feels useful.
- **Respect the nuance.** Say "usually don't need" rather than "never need". Mention exceptions briefly.
- **End with the intuition, not a recap of syntax.** The last line should be the one sentence the reader remembers.

## Quick self-check before finishing

- Did the opening start from what learners already know, then pivot to the new concept?
- Did the reader see the problem in a concrete example before the definition?
- Is every formula followed by a legend and a tiny worked example?
- Is there a labeled "most important rule" with a Do/Don't pair?
- Are there at least one flow diagram and one analogy?
- Does the summary list a few numbered points and end with a single core-intuition sentence?
- Are paragraphs short, with no dense walls of text?
