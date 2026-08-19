# 2D projector trained on ersilia reference library

Positions a compound against the Ersilia Reference Library of 1.3 million molecules, returning coordinates from four complementary projections: PCA, UMAP, t-SNE and TMAP. Each captures a different aspect of the space, PCA preserving global variance while the others emphasise local neighbourhood structure, so a compound can be examined from several perspectives at once. ECFP4 fingerprints and RDKit descriptors provide the input, and coordinates are meaningful only relative to this fixed reference.

This model was incorporated on 2026-03-10.Last packaged on 2026-06-22.

## Information
### Identifiers
- **Ersilia Identifier:** `eos1klk`
- **Slug:** `lazychemvis-reference-library`

### Domain
- **Task:** `Representation`
- **Subtask:** `Projection`
- **Biomedical Area:** `Any`
- **Target Organism:** `Any`
- **Tags:** `Embedding`

### Input
- **Input:** `Compound`
- **Input Dimension:** `1`

### Output
- **Output Dimension:** `8`
- **Output Consistency:** `Fixed`
- **Interpretation:** Coordinates from PCA, UMAP, t-SNE and TMAP projections against the Ersilia reference library.

Below are the **Output Columns** of the model:
| Name | Type | Direction | Description |
|------|------|-----------|-------------|
| pca_x | float |  | First principal component projected on the reference chemical space |
| pca_y | float |  | Second principal component projected on the reference chemical space |
| tmap_x | float |  | First TMAP dimension projected on the reference chemical space |
| tmap_y | float |  | Second TMAP dimension projected on the reference chemical space |
| tsne_x | float |  | First TSNE dimension projected on the reference chemical space |
| tsne_y | float |  | Second TSNE dimension projected on the reference chemical space |
| umap_x | float |  | First UMAP dimension projected on the reference chemical space |
| umap_y | float |  | Second UMAP dimension projected on the reference chemical space |


### Source and Deployment
- **Source:** `Local`
- **Source Type:** `Internal`
- **DockerHub**: [https://hub.docker.com/r/ersiliaos/eos1klk](https://hub.docker.com/r/ersiliaos/eos1klk)
- **Docker Architecture:** `AMD64`, `ARM64`
- **S3 Storage**: [https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos1klk.zip](https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos1klk.zip)

### Resource Consumption
- **Model Size (Mb):** `340`
- **Environment Size (Mb):** `8302`
- **Image Size (Mb):** `9256.49`

**Computational Performance (seconds):**
- 10 inputs: `41`
- 100 inputs: `41.51`
- 10000 inputs: `866.73`

### References
- **Source Code**: [https://github.com/ersilia-os/lazy-chemvis](https://github.com/ersilia-os/lazy-chemvis)
- **Publication**: [https://github.com/ersilia-os/lazy-chemvis](https://github.com/ersilia-os/lazy-chemvis)
- **Publication Type:** `Other`
- **Publication Year:** `2026`
- **Ersilia Contributor:** [Marina18](https://github.com/Marina18)

### License
This package is licensed under a [GPL-3.0](https://github.com/ersilia-os/ersilia/blob/master/LICENSE) license. The model contained within this package is licensed under a [GPL-3.0-or-later](LICENSE) license.

**Notice**: Ersilia grants access to models _as is_, directly from the original authors, please refer to the original code repository and/or publication if you use the model in your research.


## Use
To use this model locally, you need to have the [Ersilia CLI](https://github.com/ersilia-os/ersilia) installed.
The model can be **fetched** using the following command:
```bash
# fetch model from the Ersilia Model Hub
ersilia fetch eos1klk
```
Then, you can **serve**, **run** and **close** the model as follows:
```bash
# serve the model
ersilia serve eos1klk
# generate an example file
ersilia example -n 3 -f my_input.csv
# run the model
ersilia run -i my_input.csv -o my_output.csv
# close the model
ersilia close
```

## About Ersilia
The [Ersilia Open Source Initiative](https://ersilia.io) is a tech non-profit organization fueling sustainable research in the Global South.
Please [cite](https://github.com/ersilia-os/ersilia/blob/master/CITATION.cff) the Ersilia Model Hub if you've found this model to be useful. Always [let us know](https://github.com/ersilia-os/ersilia/issues) if you experience any issues while trying to run it.
If you want to contribute to our mission, consider [donating](https://www.ersilia.io/donate) to Ersilia!
