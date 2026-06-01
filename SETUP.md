# Pushing the Bundle to `cybermahaguru/sevenailawsbook`

Your repo already exists at https://github.com/cybermahaguru/sevenailawsbook and already has a README. This guide adds everything else (LICENSE, CONTRIBUTING, issue templates, etc.) without disturbing what you have.

You have two paths. **Pick one — don't do both.**

---

## Path A — Web UI (no terminal needed)

Best if you're not comfortable with git or just want it done in 10 minutes.

1. Go to https://github.com/cybermahaguru/sevenailawsbook
2. Click **Add file → Upload files** at the top of the file list.
3. Drag in these from your outputs folder:
   - `LICENSE`
   - `CONTRIBUTING.md`
   - `CODE_OF_CONDUCT.md`
   - `CITATION.cff`
   - `CHANGELOG.md`
   - `SECURITY.md`
   - `.gitignore`
4. Scroll down → commit message: `chore: add governance files (license, contributing, security, citation)` → **Commit changes**.
5. Click **Add file → Create new file**. In the filename box, type:
   `downloads/README.md`
   Paste the contents of your local `downloads/README.md`. Commit.
6. Repeat step 5 for each `.github/` file:
   - `.github/FUNDING.yml`
   - `.github/PULL_REQUEST_TEMPLATE.md`
   - `.github/ISSUE_TEMPLATE/config.yml`
   - `.github/ISSUE_TEMPLATE/errata.yml`
   - `.github/ISSUE_TEMPLATE/case_law_update.yml`
   - `.github/ISSUE_TEMPLATE/translation_proposal.yml`
   - `.github/ISSUE_TEMPLATE/dissent.yml`

   (Typing `path/to/file` in the filename box auto-creates the folders.)
7. Skip your existing `README.md` — yours is already up. If you ever want to replace it with the slightly polished one in this bundle, open the existing README in the GitHub UI, click the pencil icon, paste, commit.

---

## Path B — Terminal (faster, recommended)

Best if you have git installed and know the basics.

### Step 1 — Clone the existing repo into a fresh folder

```bash
cd ~                                       # or wherever you keep code
git clone https://github.com/cybermahaguru/sevenailawsbook.git
cd sevenailawsbook
```

### Step 2 — Copy the bundle files into the clone

Replace `<OUTPUTS>` with the path to your Cowork outputs folder.

```bash
# from inside the cloned repo
OUTPUTS="<paste the full path to your outputs folder here>"

cp "$OUTPUTS/LICENSE" .
cp "$OUTPUTS/CONTRIBUTING.md" .
cp "$OUTPUTS/CODE_OF_CONDUCT.md" .
cp "$OUTPUTS/CITATION.cff" .
cp "$OUTPUTS/CHANGELOG.md" .
cp "$OUTPUTS/SECURITY.md" .
cp "$OUTPUTS/.gitignore" .

mkdir -p downloads
cp "$OUTPUTS/downloads/README.md" downloads/

mkdir -p .github/ISSUE_TEMPLATE
cp "$OUTPUTS/.github/FUNDING.yml" .github/
cp "$OUTPUTS/.github/PULL_REQUEST_TEMPLATE.md" .github/
cp "$OUTPUTS/.github/ISSUE_TEMPLATE/"*.yml .github/ISSUE_TEMPLATE/
```

> **Note on the README:** the bundle's `README.md` is essentially identical to yours. If you want to overwrite, also run `cp "$OUTPUTS/README.md" .` — otherwise skip it.

### Step 3 — Commit and push

```bash
git add .
git status                                 # quick sanity check
git commit -m "chore: add governance files (license, contributing, security, citation, issue templates)"
git push origin main
```

That's it. Go to https://github.com/cybermahaguru/sevenailawsbook and you'll see the new files, plus a "Cite this repository" button and a Sponsor button appearing on the right.

---

## After the push — turn on the features that just unlocked

1. **Enable Discussions** — Repo → Settings → General → Features → tick **Discussions**. Your issue-template `config.yml` already routes general debate there.
2. **Add About metadata** — On the repo home page, click the cog icon next to "About":
   - **Description:** `Open-access book on the constitutional governance of AI. CC-BY 4.0. The Mali Doctrines and the Seven Laws of AI by Adv. (Dr.) Prashant Mali.`
   - **Website:** `https://archive.org/details/seven-ai-laws-the-future-of-mankind-by-prashant-mali`
   - **Topics:** `ai-law` `ai-governance` `ai-policy` `responsible-ai` `tech-law` `cyber-law` `open-access` `open-book` `creative-commons` `jurisprudence` `philosophy-of-ai` `mali-doctrines` `seven-laws-of-ai` `india-law` `regulation-of-ai` `agi-safety`
3. **Tag a release** — Releases → **Draft a new release** → Tag `v1.0.0` → Title `Seven AI Laws — First Edition (v1.0.0)` → paste the v1.0.0 section from `CHANGELOG.md` into the description → **Publish release**.
4. **Get a DOI (free, 5 minutes)** — Log in to [Zenodo](https://zenodo.org) with your GitHub account → flip the switch ON next to `sevenailawsbook` → re-publish the release (or draft a `v1.0.1`). Zenodo mints a DOI and archives the snapshot. **Now the repo is citable in any peer-reviewed venue.** This is the single highest-leverage move for academic adoption.
5. **Pin the repo** on your GitHub profile (your profile page → Customize your pins).

---

## Optional polish

- **Social preview image** — Settings → General → Social preview → upload a 1280×640 PNG with the book cover + title. Boosts click-through when the link is shared on LinkedIn / X.
- **Verified domain** — if you control `prashantmali.com`, add it as a verified domain in your GitHub profile settings. Adds a green tick to the "Sponsor" link.
- **Wiki** — leave off. The book itself is the wiki.

---

## Sanity checklist

After the push:

- [ ] LICENSE shows up on the repo home page sidebar as "Creative Commons Attribution 4.0 International"
- [ ] "Cite this repository" button appears (top right of the file list)
- [ ] Sponsor button appears (top of the file list)
- [ ] New issue page shows your three structured templates + Discussions link
- [ ] Discussions tab is enabled
- [ ] Repo description, website, and topics are set
- [ ] Release `v1.0.0` exists
- [ ] (Optional) Zenodo DOI minted

When all those are ticked, you're done. The repo is now a permanent, citable, contributable home for the book — and the launch playbook from the earlier message becomes the next chapter.
