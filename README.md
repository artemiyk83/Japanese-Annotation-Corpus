# OJ to cNJ CoS standardized locked annotation corpus

Version 1.0, released 2026-08-18.

This folder is a publication-oriented raw-data release for verification and reuse. It contains one workbook per annotated text. Every workbook has exactly two worksheets:

- **Annotations** — the canonical flat data table; one retained clause-level annotation record per row.
- **Metadata** — text-level provenance, checksums, lock status, and release notes.

## Corpus scope

- 19 text-specific workbooks
- OJ, EMJ, LMJ, and cNJ
- 2,185 retained rows
- 87 identically ordered columns in every Annotations sheet
- no unresolved annotation-review rows
- clause segmentation unchanged from the locked annotation layer

## Reproducibility and provenance

Use **Analysis_Row_ID** as the stable row identifier. **Source_Alias**, **Source_Sheet**, and **Source_Row** locate the record in the original annotation workbook. **Source_SHA256** identifies the exact original workbook. Local absolute paths have been removed from this public release; the source filename and checksum remain.

The release workbooks contain locked annotation values only. They contain no substantive model results and no hidden transformation sheets. Missing values were not imputed: blank, 'n/a', 'none', 'unknown', and uncertainty categories retain their documented distinctions.

## Files

- *_CoS_raw_data_v1.xlsx — one standardized workbook per text
- DATA_DICTIONARY.tsv — variable definitions and controlled vocabularies
- MANIFEST.tsv — text/file inventory and source, locked-input, and publication checksums
- SHA256SUMS.txt — checksums for integrity verification
- RELEASE_CHECKLIST.md — items the author must complete before making the repository public

## Minimal verification workflow

1. Verify downloaded files against SHA256SUMS.txt.
2. Confirm that each workbook has only Annotations and Metadata.
3. Join or compare rows using Analysis_Row_ID, Clause_ID, and the source-row provenance fields.
4. Apply analytical inclusion rules explicitly, especially Count_Predicate_RD2, Counting_Status, and Predicate_Status.
5. Report dataset version and file checksums with verification results.

## Annotation and statistical policy

The release implements the accepted P01-P03 decisions. The factorized CoS fields are the primary annotation standard. EF RD2 is reported as 0.89 at hundredths precision; 0.90 is treated as an internal reporting inconsistency. Strict what-you-see transitivity is primary, with lexical-valency recoding reserved for a separately documented robustness analysis.

## Citation and license

Before public release, the author must add the final dissertation citation, repository URL or DOI, author details, and an explicit data license. No license is inferred by this package.
