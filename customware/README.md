# customware/

This directory captures the fork-local patches that ride on top of
upstream. Each numbered entry has two files:

- `NNN-<slug>.md` — the plan, including any deviations noted under
  "Implementation notes" after the work shipped.
- `NNN-<slug>.patch` — `git diff upstream/main..HEAD --` at the time
  the entry was sealed, used as the primary rebase tool on the next
  upstream update.

Tag format on `main`: `v<upstream-version>-customware.<n>`.
Branches named `<upstream-version>` (no `customware` suffix) are
created at the start of an `/customware update` and preserve the
pre-update state.
