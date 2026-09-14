# CBAG — Class-Balanced Adversarial Generation

Self-contained implementation of **CBAG** (Class-Balanced Adversarial Generation) with real generators and **Tri-Gate** filtering.

Designed for UAV and Access-Point wireless network traffic datasets.

## Repository Structure

```
CBAG-Targeted/
├── README.md
├── LICENSE
├── requirements.txt
│
├── Notebooks (run these)
│   ├── cbag-uav1.ipynb              # UAV1 – targeted to Normal
│   ├── CBAG_AccessPoint_final_1.ipynb  # AccessPoint / UAV2
│   └── CBAG_GSC_final_1.ipynb         # UAV3 / GSC (benign-mimicry)
│
└── Results
    ├── CBAG_UAV1_results.zip
    ├── CBAG_UAV3_GSC_results (2).zip
    └── cbag_out_AccessPoint (2).zip
```

## Quick Start

```bash
pip install -r requirements.txt
# Edit the dataset path (glob) in Cell 1 of the notebook you want to run
jupyter notebook cbag-uav1.ipynb
```

1. Set configuration in the first code cell (dataset path, SUBSAMPLE, EVAL_CAP, gate thresholds).
2. Run cells top-to-bottom.
3. Each phase caches to disk — you can re-run the Tri-Gate phase with different thresholds without regenerating candidates.

## Generators (all inlined)

- Classical: C-SA, C-RL, C-PSO, C-GA, C-BO
- Generative: CG-Diffusion, CC-CGAN
- Black-box: HopSkipJump, Sign-OPT

## Getting a DOI (Zenodo)

1. Create a new **Release** on GitHub (tag `v1.0.0`, title "CBAG v1.0").
2. Go to [zenodo.org](https://zenodo.org) → Login with GitHub.
3. Enable the repository **CBAG-Targeted**.
4. Zenodo will automatically archive the release and give you a DOI.

## License

MIT License
