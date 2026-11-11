# Momente Wortschatz

Karteikarten-, Verb-, Grammatik- und telc-B1-Trainer, Deutsch → Русский.
**2040 Wörter** in vier Decks, mit Artikeln, Pluralformen, Perfektformen und Beispielsätzen:

| Deck | Inhalt |
|---|---|
| **Kurs A1–A2** | 799 Wörter aus den 37 Lektionen von *Momente* |
| **B1-Wortschatz** | 1034 Wörter in 15 Themendecks, darunter *telc B1 · Lesen* |
| **Redemittel** | 130 Prüfungswendungen in 5 Gruppen |
| **Präpositionen & Konjunktionen** | 77 Funktionswörter mit Kasus bzw. Satzstellung |

Jedes Wort ist nach Wortart getaggt — Nomen, Verben, Adjektive, Adverbien,
Funktionswörter, Wendungen, Sätze — und die Leiste über der Karte schaltet sie mit
einem Tipp um, wenn du nur eine Wortart üben willst.

One self-contained `index.html` — no build step, no dependencies, no server.
Progress is stored in the browser's `localStorage` and can be exported/imported as text.

## Modes

| Mode | What it does |
|---|---|
| **Karten** | Flashcards with Leitner spaced repetition (boxes at 0 / 1 / 3 / 7 / 21 days) |
| **Auswahl** | Multiple choice, distractors drawn from the same part of speech |
| **der·die·das** | Article drill on the 286 nouns |
| **Tippen** | Type the German; umlaut keys provided, `ae/oe/ue/ss` accepted |
| **Verben** | Five conjugation drills — see below |
| **Grammatik** | Eight grammar drills — see below |
| **telc B1** | Five exam trainers — see below |
| **Leben in DE** | Einbürgerungstest practice and mock exam — see below |
| **Liste** | Searchable list; translations can be blurred for self-testing |

Keyboard: `Space` flip · `1` `2` `3` rate · `S` star · `→` skip · `1`–`4` pick an option · `Enter` check / continue.

Use **Deck** (top right) to choose between the course list and the B1 themes, filter by
lesson date or theme, switch direction, or narrow to due / starred / unseen words.

### Verben — 118 items

| Drill | Task |
|---|---|
| **Stammformen** | Infinitiv → Präteritum → Perfekt, e.g. `gehen — ging — ist gegangen` |
| **Präsens** | Conjugate for a random pronoun; stem changes and separable prefixes included |
| **Präteritum** | Pick the 3rd-person form from four candidates of the same class |
| **Modalverben** | Präsens and Präteritum of the six modals plus `möchten` |
| **Reflexiv** | `mich` or `mir` — Akkusativ vs Dativ reflexive pronouns |

### Grammatik — 321 items

| Drill | Task |
|---|---|
| **Perfekt** | Pick `hat`/`ist`, type the Partizip II (121) |
| **Verb + Präposition** | Pick the preposition, then its case (40) |
| **Wo & Wohin** | Wechselpräpositionen: Dativ for position, Akkusativ for direction (26) |
| **Konnektoren** | `weil` / `denn` / `deshalb` / `obwohl` and the word order each forces (30) |
| **Adjektivendungen** | The ending for that article word, gender, case and number (30) |
| **Konjunktiv II & Passiv** | `würde` / `hätte` / `wäre` / `könnte`, and `wird`/`wurde` + Partizip II (25) |
| **Relativsätze & Genitiv** | Relative pronoun by case, `dessen`/`deren`, and Genitiv endings (25) |
| **Partizip I** | Build `Infinitiv + d`; feedback shows the adjectival use (24) |

Every answer shows the rule that decided it and an example sentence. Verb and grammar
progress is tracked separately from the vocabulary deck, under keys prefixed `v:` and `g:`.

### telc B1 — exam practice

| Trainer | What it gives you |
|---|---|
| **Sprachbausteine 1** | 6 texts × 6 grammar gaps, four options each (36 items) |
| **Sprachbausteine 2** | 6 texts × 6 vocabulary gaps from a 12-word box (36 items) |
| **Leseverstehen** | 3 matching sets, 4 articles with 5 questions each, 2 situation sets (55 items) |
| **Schreiben** | 12 letter tasks with Leitpunkte, a word counter, a model answer and task-specific tips |
| **Sprechen** | 8 + 10 + 10 cards for the three Prüfungsteile, each with its own phrases |

All of it is original practice material written in the exam's published format — not
reproduced past papers. Schreiben and Sprechen run unscored, as practice; the other
three are scored and feed the same Leitner boxes under keys prefixed `t:`.

There is no Hörverstehen trainer: that part needs audio, which this app has none of.

### Leben in Deutschland — the official 310 questions

The complete official question catalogue: **300 general questions + the 10 for Bayern**,
in BAMF's own wording, with an English translation under every question and option
(the **EN** button toggles it).

**Üben:** all 310, or just the general block, or just Bayern; each answer shows which
option is right and why. **Prüfung:** 33 questions drawn at random — 30 general plus 3
on Bayern, as in the real test — answered without feedback, then scored against the
pass mark of 17, with every missed question listed and explained.

Provenance: the questions were extracted from the BAMF *Gesamtfragenkatalog* PDF
(Stand 07.05.2025). That PDF publishes no answer key, so the key was taken from BAMF's
own practice application at `oet.bamf.de` and cross-checked question by question —
an independently derived set of answers agreed with it on all 305 it had committed to.
Explanations and translations are written for this app.

8 questions show a picture in the real exam (coats of arms, the EU flag, a ballot
paper, the occupation-zone map, Bavaria on a map). They carry a **Bildfrage** badge;
the correct answer and an explanation of what the picture shows are given, since the
image itself isn't reproduced here.

Three questions depend on the current legislative period — the Chancellor, the Head of
State and the two largest Bundestag groups. They are keyed to the position as of
October 2026; the Bundespräsident answer has a known expiry, as the Bundesversammlung
meets in January 2027.

The Bayern block applies if you register for the test in Bayern. Another Bundesland
means a different set of ten.

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
| `s` | deck: `k` = course, `b` = B1, `r` = Redemittel, `f` = function words |
| `l` | lesson number · `t` lesson date (course words) · `th` theme index (all other decks) |
| `p` | `noun` · `verb` · `adj` · `adv` · `func` · `phrase` · `sentence` |
| `g` | gender: `der` / `die` / `das` · `n` plural ending · `v` Perfekt form |
| `e` | examples: `[["Deutsch","Русский"], …]` |

Adding a word means appending one object with a fresh `i`. Changing an existing `i`
detaches that word from its saved progress.

`const THEMES = […]` after it lists the B1 theme names; a B1 word's `th` is an index into it.

The drills sit in `const GRAM = {…}` and `const VERBS = {…}`:

```js
perfekt: ["essen","hat","gegessen","есть","Ich habe eine Pizza gegessen.","unregelmäßig"]
p1:      ["weinen","weinend","плакать","das weinende Kind","плачущий ребёнок"]
vp:      ["warten","auf","A","ждать чего-либо","Ich warte auf den Bus.","Я жду автобус."]
ww:      ["Das Buch liegt ","auf dem","auf den"," Tisch.","wo","liegen → wo? → Dativ","Книга лежит на столе."]

// konn / adj / konj / rel all share one shape:
["Ich bleibe zu Hause, ___ ich krank bin.","weil",["denn","deshalb","trotzdem"],"weil → Verb ans Ende.","…"]

VERBS.stamm:    ["gehen","идти","gehst","geht","ging","ist","gegangen","stark"]
VERBS.modal:    ["können","мочь","kann","kannst","kann","können","konnte","hat gekonnt","Ich kann gut schwimmen."]
VERBS.reflexiv: ["sich freuen","радоваться","A","Ich freue mich auf das Wochenende.","Я радуюсь выходным."]
```

In `ww` and the four multiple-choice sets the full sentence is `start + answer + rest`;
the field after the prompt is the correct answer, then the distractors.

`VERBS.stamm` drives three drills at once — the Präsens forms for *ich / wir / ihr / sie*
are derived from the infinitive by rule, with `PRES_FULL` holding the five verbs
(`sein`, `haben`, `werden`, `wissen`, `tun`) that no rule predicts. Add an irregular verb
there too, or the drill will generate a wrong form for it.

Progress is keyed by array position, so inserting a row mid-array shifts the saved state
of every row after it — append instead.
