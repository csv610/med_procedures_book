# Common Medical Procedures

An educational reference book covering common medical procedures, clinical interventions, and patient-facing procedure information.

The book is written in LaTeX and includes both the complete source and a compiled PDF.

## Contents

Each included chapter is designed to explain a procedure in clear clinical language, including relevant indications, preparation, performance, precautions, risks, recovery, results, and follow-up.

The active book intentionally excludes:

- Major operative surgeries
- Laboratory-test chapters

Some excluded source chapters remain in the chapters directory for archival and future editorial use, but they are not included in the active book compilation.

## Repository layout

~~~text
.
├── medical_procedures.tex   # Main LaTeX document
├── medical_procedures.pdf   # Compiled book
├── chapters/                # Procedure chapter sources
└── README.md               # Project documentation
~~~

## Building the book

Install a LaTeX distribution such as TeX Live or MiKTeX, then run:

~~~bash
pdflatex -interaction=nonstopmode -halt-on-error medical_procedures.tex
pdflatex -interaction=nonstopmode -halt-on-error medical_procedures.tex
~~~

The second pass updates cross-references and the table of contents. Build artifacts such as AUX, LOG, OUT, and TOC files are generated locally and are not part of the repository's maintained source.

## Editorial scope

This is an educational medical reference project, not a clinical practice manual. Procedure selection, preparation, contraindications, medication management, and follow-up can vary according to the patient, clinical setting, local protocols, and current professional guidance.

High-risk clinical statements should be reviewed against current guidance before publication or clinical use. In particular, readers should not independently stop anticoagulants, antiplatelet medicines, or other prescribed treatments based solely on this book.

## Contributions

Contributions should:

1. Preserve the existing LaTeX structure and terminology.
2. Use current, authoritative medical references.
3. Clearly distinguish patient education from clinician-directed decisions.
4. Avoid universal instructions where management depends on patient-specific factors.
5. Keep the active inclusion list consistent with the project scope.

Please run a clean two-pass LaTeX build before submitting changes.

## License

No open-source license has been assigned to this repository. All rights are reserved unless the repository owner specifies otherwise.
