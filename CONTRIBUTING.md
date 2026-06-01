# Contributing to *Seven AI Laws*

> *"Law without technical literacy is blindness; technical development without legal wisdom is recklessness."*
> — From the Preface

Thank you for considering a contribution. This is a **living text**, and the strongest constitutions in history — from Magna Carta (1215) to the Indian Constitution (1950) — were sharpened by dissent, debate, and amendment, not by silence. Your edits matter.

---

## What you can contribute

| Type | What it looks like | How to file |
|------|-------------------|-------------|
| **Errata** | Typos, broken links, citation fixes | Issue or PR |
| **Case-law updates** | New judgments (post-April 2026) that strengthen, challenge, or apply a Doctrine | Issue with citation |
| **Annotations** | Scholarly commentary on a specific Law or Doctrine | PR to `/annotations/` |
| **Translations** | Full or partial translation into another language | Issue first → then PR |
| **Companion artefacts** | Infographics, slide decks, podcasts, video summaries, study guides | PR to `/companion/` |
| **Bibliographic additions** | Suggested further reading, related scholarship | Issue or PR to `/bibliography.md` |
| **Critique** | Disagreement, counter-arguments, alternative frameworks | Issue labelled `dissent` |

**Critique is welcome and protected.** A doctrine that cannot survive scrutiny is not a doctrine; it is a slogan.

---

## Before you start

1. **Search existing Issues and PRs.** Someone may already be working on it.
2. **For large changes**, open an Issue first to discuss scope. Small fixes can go straight to PR.
3. **For translations**, declare the language and your background so we can avoid duplication.

---

## Filing an Issue

Use the templates in `.github/ISSUE_TEMPLATE/`. At minimum:

- **What** — the section, page, or claim affected
- **Why** — what is wrong, missing, or worth adding
- **Sources** — for case-law and citation updates, please include the *full* citation (Bluebook, OSCOLA, or APA)

**Good example:**

> **Section:** Part V, Law III (on Algorithmic Transparency)
> **Issue:** The book cites *Loomis v. Wisconsin*, 881 N.W.2d 749 (Wis. 2016) but does not mention *State v. Pickett*, 466 N.J. Super. 270 (App. Div. 2021), which extended *Loomis*-style reasoning to probabilistic genotyping software. Worth adding for symmetry.
> **Source:** *State v. Pickett*, 466 N.J. Super. 270 (App. Div. 2021).

**Bad example:**

> "Section on AI is wrong, pls fix."

---

## Submitting a Pull Request

1. **Fork** the repository.
2. **Create a branch** named clearly: `errata/page-72-typo`, `annotation/law-iv`, `translation/hindi-preface`.
3. **Make minimal, focused commits.** One logical change per commit.
4. **Reference the Issue** in your PR description: `Closes #12`.
5. **Sign your work** by including your name and a one-line summary of credentials where relevant (e.g., "LL.M., NLSIU, 2024"). This is for transparency, not gatekeeping.

### Commit message style

```
<type>: <short summary>

<optional longer explanation>
<optional citation>
```

Types: `errata`, `case-law`, `annotation`, `translation`, `companion`, `bib`, `dissent`, `chore`.

Example:
```
case-law: add State v. Pickett to Law III commentary

State v. Pickett, 466 N.J. Super. 270 (App. Div. 2021)
extends Loomis-style reasoning to TrueAllele probabilistic
genotyping software.
```

---

## Translations

Under **CC-BY 4.0**, you may translate freely without permission. We ask only that you:

1. Open an Issue declaring the language and timeline.
2. Keep the original meaning. Where idiomatic translation requires a choice, footnote it.
3. Submit as a PR to `/translations/<language-code>/` (e.g., `/translations/hi/`, `/translations/fr/`).
4. You will be credited as **Translator** in the README and the translated file's frontmatter.

Translations of the **Preface, the Mali Doctrines (Part IV), and the Seven Laws (Part V)** are the highest priority — they are the shareable core.

---

## Standards we hold ourselves to

- **Cite everything.** Bluebook (21st ed.), OSCOLA, or APA — pick one and stay consistent within a contribution.
- **Distinguish description from argument.** When a doctrine is your view, say so. When it is settled law, cite it.
- **No ad hominem.** Critique ideas, not authors. The Mali Doctrines themselves are fair game; the author is not.
- **No silent edits to the author's voice.** Annotations live in `/annotations/`. The body text is amended only for errata.

---

## What we will not accept

- **Plagiarised material.** All contributions must be your original work or properly cited.
- **AI-generated commentary submitted as your own.** Using AI to draft is fine; passing it off as human scholarship is not. Disclose AI assistance in the PR.
- **Vendor or product promotion** disguised as commentary.
- **Edits motivated by personal, political, or commercial vendetta** rather than scholarship.
- **Removal of attribution** to the original author or to prior contributors. This violates CC-BY 4.0.

---

## Code of Conduct

By participating, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md). In short: argue hard, attack ideas, respect people. The same rules a good moot court would enforce.

---

## Questions?

Open a Discussion (preferred), or email **cyberlawconsulting@gmail.com**.

*Thank you for helping keep a text on AI governance itself governable — by humans, in the open.*
