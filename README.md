# Modelling of Tumour Growth with Respect to the Use of Anti-Cancer Agents
This repository contains individual fittings performed on Tumour Volume Models (TVMs) as described by Dr. A. Nasim et al. [1] and Professor J. Yates and A. Fairman [2].

## Data Sources
The analysis utilises publicly available datasets accessed through the [PDXNet Portal](https://portal.pdxnetwork.org/). Both control and drug data were obtained from the dataset. The anti-cancer agent studied is Docetaxel, with its corresponding PK model accessed from Neil Evans et al. [3]. The analysis focuses on the Invasive Breast Carcinoma population data and was performed via [Monolix](https://lixoft.com/products/monolix/).

## Folder Structure
- **Control Analysis**: Contains individual fits (119 for each analysis) and models analysed under control conditions (no drug is present).
  - *Surrey TVM:* Individual fits and models from the Surrey TVM.
    - Diffusion-Limited model (varying GF(0))
      - $GF(0) = 0.25$
      - $GF(0) = 0.50$
    - Proliferative Rim model
    - Surface Growth model
  - *Yates' TVM:* Individual fits and models from the Yates TVM, for varying $GF(0)$.
    - $GF(0) = 0.25$
    - $GF(0) = 0.50$
    - $GF(0) = 0.75$
- **Drug Analysis**: Contains individual fits (33 for each analysis) and models analysed under drug conditions (Docetaxel administration).
  - *Surrey TVM:* Individual fits and models from the Surrey TVM, including coupling mechanisms and for varying GF(0).
    - Diffusion-Limited model (varying GF(0))
      - Power Coupling
        - $GF(0) = 0.25$
        - $GF(0) = 0.50$
    - Surface Growth model
      - Hill Coupling
      - Power Coupling
  - *Yates' TVM:* Individual fits and models from the Yates TVM, including coupling mechanisms (Michaelis-Menten).
    - $GF(0) = 0.25$
    - $GF(0) = 0.50$
    - $GF(0) = 0.75$


## File Naming Convention
Each folder contains an empty `.txt` file used to denote the combination of error model and distribution chosen for the analysis, e.g. `Constant-Normal.txt`

## References
[1] Nasim, A., et al. "A Spatially Resolved Mechanistic Growth Law for Cancer Drug Development Predicting Tumor Growing Fractions." Cancer Research Communications 2.8 (2022): 754-766. [Link](https://aacrjournals.org/cancerrescommun/article/2/8/754/707358/A-Spatially-Resolved-Mechanistic-Growth-Law-for)

[2] Yates, J., & Fairman, A. "How translational modeling in oncology needs to get the mechanism just right." Cancer Research Communications (2023). [Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8932697/)

[3] Evans, N., et al. "Modelling of tumour growth and cytotoxic effect of docetaxel in xenografts." British Journal of Cancer 109.6 (2013): 1627-1637. [Link](https://pubmed.ncbi.nlm.nih.gov/23948442/)