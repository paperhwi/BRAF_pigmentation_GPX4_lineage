# Pigmentation-associated expression tracks basal *GPX4* dependency in melanoma: comparison with diffuse glioma

Reproducibility repository for the computational analyses, fixed gene-set definitions, sample/compound manifests, and figures accompanying the manuscript comparing *BRAF* V600E treatment-response transcriptomes and basal *GPX4* / ferroptosis vulnerability across melanoma and diffuse glioma. All analyses use publicly available, de-identified datasets; no new participant data were collected.

## Planned Repository Contents

The following curated directories and files will be uploaded to reproduce all results and figures end to end:

| Path | Contents to be uploaded |
| :--- | :--- |
| `docs/` | Audited manuscript (`BRAF_Pigmentation_GPX4_Manuscript_20261124_v6.md` / `.docx`), fixed gene-set summary, and step-by-step execution guide |
| `scripts/` | Python 3.12 analysis and figure scripts: (1) DepMap Public 24Q4 CRISPR/RNA & somatic *BRAF* stratification, (2) CTRPv2 pharmacogenomic harmonization & pan-drug specificity screens (`491` glioma / `475` melanoma entries), (3) strict fold-fitted leave-one-donor-out Ridge cross-validation, (4) three-axis pigmentation / lysosome / cysteine–GSH dissection, (5) MAPK-inhibitor bulk RNA-seq (`PyDESeq2` 0.5.4, common-universe score transforms, LOMO & time-matched control sensitivities), (6) paired clinical biopsy & auxiliary scRNA-seq analyses, and (7) physical-scale figure builders |
| `supplement/` | Reproducibility manifests `S0–S8`, including master index `S0`, frozen 26 developmental (`S1`) and mechanistic/basal (`S2`, with `GBA1` / Entrez `2629` harmonization) gene sets, single-cell operational cell IDs (`S3`), statistical & CTRPv2 pan-drug tables (`S4–S7`), and the multi-sheet Excel workbook `S8` (`Supplementary_Reproducibility_Models_GEO_CTRPv2_20261124.xlsx`: DepMap IDs, Cellosaurus RRIDs, donor IDs, Oncotree diagnoses, *BRAF* annotations, GEO GSM IDs/durations/drugs/matched controls, and CTRPv2 compound IDs) |
| `figures/` | Main Figures `1–7` and Supplementary Figures `1–6` (`PDF` / `SVG` / `PNG`) together with panel-level `source_data/*.csv` tables |
| `data/` | Download scripts and checksum/provenance manifests for public inputs (large raw public matrices are retrieved directly from their official repositories rather than redistributed here) |
| `pyproject.toml` / `requirements.txt` | Pinned Python environment (`numpy`, `scipy`, `pandas`, `statsmodels`, `scikit-learn`, `pydeseq2==0.5.4`, `anndata`, `matplotlib`, `openpyxl`) |

## Public Data Sources

- **DepMap Public 24Q4**: CRISPR `Chronos` gene effects, `log2(TPM + 1)` RNA-seq, somatic mutations, and model metadata (Figshare+ DOI: `10.25452/figshare.plus.27993248.v1`)
- **CTRPv2**: Post-QC small-molecule dose–response AUCs and compound metadata (`ML210`, `RSL3`, `ML162`, `erastin`, and full library)
- **NCBI GEO**:
  - Human treatment-response bulk RNA-seq: `GSE75299`, `GSE103687`, `GSE103688` (melanoma); `GSE249718`, `GSE287972` (astrocytic glioma)
  - Paired clinical melanoma bulk biopsies: `GSE75299`, `GSE196434`, `GSE77940`
  - Auxiliary single-cell RNA-seq: `GSE116237` (Rambow *MEL006* PDX), `GSE72056` (Tirosh patient melanomas), `GSE288791` / `GSM8775515` (murine RCAS-*BRAF* glioma)
