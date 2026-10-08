# AGENTS.md

Project-wide guidance for OpenAI Codex. Follow these rules when writing, reviewing, or refactoring code in this repository.

These guidelines favor caution over speed. For obvious one-line fixes, apply them proportionately.

## 1. Think Before Coding

- Understand the request and the relevant existing code before editing.
- State consequential assumptions. When ambiguity would change behavior or scope, ask rather than silently guessing.
- Identify meaningful tradeoffs and suggest a simpler approach when appropriate.
- Do not pretend to understand unfamiliar code or requirements.

## 2. Simplicity First

- Implement only the requested behavior.
- Prefer the smallest readable change; avoid speculative features, needless abstractions, and configuration without a concrete use case.
- Follow established project conventions rather than introducing a new pattern.
- Reconsider a solution if a much shorter, equally clear implementation is possible.

## 3. Surgical Changes

- Edit only files and lines needed for the task.
- Do not reformat, refactor, rename, or delete unrelated code and comments.
- Clean up imports, variables, or files made obsolete by your own changes.
- Mention pre-existing unrelated issues separately instead of modifying them.

## 4. Goal-Driven Execution

- Define observable success criteria before significant changes.
- For bug fixes, reproduce the failure with a test when practical; for new behavior, add or adjust focused tests.
- Run relevant tests, linters, or builds that are available.
- Review the final diff for unrelated changes and verify that it satisfies the success criteria.
- Report what was verified and clearly identify any checks you could not run.

For multi-step work, provide a brief plan with a verification point for each step. Avoid elaborate process for trivial edits.

## Project-specific instructions

Add repository-specific requirements below this heading as needed.
