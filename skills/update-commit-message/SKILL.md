---
name: update-commit-message
description: Update an existing commit message.
argument-hint: <commit-hash>
---

# Update Commit Message

Update the specified commit's message using the bundled helper.

## Message

- Follow the project's documented commit conventions and established history, including format and language. If no convention is established, use `<type>(<scope>): <summary>`.
- Default to a subject-only message; add a body when project conventions or necessary context call for one.
- Use the commit's diff and conversation to understand what changed and why. Ask only when essential context is missing.

## Execution

- Inspect the target commit and its current message; if it does not exist, report it and stop.
- Present the proposed message and wait for explicit approval before rewriting history.
- Run [git-reword.sh](scripts/git-reword.sh) with the target commit hash and approved message as two arguments. Resolve the script path relative to this skill directory.
- Verify the updated target commit and return its new hash and message. Rewriting an older commit also changes descendant hashes.
