# Dataset Card

## Summary

The starter workbook contains 134 records of short Hindi, English, and Hinglish messages with language-quality, sentiment, intent, and code-switching annotations.

## Status and intended use

The workbook identifies the examples as synthetic starter annotations. Every row is marked `Needs Human Review`. The labels are not validated ground truth and should not be used to claim model quality, benchmark results, or annotator agreement.

It is intended to help define the schema and support a human annotation workflow. After independent review and adjudication, a separate version may be considered for research or evaluation, with its provenance and limitations documented.

## Contents

The workbook has six sheets: `QA Summary`, `Sheet1`, `Noisy Dataset`, `Sheet2`, `Label Schema`, and `Error Taxonomy`. The main dataset has 134 records and 11 columns: serial number, original text, corrected text, language, code-switching, sentiment, intent, error presence, error severity, error type, and annotation rationale.

The workbook also contains summary tables and pivot sheets. These are supporting views; the `Noisy Dataset` sheet is the row-level annotation table.

## Reported coverage

- Language: 45 English, 45 Hindi, 44 Hinglish
- Sentiment: 61 Neutral, 51 Negative, 22 Positive
- Linguistic quality: 44 Correct, 43 Minor Error, 47 Major Error
- Intent: 28 Information Request, 36 Complaint, 26 Feedback, 26 Request for Assistance, 11 Appreciation, 7 General Conversation

These are workbook-reported counts, not independently verified findings.

## Known limitations

- All labels are synthetic starter annotations and require fluent human review.
- The workbook notes that `Error_Type` includes free-text combinations that need normalization to the listed taxonomy.
- No inter-annotator agreement, adjudication results, sampling method, or model evaluation has been established.
- Language conventions for romanized Hindi and mixed-language boundaries should be finalized before annotation.
- The current class distribution may not represent real-world use.

## Privacy and release

The examples are described as synthetic. A pattern-based local check found no email, phone-number, or identity-number matches. That check cannot guarantee that content is free of personal or confidential information. Review text and workbook metadata before every public release; do not add real conversations or identifying data.

## Provenance

Source file: `Revised_Hindi_English_Annotation_Workbook(1).xlsx`, supplied for project setup. The repository copy is renamed for clarity; its annotation content is not represented as corrected or adjudicated.
