# Test repo A — Harbor Café

A small, self-contained café website with clear visual changes and deliberately unchanged screenshot pairs.

**Expected result: Accept · 10 versions available.**

Exactly **10 commits** on main. Commit numbers are oldest first.
Synthetic history for Git Gallery testing; all content is fictional.

## Scenarios

### All versions selected

Page: `index.html`. Versions: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10.

Compatibility passes. All 10 commits are initially selected. Capturing them produces Complete status and 10 timeline entries in oldest-to-newest order.

### Visible evolution

Page: `index.html`. Versions: 1, 10.

Both captures succeed. The comparison shows the added brand styling, menu, illustration, visit details, seasonal section, and final accent treatment.

### Documentation-only change

Page: `index.html`. Versions: 6, 7.

The screenshots show no visible difference. Commit 7 changes documentation, not the website. AI should explicitly report no visual change.

### Code cleanup without visual change

Page: `index.html`. Versions: 8, 9.

The screenshots are visually identical. The CSS comment added at commit 9 must not be described as a visible redesign.

## Fixture rules

- The homepage exists in every commit.
- Use a fixed viewport and fresh initial page state for comparison.
- This is a synthetic fixture, not a real café or organic development history.
- Every historical page fits the current passive HTML/CSS/PNG profile. Large visual redesigns are intentional synthetic test data; only the documented identical pairs should stay unchanged.

## Preview

Run `python3 -m http.server 8000` and open http://127.0.0.1:8000/index.html.
Only native HTML, flat CSS, system fonts, and local PNG artwork are used. No install, build step, script, external service, or backend is required.

Do not append commits: counts are part of the fixtures. The 2026-11-10 refresh intentionally replaced historical SHAs; refresh previously cached Git Gallery selections.
Queue completion, partial completion, and timeline behavior are acceptance expectations; local fixture verification alone is not a live database/worker test.
README text supplies expected answers; use screenshots and source diffs when judging AI claims.
