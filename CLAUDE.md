# CLAUDE.md

Guidance for Claude Code (and other AI assistants) working in this repository.

## What this repository is

This is **not a software codebase**. It is Frontier Climate's public archive of
source materials for its carbon dioxide removal (CDR) advance market commitment
purchases — RFPs, project applications, reviewer forms, purchase agreements, and
supporting guidance documents. There is no source code, no build system, no
tests, and no CI/CD. The repository exists purely to publish documents under a
Creative Commons CC0 license for transparency in the CDR field.

Prior purchasing-cycle materials from Stripe Climate (the predecessor program)
live in a separate repo: https://github.com/stripe/carbon-removal-source-materials

Because there is no code, most of the usual "development workflow" guidance
(build/lint/test commands, coding conventions, architecture) does not apply.
Treat tasks here as **document/file organization and content lookup tasks**,
not programming tasks.

## Repository structure

```
/
├── Call for Proposals/          RFP documents (PDF), by cycle
├── Project Applications/        Applications submitted by CDR project teams, by cycle
│   ├── 2022 Fall/
│   ├── 2022 Spring/
│   ├── 2023 Summer/
│   ├── 2024 Summer/
│   ├── 2025 Summer/
│   └── 2025 Fall/
├── Purchase Agreements/         Executed contracts (purchase agreements, R&D grants), by cycle
│   ├── 2022 Fall/
│   ├── 2022 Spring/
│   ├── 2023 Summer/
│   ├── 2024 Summer/
│   └── 2025 Summer/, 2025 Fall/
├── Purchasing Resources/        Standing guidance docs (M&V Q&A, pricing guidelines,
│                                 energy-accounting guidelines, sample TEA/emissions calcs)
├── TEMPLATE Project Application/  Blank application templates + modular technology
│                                 supplements (DAC, mineralization, biomass, oceans,
│                                 geologic injection, CO2 utilization), by cycle
├── TEMPLATE Purchase Agreements/  Blank purchase agreement templates, by cycle
├── TEMPLATE Review Forms/         Blank scientific & governance reviewer forms, by cycle
├── README.md                    Top-level orientation and links
├── CONTRIBUTING.md              States the repo does NOT accept external GitHub contributions
└── LICENSE                      CC0 1.0 Universal (public domain dedication)
```

Nearly all content is **PDF** (contracts, applications, guides) with a handful of
**XLSX** files (techno-economic analysis templates, sample emissions calculations).
There are no other file types of substance in the repo.

## Naming and organizational conventions

- **Cycles are named `<Year> <Season>`** (e.g. `2023 Summer`, `2025 Fall`) and used
  consistently as subfolder names under `Project Applications/`, `Purchase Agreements/`,
  and `TEMPLATE Review Forms/`. `TEMPLATE Project Application/` instead uses
  `YYYY_MM (season)` folder names (e.g. `2024_06 (summer)`).
- **Project application filenames** follow `[Company Name] Frontier Carbon Removal
  Purchase Application.pdf` (older cycles) or `[Company Name] Prepurchase Application
  YYYY.pdf` (2025+ cycles). The bracketed company name is the canonical identifier
  for a submission — use it to cross-reference a company's application against its
  purchase agreement in the corresponding cycle folder.
- **Purchase agreement filenames** are typically `<Company> Purchase Agreement.pdf`,
  `[<Company>] Frontier Prepurchase Agreement.pdf`, or `<Company> R&D Grant.pdf` /
  `Frontier R&D Agreement.pdf` for research-and-development-only deals (as opposed to
  binding CDR purchases).
- Company name spelling/casing sometimes drifts slightly between the application
  filename and the agreement filename for the same company/cycle (e.g. capitalization,
  "and" vs "&"). When matching a company across folders, compare loosely rather than
  assuming exact string equality.
- Not every applicant in a cycle has a corresponding purchase agreement — most
  applicants are not selected for purchase, so `Purchase Agreements/<cycle>/` is
  always a small subset of `Project Applications/<cycle>/`.

## Working in this repo

- **Adding new cycle materials**: create a new `<Year> <Season>` folder under the
  relevant top-level directory (mirroring the existing pattern) rather than dumping
  files into an existing cycle folder or the repo root.
- **Templates vs. actuals**: never edit files under `TEMPLATE *` directories to
  reflect a specific company/cycle — templates are the blank forms that get copied
  and filled in externally, then the completed file is added under
  `Project Applications/`, `Purchase Agreements/`, etc. Add a new dated subfolder to
  the relevant `TEMPLATE` directory only when a new template version is released for
  a cycle.
- **License**: all content here is released under CC0 1.0 (public domain
  dedication), per `LICENSE`. Assume any new file added to the repo is intended to be
  released under the same terms.
- **No external contributions**: per `CONTRIBUTING.md`, this repo does not accept
  outside pull requests. Do not open PRs from outside contributors' forks or imply
  this is a community-contribution project. Direct people with supplier/buyer/reviewer
  interest to the emails listed in `CONTRIBUTING.md` (suppliers@, buyers@,
  info@frontierclimate.com) instead of a GitHub workflow.
- **Editing PDFs/XLSX**: these are binary documents, typically finalized/signed
  contracts or published guides. Don't attempt to "fix" content inside a PDF unless
  explicitly asked — most are legal or point-in-time records and should be treated
  as authoritative as committed. If asked to extract, summarize, or search within
  them, read the file directly (PDF/XLSX tooling) rather than guessing content from
  filenames.
- **No build/lint/test commands exist** for this repository — do not invent or run
  any (e.g. there is no `package.json`, `Makefile`, or CI config to discover).

## Useful entry points

- `README.md` — top-level description and links to CarbonPlan's markdown mirror of
  the application template.
- `Purchasing Resources/` — the best starting point for understanding Frontier's
  substantive evaluation criteria (M&V, out-of-scope approaches, pricing guidelines,
  energy accounting).
- `TEMPLATE Project Application/` — shows what information Frontier collects from
  applicants and how the ask has evolved cycle over cycle.
