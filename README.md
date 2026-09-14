# CBAG — Class-Balanced Adversarial Generation for Network Intrusion Detection

Self-contained Jupyter notebooks implementing **CBAG** (Class-Balanced Adversarial Generation) with real generators and a **Tri-Gate** filter.

Designed for UAV / Access-Point wireless network traffic datasets.

## Current Status

The repository structure is ready (README, requirements, LICENSE).

**The three full cleaned notebooks are prepared and available in the project artifacts.**  
Please upload them via the GitHub web interface:

1. Go to this repository
2. Click **Add file → Upload files**
3. Upload these three files:
   - `CBAG_UAV1_clean.ipynb`
   - `CBAG_AccessPoint_clean.ipynb`
   - `CBAG_GSC_clean.ipynb`

All code functionality is 100% preserved (only empty cells removed + improved documentation).

## Notebooks (after upload)

| Notebook | Dataset | Target class | Notes |
|----------|---------|--------------|-------|
| `CBAG_UAV1_clean.ipynb` | UAV-Case1 | Normal | Classic targeted setting |
| `CBAG_AccessPoint_clean.ipynb` | AccessPoint | Normal (~20.9%) | Real Normal class present |
| `CBAG_GSC_clean.ipynb` | UAV3 / GSC | Benign | Benign-mimicry variant |

## Generators (inlined)

- Classical: C-SA, C-RL, C-PSO, C-GA, C-BO
- Generative: CG-Diffusion, CC-CGAN
- Black-box: HopSkipJump, Sign-OPT

## Quick start

```bash
pip install -r requirements.txt
# Update the dataset `glob` path in Cell 1 of each notebook
jupyter notebook CBAG_UAV1_clean.ipynb
```

## Getting a DOI

1. Create a GitHub Release (tag `v1.0.0`)
2. Go to https://zenodo.org → Login with GitHub → Enable this repository
3. Zenodo will mint a DOI for the release

## License

MIT License
