# Spec: personal auto policy admin, mid-term changes

The reference spec for Builder Mode Messenger's first test case. It is synthetic: written from public sources, each listed in `../sources.md`.

## How to read this folder

- `context.md`: who uses the system, what it touches and what it connects to.
- `milestones.yaml`: the two milestones and the requirements in each.
- `R-001.md` to `R-022.md`: one requirement per file. The block at the top of each file (between the `---` lines) gives its ID, title, owner, status, milestone, scope, sources and the fields its examples use.
- `data/`: synthetic policies the examples and scenarios refer to.

## Worked examples are the acceptance tests

- **Calculation examples** are tables. Columns whose heading starts with "→" are the expected results; the others are inputs. Text must match exactly; money matches to the cent unless the field says otherwise.
- **Workflow scenarios** are step tables: who does what, and what they should see.

## Conventions used throughout

- Dates are written year-month-day (2027-03-03). A policy change, cancellation or reinstatement takes effect at 12:01 a.m. on its effective date.
- The sample term runs from 2026-12-01 to 2027-06-01: 182 days.
- "Full-term premium" is what the rating engine charges for the whole term. This slice never calculates it; it only prorates it.
- Money is rounded to the cent; exactly half a cent rounds away from zero (R-004).
