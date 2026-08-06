# GitHub Profile Editorial Redesign Implementation Plan

> **For Hermes:** Use incremental implementation and verify each slice before deployment.

**Goal:** Replace the fragile widget-heavy GitHub profile with a concise, theme-aware, proof-first editorial profile and align the public GitHub metadata.

**Architecture:** The profile remains a static GitHub Markdown document. Two repository-owned SVG files provide light/dark hero variants through a Markdown `<picture>` element; all factual proof links point to Umer's website or the IEEE publication. Browser automation is used only for GitHub account metadata and pins that cannot be changed through the profile repository.

**Tech Stack:** GitHub Flavored Markdown, SVG, Git, GitHub web UI, Obsidian Markdown

---

### Task 1: Add the theme-aware editorial hero

**Objective:** Create durable light and dark hero assets that match the personal website and remain readable in both GitHub themes.

**Files:**
- Create: `assets/profile-hero-light.svg`
- Create: `assets/profile-hero-dark.svg`

**Steps:**
1. Create a 1200×360 SVG in the warm light palette with near-black text and a restrained red accent.
2. Create the equivalent dark SVG with warm off-white text and terracotta accent.
3. Validate both files as XML using Python's standard XML parser.
4. Render or load both assets and visually inspect legibility.

### Task 2: Replace the profile README

**Objective:** Make verified impact and selected work the central profile story.

**Files:**
- Modify: `Readme.md`

**Steps:**
1. Replace the typing image with a `<picture>` element using the two hero assets.
2. Add one compact row linking website, Zenovae, LinkedIn, and email.
3. Present four verified impact metrics.
4. Add concise sections for what Umer builds, selected work, core capabilities, and published research.
5. Link each selected-work row to its exact case-study URL and link the research directly to IEEE.
6. Remove visitor counters, stats cards, streak cards, trophies, top languages, duplicate CTAs, and the large badge wall.
7. Run a link and asset validation script; expect zero broken URLs.

### Task 3: Document and deploy the repository change

**Objective:** Preserve the approved rationale and publish the static profile update safely.

**Files:**
- Create: `docs/plans/2026-08-07-github-profile-editorial-design.md`
- Create: `docs/plans/2026-08-07-github-profile-editorial-plan.md`

**Steps:**
1. Review `git diff` and check for secrets.
2. Commit the design and plan separately from the visual/profile implementation when practical.
3. Push `main` to the profile repository.
4. Verify the raw README and SVG files are available on GitHub.

### Task 4: Align public GitHub metadata and pins

**Objective:** Remove the visible contradiction between the profile README and sidebar metadata.

**Files:** None; GitHub account settings and profile pins.

**Steps:**
1. Connect to Umer's authorized headed Chrome session.
2. Set display name to `Umer Farooq`.
3. Set the approved production-AI bio within GitHub's limit.
4. Preserve `umerfarooq.me` and the LinkedIn social link.
5. Remove forked pins.
6. Pin `openclaw-security-fix-cli`; add no weak filler repositories.
7. Re-open the public profile and verify sidebar metadata and pins.

### Task 5: Update the Obsidian source of truth

**Objective:** Make the existing vault accurate, sourced, and reusable.

**Files:**
- Modify: `C:\Users\umerf\Documents\Umer-Vault\Profile.md`
- Modify: `C:\Users\umerf\Documents\Umer-Vault\GitHub Profile Design Strategy.md`
- Modify: `C:\Users\umerf\Documents\Umer-Vault\GitHub Optimization Research.md`
- Modify: `C:\Users\umerf\Documents\Umer-Vault\README.md`

**Steps:**
1. Update the current GitHub state after deployment.
2. Add exact source URLs for GitHub docs, Reddit discussions, case studies, and IEEE.
3. Separate verified durable facts from time-sensitive GitHub counts.
4. Record the approved design principles and maintenance rules.
5. Verify all wikilinks resolve to existing notes.

### Task 6: Final live visual QA

**Objective:** Prove the deployed profile works as a public landing page.

**Steps:**
1. Open the public profile in a clean/logged-out view.
2. Capture a full-page screenshot in dark mode and inspect it with a vision model.
3. Check above-the-fold clarity, theme contrast, image loading, links, section length, and pins.
4. Repeat in light mode if the browser session permits.
5. Fix any visible defect, re-push if needed, and capture the final screenshot.
