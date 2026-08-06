# GitHub Profile Editorial Redesign

**Date:** 2026-08-07
**Status:** Approved
**Direction:** Editorial proof-first

## Objective

Make Umer Farooq's GitHub profile communicate, within five seconds, that he is an experienced independent AI consultant and full-stack engineer who delivers production systems—not a generalist listing technologies.

## Evidence and constraints

The design uses only claims verified from Umer's current website, GitHub account, LinkedIn URL, and existing professional records:

- $1M+ value delivered
- $37K+ enterprise engagement
- 500K+ documents made searchable
- IEEE-published biometric-security research using 80,000 frames
- Founder of Zenovae
- Work across document automation, source-backed knowledge systems, controlled AI workflows, Voice AI, and full-stack delivery

The profile must render cleanly in GitHub light and dark themes, avoid fragile third-party widgets, and link proof claims to the relevant case study or publication.

## Research conclusions

GitHub supports a profile README in the public `username/username` repository, up to six pinned repositories or gists, social links, status, location/timezone, achievements, and contribution visibility.

GitHub community discussions consistently favor original repositories, concise explanations, and proof of work over long widget dashboards. Polished presentation helps signal attention to detail, but stats cards and contribution scores are easy to game, often clutter profiles, and can fail when external image services are unavailable.

## Visual direction

- Match the warm, restrained editorial character of `umerfarooq.me`.
- Use a repository-owned, theme-aware SVG hero instead of an animated third-party typing image.
- Light hero: warm off-white, near-black typography, restrained red accent.
- Dark hero: warm near-black, off-white typography, restrained terracotta accent.
- Use large type, thin rules, generous whitespace, and no literal diagrams or icon collage.
- Keep GitHub's native typography for body content and use the custom SVG only for the branded hero.

## Information architecture

1. Theme-aware hero with name, role, positioning, and links
2. Four verified impact metrics
3. Short “What I build” statement
4. Three linked selected-work case studies
5. Compact capability list
6. Published research with direct IEEE and summary links
7. One contact call to action

## Profile metadata

- Normalize display name to `Umer Farooq`.
- Replace the keyword-dump bio with a specific production-AI positioning statement.
- Preserve website and LinkedIn links.
- Remove forked and unrepresentative pinned repositories.
- Pin only original, current work; start with `openclaw-security-fix-cli` until stronger public repositories such as shipkit are ready.

## Removed elements

- Typing animation
- Visitor counters
- GitHub stats, streak, trophy, and top-language cards
- Duplicate contact rows
- Large technology badge wall
- Unlinked or unverifiable project claims

## Acceptance criteria

- Hero is readable in both GitHub themes.
- No externally hosted dynamic stats or typing services remain.
- Every case study and research link resolves successfully.
- README is materially shorter and scannable.
- Public bio matches the current AI-consulting identity.
- Pinned section contains no forks.
- Final live profile is visually inspected from a full-page screenshot.
