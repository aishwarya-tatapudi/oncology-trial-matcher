# Oncology Clinical Trial Matching Assistant

> Status: Work in progress — planning and initial development.
> No working end-to-end demo or evaluation results yet.

## Overview

A planned Python prototype that will retrieve potentially relevant
cancer clinical trials for synthetic patient records and assess
individual eligibility criteria.

The goal is to return evidence-backed assessments of:
- Met
- Not met
- Unknown due to missing information

This is a portfolio and learning project, not a clinical decision tool.

## Current progress

The initial project scope and architecture have been outlined.
Implementation and validation are the next steps.

## Planned workflow

Synthetic patient record
→ Structured patient summary
→ Trial retrieval
→ Criterion-level eligibility assessment
→ Results and explanations

Trial relevance and trial eligibility will be treated separately:
a relevant search result does not establish eligibility.

## Planned components

| File | Responsibility |
|------|----------------|
| fetch_trials.py | Retrieve trial data from ClinicalTrials.gov |
| parse_patients.py | Parse synthetic patient records |
| build_index.py | Create and store trial-text embeddings |
| matcher.py | Retrieve trials and assess eligibility criteria |
| evaluate.py | Compare assessments with manually labeled examples |
| app.py | Display results in a Streamlit interface |

These are planned modules, not a list of completed features.

## Planned technology stack

- Python
- requests and pandas
- sentence-transformers
- ChromaDB
- An LLM API
- scikit-learn
- Streamlit

The stack may change during development.

## Roadmap

- [x] Define project scope and initial architecture
- [ ] Download and inspect a small set of cancer trials
- [ ] Prepare synthetic patient examples
- [ ] Implement and test trial retrieval
- [ ] Implement criterion-level eligibility assessment
- [ ] Create a manually labeled evaluation set
- [ ] Report evaluation results and failure cases
- [ ] Build a Streamlit demo
- [ ] Add installation and usage instructions

## Evaluation plan

Compare the system's assessments with manually labeled examples.
Review incorrect matches, missed matches, and failures to acknowledge
missing patient information.

No performance claims will be made before evaluation.

## Data and safety

- Use synthetic patient records only.
- Do not upload real patient records or identifying information.
- Do not commit API keys or credentials.
- Preserve missing information as unknown.
- The prototype will not determine final trial enrollment eligibility.

## Running the project

Setup and execution instructions will be added once the first
working component is available.
