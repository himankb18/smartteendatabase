# AI-supported coding log

This log supports Section 9 of the ISOM3260 final report. Add screenshots of the
conversation and the affected notebook code before submission.

## 12 October 2026 — Progress demonstration notebook review

**AI tool:** OpenAI Codex

**Files supplied as context:**

- `Smart_Teen_Community_Progress_Demo.ipynb`
- `Smart_Teen_Community_Progress_Demo (1).ipynb`
- `ISOM3260 ProjectCase_Fall2026.pdf`
- `ISOM3260 ProjectGuideline_Fall2026.pdf`
- `DDL File Editor.ddl`
- `Smart Teen Community - Fixed.zip`

**Exact user prompts, in chronological order:**

1. `i am starting a projct isom3260. gonna give u all context`
2. `i gave it in the md fil`
3. `thios is remaining context and current state if u need. now check the colab file i attached earlier. lets edit code together`
4. When asked which edit to make next, the selected response was `Harden demo (Recommended)`.

**AI-supported changes:**

- Aligned the `GOAL`, `TRANSACTIONS`, and `POST` SQL with the current DDL by
  replacing the outdated foreign-key column names with `MEMBER_USERNAME` and
  `BANK_ANALYST_BA_USERNAME`.
- Added validation for the Oracle `VARCHAR2` size limits before insert and
  update statements execute.
- Set explicit monetary input limits and a two-decimal step matching
  `NUMBER(12,2)`. This also removes the widget's default maximum of 100.
- Added `show_demo_evidence()` to display committed M1–M5 and BA1 records
  without displaying passwords.
- Updated the demonstration checklist to explain how to prove the password
  change safely by logging in again.

**Verification performed:**

- The edited notebook parses as valid JSON.
- The combined Python code cells pass a Python syntax parse after excluding the
  Colab `!pip` command.
- A live Oracle test was not performed because it requires the group's course
  database credentials and access to `imz409.ust.hk` from Colab.

**Screenshots to add to the final report:**

- This conversation showing the prompts above.
- The corrected schema verification dictionary and SQL column names.
- The added validation code and `show_demo_evidence()` function.

