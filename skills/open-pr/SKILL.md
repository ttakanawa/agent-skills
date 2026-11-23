---
name: open-pr
description: Create a GitHub PR or GitLab MR from the current branch, following project conventions.
---

# Open PR

Create a GitHub PR or GitLab MR using the appropriate tools for the repository's hosting platform.

## Content

- Build the title and body from the branch's commits and diff, following the project's language and conventions.
- Follow the repository's PR/MR template when available; otherwise write a concise description suited to the change.
- For material design choices, summarize the viable alternatives considered, including the existing approach when viable. Explain the concrete trade-offs and why the chosen approach fits the request. If only one option is viable, state the constraint. Call out any new dependencies, permissions, setup, or ongoing maintenance the reviewer would inherit.
- Use Mermaid diagrams proactively when they help reviewers understand the change's structure, relationships, or flow.
- Include actual verification results and mark checklist items complete only when verified.
- Do not add a generated-by footer.

## Review and Execution

- Before pushing or creating, inspect CI configuration and project scripts and run the applicable tests and checks locally. If any required check fails or cannot be run, report the blocker and stop. This applies even when confirmation is skipped.
- Normally, present the complete title, body, target branch, and draft status together for approval before pushing and creating.
- If the user explicitly asks to skip confirmation, or has already approved pushing and creation in the conversation, proceed without another approval.
- Ask additional questions only when essential information is missing.
- Push the branch, create the PR/MR, and return its URL.

## Defaults

Unless the user specifies otherwise:

- Follow the project's target branch convention; use the repository's default branch only if none is defined.
- Create as ready for review only when the change is ready to merge; otherwise create as draft.
- Assign to the current user (`@me`).
- Enable source branch deletion on merge; repository-wide setting changes require explicit authorization.
- Follow the project's squash policy.
