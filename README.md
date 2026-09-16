# Momente Wortschatz

Karteikarten-Trainer für den Wortschatz aus *Momente A1–A2*, Deutsch → Русский.
799 Wörter aus 37 Lektionen, mit Beispielsätzen, Artikeln und Pluralformen.

One self-contained `index.html` — no build step, no dependencies, no server.
Progress is stored in the browser's `localStorage` and can be exported/imported as text.

## Modes

| Mode | What it does |
|---|---|
| **Karten** | Flashcards with Leitner spaced repetition (boxes at 0 / 1 / 3 / 7 / 21 days) |
| **Auswahl** | Multiple choice, distractors drawn from the same part of speech |
| **der·die·das** | Article drill on the 286 nouns |
| **Tippen** | Type the German; umlaut keys provided, `ae/oe/ue/ss` accepted |
| **Grammatik** | Four drills — see below |
| **Liste** | Searchable list; translations can be blurred for self-testing |

Keyboard: `Space` flip · `1` `2` `3` rate · `S` star · `→` skip · `Enter` check / continue.

### Grammatik drills

| Drill | Task | Items |
|---|---|---|
| **Perfekt** | Pick `hat`/`ist`, type the Partizip II | 121 verbs |
| **Verb + Präposition** | Pick the preposition, then Dativ or Akkusativ | 40 pairs |
| **Wo & Wohin** | Wechselpräpositionen — Dativ for position, Akkusativ for direction | 26 sentences |
| **Partizip I** | Build `Infinitiv + d`; feedback shows the adjectival use | 24 verbs |

Every answer shows the rule that decided it and an example sentence. Grammar progress
is tracked separately from the vocabulary deck, under keys prefixed `g:`.

## Publish on GitHub Pages

The repository is already initialised with one commit and the remote set to
`https://github.com/arkkienkeli/arkkienkeli.github.io.git`. From this folder:

```bash
git push -u origin main
```

If the repository does not exist yet, create it on GitHub first — named exactly
`arkkienkeli.github.io`, public, with **no** README, .gitignore or licence
(an initialised repo will reject this push).

Then in the repo: **Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save**.

The site goes live at **https://arkkienkeli.github.io/** a minute or two later.

### If that repository already has a site in it

This push would replace it. To keep both, put the app in its own repository instead —
say `deutsch` — and it lands at `https://arkkienkeli.github.io/deutsch/`:

```bash
git remote set-url origin https://github.com/arkkienkeli/deutsch.git
git push -u origin main
```

Note: a public repository makes the vocabulary list public too.

## Editing the word list

The vocabulary sits in one line near the bottom of `index.html`:

```js
const DATA = [{"i":0,"d":"immer","r":"всегда","l":1,"t":"2026-02-14","p":"other"}, …];
```

| Key | Meaning |
|---|---|
| `i` | id — must stay unique, it's what progress is keyed on |
| `d` | German |
| `r` | Russian |
| `l` | lesson number · `t` lesson date |
| `p` | `noun` · `verb` · `phrase` · `sentence` · `other` |
| `g` | gender: `der` / `die` / `das` · `n` plural ending · `v` Perfekt form |
| `e` | examples: `[["Deutsch","Русский"], …]` |

Adding a word means appending one object with a fresh `i`. Changing an existing `i`
detaches that word from its saved progress.

The grammar drills sit in `const GRAM = {…}` just after it, as four arrays of rows:

```js
perfekt: ["essen","hat","gegessen","есть","Ich habe eine Pizza gegessen.","unregelmäßig"]
p1:      ["weinen","weinend","плакать","das weinende Kind","плачущий ребёнок"]
vp:      ["warten","auf","A","ждать чего-либо","Ich warte auf den Bus.","Я жду автобус."]
ww:      ["Das Buch liegt ","auf dem","auf den"," Tisch.","wo","liegen → wo? → Dativ","Книга лежит на столе."]
```

In `ww` the full sentence is `start + answer + end`, the second field is the correct
answer and the third the distractor; progress is keyed by position, so inserting a row
mid-array shifts the saved state of the rows after it — append instead.
