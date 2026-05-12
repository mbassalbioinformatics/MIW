# Mesa Identification Workflow (MIW)

The Mesa Identification Workflow (MIW) is a high-resolution computational pipeline designed for the precise identification, spatial profiling, and quantification of **Methylation Mesas (MM)** from Whole Genome Bisulfite Sequencing (WGBS) data. 

Historically, DNA methylation regulatory elements have been defined by static sequence density (e.g., CpG Islands). The MIW pipeline redefines these elements by identifying regions of dynamic biophysical hypersensitivity, isolating the narrow-width (~45–300 bp) structural boundaries that dictate functional gene reactivation.

## 📖 Documentation & Workflow
To support academic reproducibility, the workflow is documented in our Wiki. The pipeline is divided into three core stages:

1. **[WGBS Pre-Processing (FASTQ to BedGraph)](https://github.com/mbassalbioinformatics/MIW/wiki/1-WGBS-Pre-Processing)**: Standardized alignment and preliminary Differentially Methylated Region (DMR) calling.
2. **[Mesa Identification Core (Pseudo-code)](https://github.com/mbassalbioinformatics/MIW/wiki/2-Mesa-Identification-Logic)**: The logic and thresholds used to identify the "high-low-high" hypersensitive boundaries and isolate the Mesa core. 
3. **[Manuscript Figure Generation](https://github.com/mbassalbioinformatics/MIW/wiki/3-Figure-Generation)**: Methodologies used for geneting the manuscript figures.

## ⚖️ Licensing & Commercial Use

The MIW pipeline and associated logic are dual-licensed to support both open academic research and commercial applications.

**For Academic and Non-Profit Research:**
This workflow is provided under the **GNU AGPLv3** license. You are free to use, modify, and distribute this methodology for non-commercial, academic, and personal research purposes. 

**For Commercial and For-Profit Use:**
The AGPLv3 license strictly requires that any network-interacting software linking to or utilizing this workflow must also be fully open-sourced. If you wish to use the MIW pipeline in a commercial setting, integrate it into a proprietary drug-discovery platform, or offer it as a service without open-sourcing your own corporate codebase, you must obtain a commercial license.

To inquire about commercial licensing, partnerships, or enterprise implementation, please contact me directly.
