# IIT Madras BS/BSc Data Science CGPA Calculator

A free, single-file, browser-based CGPA calculator for students of the **IIT Madras BS in Data Science and Applications** program. Pick a grade for each course and it instantly computes your CGPA at every level, plus flags whether you meet the eligibility rules to progress to the next level.

> **Disclaimer:** This is an unofficial, community-built tool and is not affiliated with or endorsed by IIT Madras. Course lists, credits, grading rules, and eligibility criteria may change without notice — always verify against official IIT Madras communications before relying on this calculator for academic decisions.

## Features

- **Level-wise CGPA** for Foundation (32 credits), Diploma in Programming (27 credits), Diploma in Data Science (27 credits), and BSc Degree (28 credits: 20 core/mandatory + 8 elective)
- **Overall CGPA** and percentage (CGPA × 10) across all levels
- **Full Degree-level elective catalog** (Data Science, CS & Programming, Science & Engineering, Humanities & Management, and more) with a dynamic add/remove picker, including the newly added 2-credit Comprehensive Exam electives
- **Degree Level Entry Checkpoint** — checks the two conditions required to progress from Diploma to Degree level (combined Foundation + Diploma CGPA ≥ 6.0, and Diploma Projects CGPA ≥ 7.0), including a course-completion tracker so it won't show "eligible" on partial grades alone
- **PG Diploma / M.Tech Upgrade Checkpoint** — tracks the credit window (106–142 credits) and CGPA cutoff (≥ 8.00) for upgrading to a PG Diploma or M.Tech after the BS
- **Grading system reference table** (S–U, absolute grading, pass cutoffs)
- **Auto-save** — grades and elective selections persist in the browser's `localStorage`, so a page refresh won't clear your progress
- No build step, no dependencies, no server — just open `index.html`

## Usage

Open [index.html](index.html) directly in a browser, or serve it with any static file server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

Select a grade for each course across the Foundation, Diploma - Prog, Diploma - DS, and Degree tabs. All CGPA figures and eligibility checkpoints update live. Use **Reset All** to clear every grade and start over.

## Project files

| File | Purpose |
|---|---|
| `index.html` | The entire application — markup, styles, and logic in one file |
| `DS Course Booklet.pdf` | Official IIT Madras course booklet used as the source of truth for course names, codes, and credits |
| `og-banner.png` | Social-preview image used in the page's Open Graph / Twitter Card metadata |

## Source of truth

Course structure, credits, and grading rules are sourced from IIT Madras's official DS Course Booklet and published program handbook. If a rule changes (a course is added/removed, a credit value changes, or an eligibility threshold is updated), verify against the current official documentation and update `index.html` accordingly.
