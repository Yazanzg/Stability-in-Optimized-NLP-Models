# PROCESS-2 staged scripts (thesis-reported)

Run from the repository root after installing dependencies and placing PROCESS-2 data locally.

| Order | Script | Main outputs |
|------:|--------|----------------|
| 1 | `validate_process2_loader.py` | `outputs/process2_loader_validation_report.txt` |
| 2 | `validate_process2_preprocessing.py` | `outputs/process2_preprocessing_validation_report.txt` |
| 3 | `validate_process2_features.py` | `outputs/process2_features.csv`, feature validation report |
| 4 | `validate_process2_baselines.py` | `outputs/process2_baseline_results.csv`, `outputs/baseline_results.csv` |
| 5 | `validate_process2_optimization.py` | `outputs/process2_optimized_results.csv`, `outputs/optimized_results.csv` |
| 6 | `validate_process2_shap.py` | `outputs/shap/process2_shap_values_*.csv` (6 files, dev split) |
| 7 | `validate_process2_stability.py` | `outputs/process2_stability_results.csv`, `outputs/direct_shap_stability.csv` |
| 8 | `validate_process2_bootstrap_stability.py` | `outputs/process2_bootstrap_stability_results.csv`, `outputs/bootstrap_stability.csv` |
| 9 | `plot_process2_stability_comparison.py` | `outputs/figures/process2_stability_direct_vs_bootstrap*.png/pdf` |

Each script includes inline comments and assertions for split sizes (train=320, dev=80) and the 13-feature contract.
