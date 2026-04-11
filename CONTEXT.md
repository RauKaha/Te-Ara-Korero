# RauKaha — Te Ara Kōrero: Context File

## About the app
Te Ara Kōrero is an interactive te reo Māori sentence building game for 
Year 1–8 students. Students read an English sentence and build its Māori 
translation by selecting and arranging colour-coded word tiles. Each colour 
represents a different grammatical category (tense marker, verb, noun etc.).

## About RauKaha
RauKaha is the developer/brand behind this app. Core values: growth, 
knowledge, language, innovation, creativity, and inspiration. The app is 
intended for commercial licensing to kura and kāhui ako in Aotearoa 
New Zealand.

## Current build
- Single HTML file (index.html) — no frameworks, no external dependencies
- Vanilla HTML, CSS, and JavaScript only
- Responsive design, light and dark mode supported
- Hosted on GitHub (no license — all rights reserved)

## App structure
Two tabs:
1. Ngā Taumata (Levels) — four levels: Emerging, Developing, Proficient, 
   Mastery. 25 sentences each.
2. Ngā Kaupapa (Topics) — nine topics: Kura, Taiao, Hākinakina, Kāinga, 
   Marae, Kai, Toa, Pāmu, Haerenga. 25 sentences each.

## Design system
- Flat, clean design — no gradients, shadows, or decorative effects
- CSS variables for all colours (light/dark mode auto-adapt)
- Font: system font (var(--font-sans))
- Colour-coded word categories:
  - Tohu wā (tense marker): green (#E1F5EE / #085041)
  - Kupu Mahi (verb): blue (#E6F1FB / #0C447C)
  - Kupu Tohu (determiner): orange-red (#FAECE7 / #712B13)
  - Kupu Ingoa (noun): amber (#FAEEDA / #633806)
  - Kupu Āhua (adjective): pink (#FBEAF0 / #72243E)
  - Kupu Tūhono Wāhi (location): purple (#EEEDFE / #3C3489)
  - Kupu Tūhono (connective): grey (#F1EFE8 / #444441)
  - Kupu Whakarerekē (modifier): olive/brown (#EAF3DE / #27500A)
  - Kupu Whakapiki (intensifier): near-black (#2C2C2A / #D3D1C7)
  - Kupu Ingoa subject (pronoun): light red (#FCEBEB / #791F1F)

## Game mechanics
- English sentence shown prominently as the translation prompt
- Shuffled word pool (correct words + 3–5 distractors)
- Placed tiles clickable to remove
- Buttons: Tūtohu (check), Ūkui (clear), Āwhina (hint), Panuku (next)
- Colour key shown per question
- Progress bar, score tracker, streak counter
- Sentences shuffle randomly each session
- Star rating on completion (★★★ 80%+, ★★☆ 50%+, ★☆☆ below)

## State management
Two separate state objects:
- lState: levels tab (level, qIdx, placed, score, total, streak, 
  phase, checked, queue)
- kState: topics tab (kaupapa, qIdx, placed, score, total, streak, 
  phase, checked, queue)

## Bilingual UI labels
- Tīmata — Start
- Tūtohu — Check
- Ūkui — Clear
- Āwhina — Hint
- Panuku — Next
- Anō — Try again
- Taumata hou — Next level
- Whakamāoritia — Translate into te reo Māori
- Tō rerenga — Your sentence
- Ngā Taumata — Levels
- Ngā Kaupapa — Topics

## Vocabulary source
Word lists drawn from Te Ara Kōrero PDF resource covering:
Tohu wā, Kupu Mahi, Kupu Āhua, Kupu Tohu, Kupu Ingoa, 
Kupu Tūhono Wāhi, Kupu Tūhono, Kupu Whakapiki, Kupu Whakarerekē

## Known issues / limitations
- No audio/text-to-speech yet
- No persistent progress (localStorage not implemented)
- No teacher dashboard
- Mobile layout needs improvement at small screen sizes
- No onboarding/tutorial for first-time users

## Planned improvements
See TASKS.md for full prioritised list.

## Session instructions for Claude Code
When starting a new session:
1. Read this file (CONTEXT.md) for full project context
2. Read TASKS.md for current priorities
3. Read index.html to understand the current build state
4. Confirm what you understand before making changes
5. Make one feature change at a time and confirm before moving on
6. Do not change existing working functionality unless explicitly asked
7. Preserve all existing sentence data — do not remove or alter any 
   Māori sentences or translations
