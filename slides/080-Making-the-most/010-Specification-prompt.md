---
template: title
---

# Getting the most out of limited credits

## "Specification Prompt" Framework - Intro

* Prompting methodology tailored specifically for software engineers working with AI code generation tools
* Avoid the "Chatbot Trap" (Under-specifying)
* And the "PR Trap" (Over-specifying implementation)
* Aiming to hit the sweet spot: high functional precision, zero implementation micromanagement. Reads like an agile user story or an RFC task card

---

Chatbot trap: Treating the agent like ChatGPT and sending vague, one-sentence requests ("Make a music player"). This burns build credits because the AI has to guess the design, state structure, and edge cases, requiring 3–4 follow-up prompts to fix what it guessed wrong.

PR trap: Trying to dictate the exact React hook, CSS class, or variable name. This is tedious, wastes time, and often clashes with the project's existing architecture
