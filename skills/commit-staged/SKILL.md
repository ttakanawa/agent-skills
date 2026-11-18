---
name: commit-staged
description: Create a commit from staged changes.
---

# Commit Staged

Create a commit from the currently staged changes.

## Message

- Follow the project's documented commit conventions and established history, including format and language. If no convention is established, use `<type>(<scope>): <summary>`.
- Default to a subject-only message; add a body when project conventions or necessary context call for one.
- Use the staged diff and conversation to understand what changed and why. Ask only when essential context is missing.

## Execution

- Inspect the staged diff; if nothing is staged, report it and stop. Leave unstaged changes untouched.
- Create the commit and return its hash and message.
