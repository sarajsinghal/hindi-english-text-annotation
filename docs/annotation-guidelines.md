# Annotation Guidelines

These guidelines describe the starter label set. The workbook labels are synthetic and unverified; annotators must validate them against the source text.

## Unit of annotation

Annotate one message per row. Read the complete original `Text` before assigning labels. Preserve the original wording exactly in `Text`.

## Fields

| Field | Allowed values or rule |
|---|---|
| `Language` | `Hindi`, `English`, or `Hinglish`. Use Hinglish when Hindi and English are meaningfully mixed in one message. |
| `Code_Switching` | `Yes` when the message switches between Hindi and English; otherwise `No`. Follow the project’s language convention consistently for romanized Hindi. |
| `Sentiment` | `Positive`, `Negative`, or `Neutral`; label the message’s expressed tone, not the annotator’s reaction. |
| `Intent` | `Information Request`, `Complaint`, `Feedback`, `Request for Assistance`, `Appreciation`, or `General Conversation`. Choose the primary communicative purpose. |
| `Linguistic_Quality` | `Correct`, `Minor Error`, or `Major Error`. Assess language form, not whether the message is factually correct. |
| `Corrected_Text` | Provide one minimally edited, natural rewrite that preserves meaning. If the original needs no correction, copy it exactly. |
| `Error_Present` | Derived: `No` for `Correct`; `Yes` for either error level. |
| `Error_Severity` | Derived: `None` for `Correct`, `Minor` for `Minor Error`, and `Major` for `Major Error`. |
| `Error_Type` | Select the applicable category from the taxonomy below. Use a consistent delimiter if multiple categories are needed; do not invent new categories without recording a schema change. |
| `Annotation_Rationale` | Briefly explain the linguistic evidence for the quality and error labels. Avoid adding personal details not present in the text. |
| `Review_Status` | `Needs Human Review`, `Reviewed`, or `Adjudicated`. Set to `Reviewed` after an independent review; use `Adjudicated` only after disagreements are resolved. |
| `Reviewer_Notes` | Optional notes from a reviewer or adjudicator. |

## Error taxonomy

Use the workbook’s broad categories:

- Spelling / orthography
- Agreement
- Tense / auxiliary
- Case / preposition
- Syntax / word order
- Code-switching
- Register / politeness
- Punctuation
- Articles / countability
- Collocation / verb pattern

The label schema defines `Linguistic_Quality` (`Correct`, `Minor Error`, `Major Error`), but this field is missing from the `Noisy Dataset` header. Add it to a reviewed copy or explicitly approve a documented mapping before using the severity fields as a substitute. The starter workbook also contains free-text combinations in `Error_Type`. Normalize these values to the taxonomy before analysis. Keep the original workbook unchanged as a source snapshot; make normalization in a reviewed copy or a scripted transformation.

## Review workflow

1. Review each row independently without relying on the starter labels.
2. Compare the proposed labels with the allowed values and derived-field rules above.
3. Check that corrections preserve meaning and that correct rows copy `Text` exactly.
4. Record uncertainty in reviewer notes rather than guessing.
5. Have a second fluent reviewer resolve uncertain or conflicting rows.
6. Mark resolved rows `Adjudicated` and retain a brief rationale for material decisions.
7. Re-run completeness, allowed-value, and derived-label checks before publishing a reviewed release.

## Privacy

Use synthetic or properly de-identified text. Do not commit personal, confidential, or customer data to this public repository. Review workbook contents and metadata before each release.
