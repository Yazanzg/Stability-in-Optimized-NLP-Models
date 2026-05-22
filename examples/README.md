# Example data (no real participants)

These files show the **expected column names and file layout** for running the pipeline without uploading PROCESS-2.

| File | Purpose |
|------|---------|
| `example_master_table_schema.csv` | Column schema for `process2_ctd_binary_master.csv` |
| `dummy_ctd.txt` | Minimal Cookie Theft Description text for path checks |

To run the full thesis pipeline you need the real PROCESS-2 cohort (400 participants) under `PROCESS-2/` with local paths in your master CSV. The committed `outputs/process2_ctd_binary_master.csv` documents the thesis run but points to paths on the author's machine; rebuild paths after cloning.

```powershell
# Example: test preprocessing on dummy text only (no models)
python -c "from src.preprocessing import clean_transcript; print(clean_transcript(open('examples/dummy_ctd.txt').read()))"
```
