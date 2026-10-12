---
template: title
---

# Getting the most out of limited credits

## "Specification Prompt" Framework - Comparison

❌ The Naive Prompt (Cost: 3–4 Build Credits)

"Add search to the songs and make a bottom audio player."
<br/>
<br/>

✅ The Specification Prompt (Cost: 1 Build Credit)

"In the song library, add real-time search across title/artist/album, clickable genre pills, and an empty state when no results match.<br/>
Add a fixed bottom player bar that simulates 30s playback of the selected track.<br/>
Constraint: Guests cannot play songs—clicking play prompts them to sign in.<br/>
Layout: Ensure bottom padding so content isn't obscured by the player."

---

What goes wrong:

Turn 1: AI builds a basic search bar that only checks title, and an audio player that breaks because there are no audio files.
Turn 2: "Make search work for artists too, and the player covers the songs at the bottom."
Turn 3: "Non-logged in users shouldn't be able to click play!"

Result: 3 credits spent, 20 minutes lost.

Specification prompt:

"In the song library, add real-time search across title/artist/album, clickable genre pills, and an empty state when no results match.
Add a fixed bottom player bar that simulates 30s playback of the selected track.
Constraint: Guests cannot play songs—clicking play prompts them to sign in.
Layout: Ensure bottom padding so content isn't obscured by the player."

Result: Handled correctly in a single turn.

