# Core quality gates (existing upstream CI)

Home Assistant Core already supplies mandatory native workflows, integration tests, static analysis, security scanning, and generated Copilot instructions. This fork deliberately **does not** add a second simplified `quality` workflow: its existing checks must be the authoritative release and PR gates.

Agent requirements are appended to `AGENTS.md`; `.github/copilot-instructions.md` is regenerated from the canonical instructions and pull request template.

- Run the relevant integration unit tests and upstream lint/type/prek checks.
- Do not weaken or skip tests, hide errors, or alter thresholds to force a passing run.
- Follow the existing AI policy and contributor review requirements.
- Preserve upstream lockfiles and requirements.
- Require the existing CI check names in branch rulesets; do not configure a nonexistent `quality` job.

These rules do not claim a standalone numerical coverage target or guarantee complete test execution. Existing CI failures must be investigated and reported.
