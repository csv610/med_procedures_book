---
name: medical-procedure-chapter
description: Create, review, or revise LaTeX chapters for this medical-procedures book, including source verification, plain-language editing, and book integration.
---

# Medical Procedure Chapter Skill

Use this skill for chapter-level writing, medical accuracy reviews, and requested edits in this repository. Follow the user's requested scope: a review should report findings; revise only when asked. Do not expand a narrow edit into a book-wide rewrite.

## Establish the project context

- Confirm the repository root contains `med_procedures.tex`; treat its `\input` list as the authority for which chapter files are in the active book.
- Read `README.md` and the relevant row in `SOURCE_MATRIX.md`. Inspect the target chapter and, when useful, one or two neighboring chapters for LaTeX conventions.
- Keep chapter titles short and precise. Preserve the book's established section structure where it fits; omit or adapt sections that do not apply instead of adding filler.
- Make patient-facing explanations understandable while retaining distinctions that affect diagnosis, safety, or treatment. Define necessary clinical terms briefly in context.

## Verify medical content

- Use current web sources for medical accuracy. Prefer a current government or established patient-information source for basic explanations and a relevant specialty society guideline or systematic review for clinical details. Use primary or authoritative sources for technical claims.
- Verify indications, preparation, procedural steps, contraindications, risks, expected results, follow-up, and warning signs that are relevant to the chapter. Check age-specific, pregnancy, medication, device, and emergency considerations when they affect the procedure.
- Treat recommendations as dependent on patient factors, clinical setting, and local protocols where appropriate. Do not turn a setting-specific guideline into a universal instruction. Do not advise readers to stop prescription medicines without a clinician-directed plan.
- Distinguish a test result or procedure finding from a diagnosis. Explain meaningful limitations, false-positive or false-negative results, and uncertainty when relevant.
- Never invent citations or imply a clinician has reviewed a chapter. Add complete references with organization or author, title, publication/update date when available, direct URL, and access date. Use `\url{...}` as in other chapter files.
- When sources are incomplete or conflicting, state the limitation and avoid overconfident wording. Do not leave unsupported specific numbers, timelines, or absolute claims in the chapter.

## Edit and integrate a chapter

- Match the existing LaTeX conventions and keep the prose concise. Explain what the patient may experience as well as what the clinician does when that distinction helps readers understand the procedure.
- Tailor precautions, aftercare, and “When to Seek Medical Care” to the specific procedure. Remove generic warning lists that do not apply; do not present emergency symptoms as routine effects of a procedure.
- If an illustration is requested, ensure it depicts the procedure and patient positioning accurately, follows project image conventions, and has a useful caption and source or license attribution. Do not substitute a decorative image for an explanatory one.
- After substantive edits, update the chapter's `SOURCE_MATRIX.md` row to reflect the actual sources and verification status; do not mark clinician review complete unless it occurred.
- When the user asks to add or fix chapter content in the book, update the active source file and rebuild the maintained PDF as appropriate. The README's main source is `med_procedures.tex`; the maintained PDF is named `medical_procedures.pdf`. Build with `pdflatex -jobname=medical_procedures -interaction=nonstopmode -halt-on-error med_procedures.tex` twice. Report build errors or material warnings accurately.
- Keep changes within the requested chapter and necessary book artifacts. Preserve unrelated existing working-tree changes.
