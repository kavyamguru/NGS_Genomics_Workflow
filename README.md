# 🧬 NGS – Genome Sequencing and Assembly Analysis

This repository documents the coursework and report for the **Next Generation Sequencing (NGS)** module (Exam No: **B269797**) from the **MSc Bioinformatics** programme at the **University of Edinburgh**.

It provides a comparative analysis of sequencing and genome assembly strategies across large, repeat-rich vertebrate genomes, focusing on the *Pleurodeles waltl* (Iberian ribbed newt) as a regenerative model organism.

---

## 📖 Overview

The project critically evaluates the study:

> **Brown, T., Mishra, P. et al. (2025)**  
> “Chromosome-scale genome assembly reveals how repeat elements shape non-coding RNA landscapes active during newt limb regeneration.”  
> *Cell Genomics, 5(2): 100761.*

and compares it with assemblies from:
- **Axolotl (*Ambystoma mexicanum*)**
- **African lungfish (*Protopterus annectens*)**
- **Human (T2T-CHM13)**

---

## 🧩 Key Topics Covered

- **Long-read sequencing technologies** – PacBio HiFi, Oxford Nanopore  
- **Hi-C scaffolding** for chromosome-scale assembly  
- **DeepVariant polishing** and machine-learning-based variant correction  
- **Repeat annotation and genome complexity** (TEs, Gypsy, hAT transposons)  
- **BUSCO and QV quality assessment metrics**  
- **Comparative genomics** across amphibian and vertebrate species  
- **Recommendations for hybrid assemblies and functional validation**

---

## 🧠 Major Insights

| Aspect | *P. waltl* (Newt) | Axolotl | Lungfish | Human (T2T) |
|--------|-------------------|----------|-----------|-------------|
| Genome Size (Gb) | 20.3 | 32 | 40 | 3 |
| Repeat Content (%) | 74 | ~60 | 61.7 | ~50 |
| BUSCO Completeness (%) | 97.2 | 96.5 | 95.4 | 99 |
| Contig N50 (Mb) | 45.6 | 2 | 1.6 | Nearly gapless |
| Sequencing Platform | PacBio HiFi + Hi-C | ONT + Optical Map | ONT + Hi-C | PacBio HiFi + ONT |

---

## ⚙️ Computational Considerations

- Genome size required **>1 TB RAM** for Hifiasm assembly  
- GPU acceleration used for DeepVariant polishing  
- Hi-C scaffolding processed on high-memory compute nodes (Eddie HPC)  
- Estimated runtime: **2–3 weeks**

---

## 💡 Recommendations

- Integrate **ONT ultra-long reads** and **optical mapping** for resolving heterochromatic repeats  
- Employ **machine-learning repeat annotation tools** (RepeatModeler, EDTA)  
- Use **hybrid polishing** with Illumina short reads (Pilon, FreeBayes)  
- Validate gene functions using **RNA-Seq**, **CRISPR**, or **RNAi** approaches  
- Adopt **cloud-based or GPU-accelerated pipelines** for cost-efficiency

---

## 📘 References

Includes key works from:
- Brown et al., *Cell Genomics* (2025)  
- Schloissnig et al., *PNAS* (2021)  
- Wang et al., *Cell* (2021)  
- Nurk et al., *Science* (2022)  
- Wenger et al., *Nat Biotechnol* (2019)
