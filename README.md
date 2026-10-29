# Earnings by Education in the United States

This project uses the 2026 IPUMS CPS Annual Social and Economic Supplement
(ASEC) to describe average 2025 wage and salary income by education among
US adults ages 25–64 with positive, valid wage income. The R Markdown
analysis groups education into five ordered categories and presents a
bar chart of unweighted sample means. The relationship is descriptive;
it does not estimate the causal effect of education on earnings.

[Rendered analysis](ipums-viz-starter.md)

## Reproduce the analysis

1. Register individually at [IPUMS CPS](https://cps.ipums.org/).
2. Request the most recent ASEC sample (2026 for this project) and the
   variables AGE, SEX, EDUC, and INCWAGE. Leave automatically included
   variables selected. Choose rectangular structure and fixed-width format.
3. Download the matching `.dat.gz` data and DDI `.xml` codebook into a
   local `data/` folder next to `ipums-viz-starter.Rmd`. Keep their matching
   filenames. This analysis uses `cps_00001.xml` and `cps_00001.dat.gz`;
   update the XML filename in the load chunk if your extract number differs.
4. Install R, RStudio, and the required R packages:

   ```r
   install.packages(c("ipumsr", "tidyverse", "scales", "rmarkdown", "knitr"))
   ```

5. Open `ipums-viz-starter.Rmd` in RStudio and choose **Knit to GitHub
   Document**, or run `rmarkdown::render("ipums-viz-starter.Rmd")` from
   the project folder.

For the same results, use the 2026 ASEC sample. A later sample will change
the results, and its codebook and citation should be checked before reuse.
No survey weighting is applied; weighting is an optional extension in the
activity. The five education categories follow the CPS codes documented
in the extract rather than the different codes in the original starter.

## Citation

Sarah Flood, Miriam King, Renae Rodgers, Steven Ruggles, J. Robert Warren,
Daniel Backman, Etienne Breton, Grace Cooper, Julia A. Rivera Drew,
Stephanie Richards, David Van Riper, and Kari C.W. Williams. IPUMS CPS:
Version 13.0 [dataset]. Minneapolis, MN: IPUMS, 2025.
<https://doi.org/10.18128/D030.V13.0>

## Data handling

Raw data and XML codebooks are excluded by `.gitignore`. Each user should
obtain their own extract from IPUMS. Upload the `.Rmd`, rendered `.md`,
chart-image folder, README, and `.gitignore`; do not upload `data/`.
