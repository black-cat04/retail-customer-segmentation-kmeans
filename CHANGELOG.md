# CHANGELOG — Week 5 → Week 9 Notebook Transformation

**File:** `2025em1200017_ApexProject_Week5.ipynb`  
**Date:** July 2026  
**Summary:** Transformed from Week 5 progress submission (28 cells) to Week 9 final submission (42 cells)

---

## Structural Changes

| Change | Detail |
|--------|--------|
| Total cells | 28 → 42 |
| Markdown cells | 12 → 25 |
| Code cells | 16 → 17 |
| Sections | 9 (with Appendix) → 11 (per Week 9 template) |
| Appendix | **Removed** — content promoted to main body |
| "Planned Next Steps" section | **Removed** — absorbed into Conclusion |

---

## Section-by-Section Changes

### Cell 0: Title & Student Details
- **MODIFIED**: Updated from "Week 5 Progress" to "Week 9 — Final Submission"
- Added student name, student ID, programme in a formatted table
- Removed the "deferred to Appendix" disclaimer

### Cell 1: Imports
- **MODIFIED**: Consolidated all imports into a single cell
- Added: `sklearn.metrics.silhouette_score`, `sklearn.preprocessing.MinMaxScaler`, `sklearn.decomposition.PCA`, `sklearn.manifold.TSNE`, `sklearn.model_selection.train_test_split`, `sklearn.pipeline.Pipeline`, `sklearn.preprocessing.PowerTransformer`, `sklearn.preprocessing.StandardScaler`, `sklearn.feature_selection.VarianceThreshold`, `sklearn.cluster.KMeans`
- Previously these were scattered across Appendix cells

### Cell 2: Section 2 — Problem Statement & Business Goal
- **NEW**: Added complete problem statement with:
  - Business objective (targeted marketing via micro-segmentation)
  - Analytical approach (K-Means on RFM)
  - Explicit scope definition (included vs. excluded) — **addresses Feedback #1**

### Cell 3: Section 3 — Dataset Description
- **MODIFIED**: Enhanced from old "Section 1. Dataset Overview"
- Added formal dataset source citation with URL
- Added data relationship description

### Cells 4–5: Dataset Summary Table & Data Dictionary
- **KEPT**: Preserved with original outputs

### Cell 6: Section 4 Header — Data Preparation
- **NEW**: Combined old "Data Inspection" and "Data Preprocessing" into unified section

### Cell 7: Feature Selection Column Decisions
- **NEW**: Added explicit KEEP/DROP/IGNORE decision table — **addresses Feedback #2**
- Covers all 5 flagged columns: `email` (DROP), `phone` (DROP), `product_name` (IGNORE), `store_location` (IGNORE), `payment_method` (IGNORE)
- Includes rationale for every decision

### Cell 8: Reviews & Support Tickets Decision
- **NEW**: Added clear project decision to EXCLUDE both tables — **addresses Feedback #4**
- 3-point rationale: low coverage, orthogonal dimension, methodological cleanness
- Future work outlined for post-hoc integration

### Cells 9–12: Data Inspection
- **KEPT**: Code cells preserved with outputs
- **MODIFIED**: Audit observations markdown enhanced with MCAR terminology and explicit reference to Figure 1

### Cells 13–15: Data Cleaning
- **KEPT**: Preprocessing code preserved with outputs
- **MODIFIED**: Preprocessing decisions markdown rewritten with numbered structure, added revenue feature explanation, clearer imputation rationale

### Cells 16–24: Exploratory Data Analysis
- **MODIFIED**: Section renumbered to "5. EDA"
- **NEW**: Added 4 interpretation markdown cells (one after each visualization block)
  - Figures 2–5 interpretation (distributions)
  - Figures 6–8 interpretation (demographics)
  - Figures 9–10 interpretation (time trends)
  - EDA Summary table correlating findings to segmentation implications
- **KEPT**: All 4 EDA code cells with their original outputs
- **addresses Feedback #5** (improved figure captions and interpretations)

### Cells 25–29: Feature Engineering
- **MODIFIED**: Section renumbered to "6. Feature Engineering"
- **KEPT**: RFM aggregation code with outputs
- **MODIFIED**: Feature Engineering Justification completely rewritten — **addresses Feedback #3**
  - Explains why additional customer attributes (age, gender) were NOT added to clustering features
  - Explains +1 adjustment for Box-Cox compatibility
  - Explains anchor date logic
- **NEW**: RFM distribution visualization (Figure 12) with interpretation

### Cells 30–33: Basic Model Implementation
- **NEW SECTION**: "7. Basic Model Implementation" — promoted from Appendix
- **NEW**: Model selection justification (K-Means rationale)
- **NEW**: Preprocessing pipeline description
- **NEW**: Elbow Method + Silhouette Score analysis (Figure 13–14) with interpretation
- **NEW**: Final K-Means fitting with k=4
- Old Appendix Cell 25 (bundled pipeline) replaced with restructured code

### Cells 34–37: Basic Evaluation & Interpretation
- **NEW SECTION**: "8. Basic Evaluation & Interpretation"
- **NEW**: Cluster centroid summary table
- **NEW**: Radar chart (Figure 15) for persona profiling
- **NEW**: PCA projection (Figure 16) — promoted from Appendix Cell 26, enhanced
- **NEW**: t-SNE projection (Figure 17) — promoted from Appendix, enhanced
- **NEW**: Cluster interpretation markdown with persona archetypes and limitations

### Cells 38–39: Reproducibility & Documentation
- **NEW SECTION**: "9. Reproducibility & Documentation"
- Documents random state usage, pipeline architecture, data source, and no manual interventions
- **NEW**: Environment version printing code cell

### Cell 40: Conclusion
- **REWRITTEN**: Old "Preliminary Observations" completely replaced with proper conclusion
- Key findings (4 points)
- Business value (3 applications)
- Future work (5 directions including reviews/tickets integration)

### Cell 41: References
- **ENHANCED**: Added formal academic citations for all libraries
- Added RFM methodology reference (Fader et al., 2005)
- Added K-Means++ reference (Arthur & Vassilvitskii, 2007)

---

## Removed Cells

| Old Cell | Content | Disposition |
|----------|---------|-------------|
| Cell 22 | "Preliminary Observations & Learnings" | Absorbed into new Conclusion (Section 10) |
| Cell 23 | "Planned Next Steps" | Absorbed into Conclusion → Future Work |
| Cell 24 | "Appendix: Future Implementation Preview" header | Removed — content promoted to main body |
| Cell 25 | K-Means pipeline code (Appendix) | Replaced with new Section 7 code (restructured) |
| Cell 26 | PCA/t-SNE code (Appendix) | Replaced with new Section 8 code (enhanced) |

---

## Instructor Feedback Resolution Summary

| # | Feedback | Resolution Cell(s) | Status |
|---|----------|-------------------|--------|
| 1 | Clarify analysis scope | Cell 2 (Problem Statement — Scope section) | ✓ |
| 2 | Sparse column KEEP/DROP/IGNORE | Cell 7 (Column Decision Table) | ✓ |
| 3 | Customer personas — meaningful attributes only | Cell 27 (FE Justification — additional attributes rationale) | ✓ |
| 4 | Reviews & Support Tickets decision | Cell 8 (Integration Decision) | ✓ |
| 5 | Improve documentation | All markdown cells enhanced; figure interpretations added | ✓ |
