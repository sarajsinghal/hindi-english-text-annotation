# Hindi–English Text Annotation

A starter project for annotating Hindi, English, and Hinglish text for language quality, sentiment, intent, and code-switching.

## Project status

The workbook in `data/` contains 134 **synthetic starter examples**. Its annotations are unverified and marked for human review. Do not treat it as ground truth or report model performance from it.

## What is included

- [Annotation workbook](data/Revised_Hindi_English_Annotation_Workbook.xlsx)
- [Annotation guidelines](docs/annotation-guidelines.md)
- [Dataset card and review status](docs/data-card.md)

## Recommended next steps

1. Have fluent Hindi–English annotators review every row independently.
2. Resolve disagreements through adjudication and record reviewer notes.
3. Normalize the current free-text `Error_Type` values to the taxonomy in the guidelines.
4. Version reviewed data separately from the starter workbook and document any changes.
5. Only use adjudicated data for evaluation or model training.

## Data handling

The included examples are described by the workbook as synthetic. Do not add real customer conversations or other personal or confidential information without a documented lawful basis, consent where required, and a privacy review. Keep identifying data out of public releases.

## License

No license has been selected yet. Unless a license is added, standard copyright applies and reuse is not granted by default.
