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

Paper reference: [ETHICA-MT: Introducing a Framework and Dataset for Studying Ethical Orientations in LLM-based Machine Translation](https://arxiv.org/abs/2506.10150)

## Included files
- `EthicaMT_official_dataset.xlsx` (primary spreadsheet release)
- `EthicaMT_official_dataset.csv` (plain-text equivalent)
- `model_wise_outputs/` (per-model CSV/XLSX splits)

## Scope and exclusions
- Included: scenarios, source texts, and translations across all language pairs in this release.
- Excluded: prompt files (already documented in the paper).
- Excluded: LLM-as-Judge ranking/evaluation artifacts (not part of the official released dataset table).

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
The paper positions ETHICA-MT as a framework for identifying, measuring, and mitigating ethical bias in machine translation. In line with that framing, this release is intended for research on ethical orientations in translation behavior and for improving accountability in MT systems.

> "This work raises a new and subtle issue about the ethics of machine translation, a topic long examined in human translation yet rarely discussed for machine translations. Earlier machine translation systems were too limited to make such ethical dilemma changes meaningful. However, general-purpose LLMs change this by mediating language at scale and enabling deeper questions about embedded biases and their downstream effects. From this standpoint, our paper offers one of the first systematic studies to identify, quantify, and mitigate these biases in Machine Translation, with practical frameworks and evaluation protocols. By bringing ethical reasoning into a standard task, we aim to ensure that technological progress (Machine Translation, in our case) translates into more ethical and accountable systems."
