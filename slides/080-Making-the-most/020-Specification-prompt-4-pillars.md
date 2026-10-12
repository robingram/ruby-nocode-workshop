---
template: title
---

# Getting the most out of limited credits

## "Specification Prompt" Framework - 4 Pillars

1. **Context & placement:** Where are we working? What existing views or components are touched?
2. **Functional requirements (numbered):** What are the explicit user actions and expected UI changes?
3. **Negative constraints & permissions:** What must NOT happen? Who is allowed to do what?
4. **Polish & edge states:** Empty states, loading, mobile layout, feedback toasts.

---

1. Context & Placement

Why it matters: AI tools scan the codebase before editing. If you don't anchor the change, the model might invent a new page instead of modifying an existing one, or mount a modal in the wrong container.

Example:

"In the Song Library view (/songs), add search and filter controls directly above the song grid/table..."

2. Numbered Functional Requirements

Why it matters: LLMs follow ordered lists with significantly higher fidelity than dense paragraphs of prose. Each numbered point acts as a discrete sub-task the model can check off during its plan-and-code loop.

Format: Action 
→
→ Target 
→
→ Result.

Example:

Search Input: Instant, case-insensitive filter across title, artist, and album.

Genre Pills: Dynamically list unique genres found in the songs table with an 'All' toggle.

Sort Menu: Sort by Title (A-Z), Release Date (newest), Duration (shortest).

3. Negative Constraints & Permissions ("The Guardrails")

Why it matters: This is the #1 credit-saver. Models are biased toward the "happy path" unless explicitly told what not to allow. Defining negative constraints up front prevents security holes and logical flaws.

Example:

"If the user is NOT authenticated, do NOT allow playback or playlist creation. Instead, trigger a sign-in toast/modal."
"Do NOT allow adding the same song to a playlist more than once."

4. Polish & Edge States

Why it matters: In software engineering, handling [] (empty set) and error states takes half the work. Calling them out in the initial prompt avoids the dreaded "blank white screen when no search results match".

Example:

"If no songs match the search/filters, show an empty state with a 'Clear filters' button."
"When docked at the bottom, ensure the player bar doesn't overlap or hide the last row of songs (add bottom padding)."
