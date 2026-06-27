---
name: resume
description: Resumes work from a saved SESSION_STATE.md record. Use when picking up where a previous session left off.
argument-hint: "[state-path]"
---

# Resume

Resume work from a saved session record.

Read SESSION_STATE.md from the working directory, or the path given as $ARGUMENTS[0]. If no record exists, say so and stop.

On resume:

- Run cheap, read-only checks to confirm the recorded state still holds before changing anything. Do not act on the record's claims without verifying them against the actual files.
- Treat only genuinely derived state as disposable: build output and other artifacts that regenerate from tracked source. When that state is corrupted, discard and regenerate it rather than repairing it in place. Working-tree edits are not derived state; do not discard them to clear corrupted derived state.

Then report where things stand (done, next, blocked) and any open questions, and continue from there.
