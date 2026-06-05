# Claude.md — Agent Instructions

## Brand Guidelines
All outputs (HTML, slides, documents, PDFs, reports, or any publication) **must** follow the Rithim corporate brand guidelines defined in [`brandguidelines.md`](brandguidelines.md). Key rules:
- Use **light theme** for all reports and PDFs.
- Use **dark theme** for on-screen/digital only.
- Never modify the logo.
- Date format: `DD Month YYYY`.
- Data viz and RAG colors are reserved for their specific uses only.

## Visual Output Skill
For any visual design output (posters, banners, graphics, artwork, `.png`, `.pdf` design assets) — use the **`canvas-design` skill**:
- Invoke with `/canvas-design <prompt>`
- Apply Rithim brand colors and identity in all canvas outputs.
- Use `/docx` for Word docs, `/pptx` for slides, `/pdf` for PDF reports, `/xlsx` for spreadsheets.

---

## Role & Approach
- **Purpose:** Separate reasoning (AI) from execution (tools).
- **Principle:** AI orchestrates workflows; tools perform execution.
- **Benefit:** Reliability, accuracy, and reproducibility.

### How to operate:
1. Read the workflow SOP.
2. Identify required tools.
3. Run tools in the correct sequence.
4. Handle errors using the checklist.
5. Document changes and edge cases.

---

## Workflow Template
Each workflow in `workflows/` must follow this structure:

```markdown
# Workflow Title

## Objective
- Clear statement of purpose.

## Required Inputs
- List of inputs (parameters, files, credentials).

## Tools to Use
- Which scripts or APIs are required.

## Expected Outputs
- Format and destination of results.

## Edge Cases & Recovery
- Common failure modes and how to handle them.
```

---

## Tooling Standards
- Naming convention: `verb_task.py` (e.g., `scrape_site.py`).
- Entrypoint: Each tool must have a `main()` function.
  - Purpose: predictable entry point, safe imports, easier testing.
- Testing: Each tool must have a corresponding test file in `tests/`.
- Documentation: Add a docstring explaining purpose, inputs, and outputs.

---

## Error Handling Checklist
1. Read the error message — capture the full trace.
2. Identify the cause — syntax, API issue, environment, or logic error.
3. Fix the tool — apply the correction.
4. Retest — confirm the fix works.
5. Document — update the workflow with the new approach.
6. Escalate if needed — check before retrying sensitive or paid API calls.

---

## Git Collaboration Guidelines
- Branching:
  - `feature/` for new tools or workflows.
  - `fix/` for bug fixes.
  - `docs/` for documentation changes.
- Commit messages: `type(scope): short description`.
- Pull requests: Always open a PR before merging.
- Versioning: Tag stable releases (e.g., `v1.0.0`).

---

## Security Checklist
- Secret storage: All credentials in `.env` or `credentials.json` (gitignored).
- Access restriction: Limit file permissions; never expose via HTTP.
- Secret rotation: Every 90 days or per provider policy.
- Audit logs: Document updates to keys.
- Compliance: Follow provider rules (Google OAuth, AWS IAM, etc.).
- Note: `.env` is standard and safe if properly restricted. Production should use environment injection or secret managers.

---

## Scope Boundaries
This project is sandboxed. Stay within:

```
C:\Users\Kenneth Hee\AI-Projects\
```

### Allowed directories:
- `C:\Users\Kenneth Hee\AI-Projects\data\obsidian\vaults\Signal-Zero\`
- `C:\Users\Kenneth Hee\AI-Projects\n8n-workflows\`
- `C:\Users\Kenneth Hee\AI-Projects\apps\sandbox\www\`

Do not read or write outside this root unless explicitly permitted.

### Sandbox Diagram:
```
C:\Users\Kenneth Hee\AI-Projects\
├── tools\                ✅ Allowed
├── workflows\            ✅ Allowed
├── .tmp\                 ✅ Allowed
├── data\obsidian\vaults\Signal-Zero\   ✅ Allowed
├── n8n-workflows\        ✅ Allowed
├── apps\sandbox\www\     ✅ Allowed
└── system\               ❌ Restricted
└── other directories     ❌ Restricted
```
