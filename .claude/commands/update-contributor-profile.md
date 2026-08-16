---
name: update-contributor-profile
description: Workflow command scaffold for update-contributor-profile in OSSPhilippines-first-contribution.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-contributor-profile

Use this workflow when working on **update-contributor-profile** in `OSSPhilippines-first-contribution`.

## Goal

Update or fix contributor profile information such as file extension or photo URLs.

## Common Files

- `contributors/*.json`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit the relevant contributor's JSON file in the contributors/ directory.
- Commit the changes with a descriptive message.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.