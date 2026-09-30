# DS-A1: Data Provenance and Measurement Audit

## Overview

This repository contains the materials for DS-A1: Data Provenance and Measurement Audit.

The audit evaluates whether a public tracking dataset of continental Black-tailed Godwits (*Limosa limosa limosa*) can support a testable comparison of southward migration timing between juveniles and adults.

**Research question:**  
Does the timing of crossing 52°N during southward migration differ between tracked juvenile and adult Black-tailed Godwits?

## Dataset

The analysis uses the Dryad dataset associated with:

Verhoeven, M. A., Loonstra, A. H. J., McBride, A. D., Kaspersma, W., Hooijmeijer, J. C. E. W., Both, C., Senner, N. R., & Piersma, T. (2022).  
*Age-dependent timing and routes demonstrate developmental plasticity in a long-distance migratory bird.*

Dryad DOI: `10.5061/dryad.02v6wwq4j`

File used:

`2.Adult_and_juvenile_timing_forR.csv`

The dataset license, source information, and SHA-256 hash are documented in `SOURCE_LICENSE_HASH.md`.

## Repository contents

- `DS_A1_godwit_timing.ipynb` — executable Jupyter notebook containing the audit
- `PDF_report.pdf` — exported report
- `2.Adult_and_juvenile_timing_forR.csv` — source dataset used in the audit
- `DATA_CARD.md` — dataset summary and intended use
- `DATA_DICTIONARY.md` — description of dataset variables
- `SOURCE_LICENSE_HASH.md` — source, license, and file hash
- `AI_USE.md` — AI-use and independent-verification log
- `README.md` — repository documentation

## Analysis scope

The analytical subset includes:

- southward migration records;
- crossing of 52°N;
- migration years 2016 and 2017;
- juvenile and adult age groups.

The subset contains 78 migration records from 71 individuals.

## Data audit

The notebook includes checks for:

- schema and data types;
- value ranges;
- missing values;
- duplicate records;
- anomalies;
- possible data leakage;
- measurement differences;
- selection bias;
- repeated observations;
- limits on interpretation.

## Dependencies

The notebook requires:

- Python 3
- pandas

The notebook was developed and executed in Google Colab.

No stochastic or random procedures were used, so no random seed is required.

## How to run

1. Download or clone this repository.
2. Open `DS_A1_godwit_timing.ipynb` in Jupyter Notebook or Google Colab.
3. Make sure `2.Adult_and_juvenile_timing_forR.csv` is available in the same working directory as the notebook.
4. Run all cells from top to bottom.

The notebook should reproduce the data filtering and audit results shown in the report.

## Interpretation boundary

The dataset supports comparison of measured migration timing between juvenile and adult godwits.

However, the observed difference should not be interpreted as evidence for a specific causal mechanism. The dataset also has important limitations related to measurement methods, sample selection, repeated observations, and pooling of migration years.
