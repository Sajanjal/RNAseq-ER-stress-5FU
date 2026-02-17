# UPR / ER Stress Gene Expression in Gastric Cancer Cells / 5FU

## Dataset

- **GEO Accession:** [GSE236987](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE236987)  
- **Title:** A novel lncRNA FUAT1/TNS4 axis confers chemoresistance by suppressing ROS-mediated apoptosis in gastric cancer  
- **Organism:** Homo sapiens  
- **Experiment:** RNA-Seq (Expression profiling)  
- **Cells:** SNU16 gastric cancer cells  
- **Treatments:** Control, 5-FU (7.69 µM, 24h), H2O2 (80 µM, 24h)  
- **Replicates:** 3 per condition  
- **Processed Data:** FPKM values ([link](ftp://ftp.ncbi.nlm.nih.gov/geo/series/GSE236nnn/GSE236987/suppl/GSE236987_lnc_transcripts.FPKM.txt.gz))  
- **BioProject:** [PRJNA993250](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA993250)

---

## Analysis Performed

1. **UPR Gene Selection**  
   Focused on 10 key genes: `HSPA5, DDIT3, ATF4, XBP1, ERN1, EIF2AK3, ATF6, DNAJB9, HERPUD1, PDIA4`

2. **Gene-Level Aggregation**  
   - Summed transcript isoforms to get gene-level FPKM  

3. **Barplots**  
   - Plotted log2(FPKM + 1) for each gene across conditions  
   - Mean ± SD shown for replicates  

4. **Heatmap**  
   - Z-score normalization per gene  
   - Visualizes relative expression across Control, 5-FU, H2O2  

---

## How to Reproduce

1. Load `GSE236987_lnc_transcripts.FPKM.txt.gz` into Python or R  
2. Filter for the 10 UPR genes  
3. Aggregate isoforms by summing FPKM  
4. Compute log2(FPKM+1) and average replicates  
5. Plot barplots and heatmap using Z-score normalization  

---

## Notes

- Z-score normalization highlights **relative up/down regulation per gene**  
- Scripts are in `GSE236987_ER_stress_analysis.ipynb`  
- Further analysis (e.g., clustering or pathway enrichment) can be added later
