# Test repo A — Harbor Café

A small, self-contained café website with clear visual changes and deliberately unchanged screenshot pairs.

**Expected compatibility result: Accept · 10 versions available.**

- Default-branch commits: **10**.
- Commit numbers below are **oldest first**, starting at 1.
- This is a synthetic Git Gallery fixture, not an organic production history.
- Expected outcomes below describe the application requirements, not a claim that Git Gallery integration tests have passed.

## Pages at the latest commit

`index.html`

## Test cases and expected results

### All versions selected

**Target page:** `index.html`  
**Commit numbers:** 1, 2, 3, 4, 5, 6, 7, 8, 9, 10.

Compatibility passes. All 10 commits are initially selected. Capturing them produces Complete status and 10 timeline entries in oldest-to-newest order.

### Visible evolution

**Target page:** `index.html`  
**Commit numbers:** 1, 10.

Both captures succeed. The comparison shows the added brand styling, menu, illustration, visit details, seasonal section, and final accent treatment.

### Documentation-only change

**Target page:** `index.html`  
**Commit numbers:** 6, 7.

The screenshots show no visible difference. Commit 7 changes documentation, not the website. AI should explicitly report no visual change.

### Code cleanup without visual change

**Target page:** `index.html`  
**Commit numbers:** 8, 9.

The screenshots are visually identical. The CSS comment added at commit 9 must not be described as a visible redesign.

## Important fixture rules

- The homepage exists in every commit.
- Use a fixed viewport and fresh initial page state for comparison.
- This is a synthetic fixture, not a real café or organic development history.

## Local preview

Serve this directory with `python3 -m http.server 8000`, then open http://localhost:8000. The site uses only local HTML, CSS, JavaScript, and original SVG assets. No build step, API, external font, account, or secret is needed.

## Preserve the test

Do not append setup or documentation commits casually: the default-branch count is part of this test. Count with `git rev-list --count main`. List the history oldest first with `git log --reverse --format="%h %s" main`.

The README contains test guidance and expected answers. AI evaluation using this repo is therefore not a blind benchmark; judge visual claims against screenshots and website changes, not this document alone.
