# CBAG — Class-Balanced Adversarial Generation for Network Intrusion Detection

Self-contained Jupyter notebooks implementing **CBAG** (Class-Balanced Adversarial Generation) with real generators and a **Tri-Gate** filter.

Designed for UAV / Access-Point wireless network traffic datasets. The method generates realistic adversarial samples that:

1. **Evade** a target detector (Gate-1: high P(benign/Normal))
2. Stay close to the original distribution according to an **oracle** and optional CMR (Gate-2)
3. Satisfy an L1-distance / feature-constraint operating point (Gate-3)

## Notebooks

| Notebook | Dataset | Target class | Notes |
|----------|---------|--------------|-------|
| `CBAG_UAV1_clean.ipynb` | UAV-Case1 | Normal | Classic targeted setting |
| `CBAG_AccessPoint_clean.ipynb` | AccessPoint | Normal (~20.9%) | Real Normal class present |
| `CBAG_GSC_clean.ipynb` | UAV3 / GSC | Benign | Benign-mimicry variant |

## Generators (inlined)

- Classical: C-SA (Simulated Annealing), C-RL, C-PSO, C-GA, C-BO
- Generative: CG-Diffusion, CC-CGAN
- Black-box: HopSkipJump, Sign-OPT

## Quick start

```bash
pip install -r requirements.txt
# Place the CSV datasets or update the `glob` path in Cell 1 of each notebook
jupyter notebook CBAG_UAV1_clean.ipynb
```

1. Edit the **CONTROL PANEL** in Cell 1 (dataset path, SUBSAMPLE, EVAL_CAP, gate thresholds, …).
2. Run cells top-to-bottom. Each phase writes a cache under `cbag_cache_<DATASET>/`.
3. Re-run Phase 3 (`phase3`) with different Tri-Gate settings without regenerating candidates.

## Citation / DOI

If you use this code, please cite the associated paper (update with your arXiv / journal reference).

A DOI for this repository can be obtained by:

1. Creating a GitHub Release (e.g. `v1.0.0`)
2. Linking the repository to [Zenodo](https://zenodo.org) (Settings → GitHub → Enable)
3. Zenodo will automatically archive the release and mint a DOI.

## License

MIT License — free for academic and research use.
