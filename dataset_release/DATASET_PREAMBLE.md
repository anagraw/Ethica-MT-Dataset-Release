# ETHICA-MT Official Dataset Release

This release provides the official ETHICA-MT dataset used for the paper, in a consolidated and publication-ready format.

The dataset includes, for all language pairs in this release:
- ethically conflicted translation scenarios,
- source texts,
- source and target language directions,
- and translations under three conditions:
  - baseline (no explicit ethical steering),
  - ethic-1-following translation,
  - ethic-2-following translation.

This package is intended to support reproducibility, comparative analysis across language directions, and model-wise inspection of ethical steering behavior.

Paper reference: [ETHICA-MT: Introducing a Framework and Dataset for Studying Ethical Orientations in LLM-based Machine Translation](https://openreview.net/pdf/63d36ab8adcc315a98d1dae1f569aaa98f6fdaf1.pdf)

## Included files
- `EthicaMT_official_dataset.xlsx` (primary spreadsheet release)
- `EthicaMT_official_dataset.csv` (comma-separated export)
- `EthicaMT_official_dataset_readable.tsv` (recommended plain-text file; tab-separated with escaped line breaks)
- `model_wise_outputs/` (per-model CSV/XLSX splits)

## Scope and exclusions
- Included: scenarios, source texts, and translations across all language pairs in this release.
- Excluded: prompt files (already documented in the paper).

## Data dictionary
- `model`: Translation model used to generate translations
- `record_id`: Unique row identifier
- `source_language`: Source language name
- `target_language`: Target language name
- `ethic_1`: First ethical framework in conflict pair
- `ethic_2`: Second ethical framework in conflict pair
- `scenario`: Translation scenario that creates ethical conflict
- `purpose_1`: Goal aligned with ethic_1
- `purpose_2`: Goal aligned with ethic_2
- `target_audience`: Intended audience of translated text
- `source_text`: Source text to translate
- `translation_no_ethic`: Baseline translation without ethical steering
- `translation_ethic_1_following`: Translation explicitly following ethic_1 purpose
- `translation_ethic_2_following`: Translation explicitly following ethic_2 purpose

## Responsible / Ethics Statement
Our intention in including harmful language in our benchmark was strictly methodological. Our goal was to study how MT systems handle such content, not to promote or normalize it. The level of explicitness was guided by internal criteria: content had to be strong enough to create a meaningful ethical conflict, but not gratuitously escalated beyond what is typical in real-world discourse. We recognize that prompts capable of eliciting controversial material can be misused. We therefore explicitly discourage reuse of the prompts for non-research purposes.
