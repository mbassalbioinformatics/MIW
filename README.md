# MIW: Mesa Identification Workflow

The **Mesa Identification Workflow (MIW)** is a high-resolution computational pipeline designed for the precise identification, spatial profiling, and multi-omic quantification of **Methylation Mesas (MM)** from Whole Genome Bisulfite Sequencing (WGBS) data.

Historically, DNA methylation regulatory elements have been defined by static sequence density (e.g., canonical CpG Islands). The MIW pipeline redefines these elements by identifying regions of dynamic biophysical hypersensitivity, isolating the narrow-width (~45–300 bp) structural boundaries that dictate functional, sequence-independent gene reactivation.

## 📊 Repository Contents
This repository hosts the downstream analytical and visualization source code required to reproduce the multi-omic profiling and manuscript figures presented in our publications. 

**Note on Core IP:** To support academic reproducibility while protecting commercial IP, the foundational data engineering and plotting scripts are provided here in full. The proprietary mathematical algorithms used for the *de novo* boundary-calling and biophysical isolation of Mesas (Phase 2) are documented conceptually in the Wiki, but the raw execution scripts are not hosted in this public repository.

## 📖 Documentation & Workflow
Complete documentation for the MIW architecture is available in our [GitHub Wiki](https://github.com/mbassalbioinformatics/MIW/wiki). The pipeline is structured into distinct operational phases:

### Core Pipeline
1. **[Phase 1: WGBS Pre-Processing & Preliminary DMR Calling](https://github.com/mbassalbioinformatics/MIW/wiki/Phase-1:-WGBS-Pre%E2%80%90Processing-&-Preliminary-DMR-Calling)**
   Standardized alignment (Msuite2), base-resolution methylation extraction, and baseline Differentially Methylated Region (DMR) calling (Defiant & Metilene).
2. **[Phase 2: Mesa Identification Logic (Pseudo-code)](https://github.com/mbassalbioinformatics/MIW/wiki/Phase-2:-Mesa-Identification-Logic)**
   The conceptual framework, spatial rulesets, and thresholds utilized by our proprietary module to identify "high-low-high" hypersensitive boundaries and isolate the Mesa core. 

### Multi-Omic Profiling & Figure Generation
The comprehensive methodologies and R scripts used for downstream visualization are explicitly detailed across the following figure-specific pages:
* **[Manuscript Figure 1](https://github.com/mbassalbioinformatics/MIW/wiki/Manuscript-Figure-1)**: High-resolution spatial profiling (ViewBS), structural width evaluation, and global spatial heatmaps.
* **[Manuscript Figure 2](https://github.com/mbassalbioinformatics/MIW/wiki/Manuscript-Figure-2)**: Genomic compartment localization, TSS-core topological depletion, and DNA methylation/expression correlation.
* **[Manuscript Figure 3](https://github.com/mbassalbioinformatics/MIW/wiki/Manuscript-Figure-3)**: ChIP-Seq intersection mapping (ComplexHeatmap), genome-wide density (circlize), and permutation testing (regioneR).
* **[Manuscript Figures 4 & 5](https://github.com/mbassalbioinformatics/MIW/wiki/Manuscript-Figures-4&5)**: CRISPR-DiR targeted demethylation kinetics and functional assay integration.
* **[Manuscript Figure 6](https://github.com/mbassalbioinformatics/MIW/wiki/Manuscript-Figure-6)**: High-resolution 4C-Seq chromatin looping visualization (Sushi).

## ⚙️ Dependencies
The downstream plotting and analysis scripts provided in this repository heavily utilize R. Key packages include:
* `tidyverse` (Data wrangling & `ggplot2`)
* `pheatmap` & `ComplexHeatmap` (Spatial gradients and chromatin enrichment)
* `UpSetR` (High-dimensional set intersections)
* `circlize` (Genome-wide density distributions)
* `Sushi` (4C-Seq chromatin conformation mapping)
* `regioneR` (Monte Carlo permutation testing)

## ⚖️ Licensing & Commercial Use

The MIW architecture and the code provided within this repository are dual-licensed to support both open academic peer-review and commercial applications.

**For Academic and Non-Profit Research (GNU AGPLv3):**
This workflow is provided under the GNU AGPLv3 license. You are free to use, modify, and distribute this methodology for non-commercial, academic, and personal research purposes. 

**For Commercial and For-Profit Use:**
The AGPLv3 license strictly requires that any network-interacting software linking to, modifying, or utilizing this workflow must also be fully open-sourced under the same license. 

If you wish to utilize the MIW pipeline in a commercial setting, integrate its spatial definitions into a proprietary drug-discovery platform, or utilize the methodology without open-sourcing your own corporate codebase, **you must obtain a commercial license.**

To inquire about commercial licensing, targeted CRISPR-DiR partnerships, or enterprise implementation, please contact the lead author directly.

## 📝 Citation
If you utilize these scripts or the Mesa spatial framework in your research, please cite our corresponding publication:

> *[Placeholder for Nature Communications Paper Citation: Authors, Title, Journal, Year, DOI]*
