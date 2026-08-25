# Repository Guide

## Scope

- This is a Power BI portfolio, not a software package. There are no build, lint, test, typecheck, CI, or code-generation commands.
- All portfolio content is under `POWERBI/`. Keep `POWERBI/README.md` as the general index of every dashboard.
- The current projects are `01_Employee_Analytics`, `02_Financial_Performance_Analytics`, and `03_Global_Population_Health_Analytics`.

## Project Structure

- Name project directories `XX_Project_Name`, using a two-digit sequence, descriptive English words, and underscores as separators.
- Every project must remain self-contained with exactly one report `.pbix`, `README.md`, `data/`, and `images/` at its top level. Keep this layout consistent across projects.
- Use descriptive English names and underscores instead of spaces for new project and documentation asset names. Preserve existing data-source filenames unless the report connections can also be updated.
- When adding, removing, or renaming a project, update the project list and relative links in `POWERBI/README.md` in the same change.
- Keep each report with its adjacent `data/` files. Renaming or moving workbooks can break Power Query file sources and requires updating the report connections and refreshing the model.
- Financial analytics uses `Finanzas.xlsx`, `Categorias.xlsx`, and the year-specific files under `data/Calendarios/`; global health uses five separate workbooks. Do not collapse these into the single filenames shown in README structure examples.

## PBIX Files

- Do not modify, delete, rename, extract, or repack `.pbix` files. Treat them as immutable binary source artifacts.

## Project READMEs

- Before editing a project README, review the other project READMEs and preserve their shared Markdown format and style.
- Use these sections in this order: project title, `Dashboard Preview`, `Live Dashboard`, `Project Overview`, `Dashboard Features`, `Report Pages` when applicable, `Technologies`, and `Project Structure`.
- Use consistent Markdown headings, list markers, spacing, and link formatting across all project READMEs.
- Embed existing screenshots from the project's `images/` directory with relative paths. Do not link to invented or missing image names.
- Describe only dashboard pages, datasets, DAX measures, visuals, and behavior that can be verified from repository artifacts. Do not infer or invent features.

## Documentation Gotchas

- Trust filesystem names over README project-tree examples. Several examples are stale: the portfolio README still links to nonexistent sales/third-project directories, and project READMEs contain outdated report, data, directory, or screenshot names.
- Match path case exactly. In particular, the employee report is `Employee_analytics.pbix`; financial screenshots include the existing misspelled names `financial-comparasion.png` and `balance-analysis.com.png`.
- When report pages or visuals change, update the corresponding project README screenshots and feature/page descriptions; do not assume the published Power BI link changed unless a new link is provided.

## Verification

- There is no automated verification. For workbook changes, open the report in Power BI Desktop without saving over the `.pbix`, refresh all data, check for query/model errors, and exercise affected pages, slicers, and visuals.
- For documentation-only changes, verify every relative link and image path against the actual case-sensitive repository path.
- Keep changes within the requested scope; do not reformat, rename, or clean up unrelated files.
