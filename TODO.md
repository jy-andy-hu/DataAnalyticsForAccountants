# TODO

Items are ordered in the sequence they are likely to be tackled.

## 1. Refine the AI courses (drafts, debate with Claude)
- [ ] Review and refine each AI course page in `chapters/AI-*.qmd` (descriptions, lengths, takeaways, case studies).
- [ ] Fact-check before delivery:
  - Ethics: AICPA and IESBA references, and CPE-credit eligibility (marked "to be confirmed" on the page).
  - AI with Power BI: Power BI MCP servers are in public preview and change often. Re-verify capabilities and setup.
- [ ] Write the "Before We Start" guides (only a placeholder exists for AI Foundations).
- [ ] Flesh out `chapters/AnalyticsStrategy-Leaders.qmd` (length and real outline) and `chapters/AI-Leaders.qmd`.
- [ ] Decide whether the AI bootcamp's hours breakdown (24h) still works after the course pages settle.

## 2. Fix existing issues in the site
- [ ] "GAAP for Data Visualization": its "Before We Start" sidebar link points to the R course page. Either create a GAAP before-we-start page or remove the link.
- [ ] Decide whether `Setup-vscode.qmd` and `InfusePythontoAccounting-before-we-start(AnacondaDistribution).qmd` should be published. They are not in the `render:` list in `_quarto.yml`.
- [ ] `.gitignore` excludes `images/`, but the site uses images from it. Check what you intend.
- [ ] Review the Preface (`preface.qmd`) wording now that the catalog is the home page.

## 3. When each AI course goes live
- [ ] Remove `draft: true` from the course page.
- [ ] Remove its `*(coming soon)*` label wherever it appears: `ai.qmd`, `python.qmd`, `r.qmd`, `powerbi.qmd`, `excel.qmd`, `analytics.qmd`, and `AnalyticsStrategy-Leaders.qmd`. (Draft pages show as plain text in the published build, so links start working only after `draft: true` is removed.)
- [ ] Update `ai.qmd` subtitle ("Courses are coming soon").
- [ ] When Analytics Strategy for Finance Leaders is finished, remove its "Coming Soon" banner and update its description.

## 4. Before committing and publishing
- [ ] Review the git state. Nearly every file showed as modified before the AI work started (probably line endings or file modes). Run `git diff --stat` and decide what to commit.
- [ ] Re-render the site (`quarto render`) and check the catalog, navbar, sidebars and all arena pages in a browser.
- [ ] Commit and push, and confirm GitHub Pages serves the `docs/` folder.

## 5. Rename the GitHub repo and URL (after the content is published)
- [ ] Rename the GitHub repo and update the site URL to match the new site name, "The Modern Accountant's Lab".
  - Current repo/URL: `DataAnalyticsForAccountants` -> https://jy-andy-hu.github.io/DataAnalyticsForAccountants/
  - Rename on GitHub (Settings > General), then update the local git remote and any shared links. GitHub redirects the repo, but GitHub Pages URLs do not redirect.
- [ ] Update `Readme.md` (title is still "Elevate Accounting with Analytics", and it holds the old URL).
- [ ] Update the "Context for claude.txt" note if the pitch or positioning changed.

## 6. Ideas for later
- [ ] Function-specific AI labs: AI for FP&A, Audit and Assurance, Tax, Controllership and Close.
- [ ] More sessions for the Excel arena.
- [ ] Show course length on the catalog cards (needs a custom card template).
- [ ] A distinct accent color for each arena in `custom.scss`.
