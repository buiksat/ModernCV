# Apple evaluation CV notes

## Sources

- Factual base: `behzadian_cv_rs.tex` and `behzadian_cv_rs.pdf`.
- Production-work presentation: `behzadian_cv_re.tex` and `behzadian_cv_re.pdf`.
- Cross-check: `behzadian_cv.tex` and `behzadian_cv.pdf`.
- Repository revision: `9ff5f551e39394b8656e95d8f3e143c4ca40993d` on `main`.
- Existing Apple-specific files were absent before this work.

## Apple roles and retrieval status

- AIML - Sr Machine Learning Engineer, Evaluation, role `200668113`: https://jobs.apple.com/en-us/details/200668113/aiml-sr-machine-learning-engineer-evaluation
- AIML - Sr Data Scientist, Evaluation, role `200631850-0836`: https://jobs.apple.com/en-us/details/200631850-0836/aiml-sr-data-scientist-evaluation

Both official U.S. pages returned HTTP 200 on 2026-09-21. The complete posting text was available in the official pages' embedded hydration data, so no substitute posting or summary-only fallback was needed. The role numbers and titles above match that data.

## Main changes

- Created one evaluation-focused CV for both roles, with production systems and Python/PyTorch visible for the preferred MLE role.
- Updated the profile to surface the Ph.D. while keeping the balanced research-and-production positioning.
- Consolidated the Meta evidence into two distinct bullets covering production correctness and auditing, statistical diagnosis, and safeguards.
- Kept UPI-TRM's workshop designation and described its finite-depth guarantees as assumption-dependent.
- Reorganized supported skills into programming, evaluation and experimentation, research, and post-training. Retained the `working knowledge` qualifier.
- Made page 1 a complete overview with Technical Skills, and placed all five publication entries together on page 2.
- Preserved employers, titles, dates, education, publication metadata, authorship order, links, and immigration wording.

## Requirement-to-evidence mapping

| Apple requirement or scope | Repository evidence | Assessment |
| --- | --- | --- |
| Evaluation methods, experimentation, statistical analysis, and data quality | Meta experiment-metric correctness, statistical diagnostics, anomaly and data-quality monitoring, and ML auditing | Direct experience |
| Production evaluation infrastructure | Production systems for measurement correctness, monitoring, auditing, and safeguards | Direct experience in experimentation systems; transferable to model evaluation |
| Python and PyTorch | Technical-skills sections in the reviewed CVs | Direct experience |
| Automated evaluators, reward models, and post-training feedback | Research on truncated evaluators and verifier-style rewards; working knowledge of reward modeling and post-training algorithms | Transferable research knowledge, not production foundation-model experience |
| Foundation-model and agent evaluation, prompt/context optimization, simulations, and trajectory generation | No supporting repository evidence | Unsupported |
| Distributed systems and production ML training infrastructure | No specific distributed-systems or training-infrastructure evidence | Unsupported |
| Eight or more years of professional software-engineering experience | Employment history does not establish this | Unsupported |
| SQL, Spark, or equivalent data-querying systems | No supporting repository evidence | Unsupported |
| Human-annotation accuracy and variability | No supporting repository evidence | Unsupported |

## Highest-value question

What concrete Meta project can you describe, including your contribution, one relevant technical decision, and a defensible outcome that is safe to disclose?

## Build and checks

- Build command: `mkdir -p build/apple && latexmk -pdf -interaction=nonstopmode -halt-on-error -outdir=build/apple behzadian_cv_apple.tex && cp build/apple/behzadian_cv_apple.pdf .`
- Final PDF: `behzadian_cv_apple.pdf`, 2 letter-size pages.
- The final pdfLaTeX log contains no errors, missing-character warnings, overfull or underfull boxes, unresolved references, or package warnings.
- Both pages were rendered to PNG at 160 DPI and inspected for clipping, overlap, spacing, section transitions, publication splits, and page balance.
- Page 1 ends with Technical Skills; page 2 begins with one Selected Publications heading and contains all five publication entries before Education and Honors.
- `pdftotext` confirmed the contact information, section order, complete content, reading order, and extraction of the \(L_\infty\) notation.
- `pdffonts` confirmed that every font is embedded, subsetted, and Unicode mapped.
- `pdfinfo -url` confirmed the email, website, LinkedIn, Google Scholar, OpenReview, and publication link annotations.
- The staged build PDF and root deliverable had identical SHA-256 hashes after the final build.
