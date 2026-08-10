# Linux Post Office — Product Vision

## Purpose

Linux Post Office is a small, friendly command-line learning game. It turns Linux tasks into mail deliveries: each letter presents a practical command challenge, and the player delivers it by entering the correct command.

## Player promise

The game should make a beginner feel that Linux commands are useful, memorable, and approachable. Every completed letter gives immediate feedback, a plain-language explanation, XP, and visible progress through a themed post-office route.

## Current experience

Players work through four unlocked-in-sequence learning levels:

1. **Morning Mail** — navigation: `pwd`, `ls`, `cd`
2. **Sorting Day** — files and directories: `cat`, `mkdir`, `find`
3. **Special Delivery** — searching and permissions: `grep`, `chmod`
4. **Night Route** — processes: `ps`, `kill`

For each letter, players can enter the post office, talk to the postmaster, read the mission, optionally walk to the destination, and submit a Linux command. A correct answer opens the letter, awards 50 XP, advances the level, and unlocks the next phase when all letters in a level are complete.

## Design principles

- **Learn by doing:** Command prompts are short, concrete tasks rather than definitions to memorize.
- **Use a clear metaphor:** The post office, letters, postmaster, and destinations provide a playful reason for each command.
- **Give immediate guidance:** Incorrect answers stay non-punitive and include a contextual hint; correct answers explain the command.
- **Show momentum:** Letter state, XP, level progress, map nodes, and visual scene changes make progression visible.
- **Support return visits:** Progress and terminal logs are stored in browser `localStorage`; reached levels remain selectable and completed levels can be replayed.

## Current boundaries

- This is a single static HTML experience with no server-side state.
- Commands are validated against predefined accepted strings; they are not run in a real Linux shell.
- Levels 5 and 6 appear in the learning-path copy but are not implemented in the game data or map.

## Near-term product direction

Complete the advertised learning path, broaden accepted command variants where appropriate, and add richer task context while preserving the quick feedback loop. A future practice mode could safely simulate command output so learners can explore before submitting an answer.
