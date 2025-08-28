# Engine Sensor Analytics

Synthetic engine dataset with Python EDA workflow and Excel reporting.  
This project demonstrates **end-to-end data wrangling, exploratory analysis, correlation mapping, and automated reporting** using Python and a realistic (but public-safe) engine dataset.

---

## Repository Contents
- **Engine_Sensor_Analytics.ipynb** — main notebook: load → clean → explore → plot → export.
- **synthetic_engine_log.csv** — synthetic dataset scaled to heavy-duty 6-cylinder ranges.
- **out/engine_analysis_export.xlsx** — consolidated Excel report (tables + plots).
- **out/samples/** — a handful of preview figures.
- **requirements.txt** — Python dependencies (pandas, numpy, matplotlib, xlsxwriter).
- **LICENSE** — MIT (open for reuse).
- **out/engine_analysis_export_sample.xlsx** — trimmed demo version of the full Excel report.  
  The complete report (~32 MB, 200+ plots) is too large for GitHub’s web upload limit,  
  but can be reproduced by running the notebook locally.

---

## How to Run
Clone the repo and install dependencies:
```bash
git clone https://github.com/RomiLoni/Engine-Sensor-Analytics.git
cd Engine-Sensor-Analytics
pip install -r requirements.txt
```
## Then open the notebook:
Running all cells will:

Load the dataset (synthetic_engine_log_scaled.csv).

Clean and coerce numeric fields.

Generate distributions, boxplots, correlations, and scatterplots.

Export everything into /out/engine_analysis_export.xlsx.
## Sample Insights

Torque ↔ CO₂: strong positive correlation (r ≈ 0.93). Higher load → more fuel burnt → higher CO₂ output.

MAP ↔ Exhaust T: very strong (r ≈ 0.97). Boost pressure raises exhaust temperature.

Lambda ↔ NOx: negative correlation (r ≈ –0.6). Leaner mixtures reduce thermal NOx formation.

Noise checks: CO vs coolant and HC vs MAT showed ~0 correlation, confirming expected independence.

These trends match physical intuition, showing the workflow can distinguish meaningful relationships from noise.
## Notes

Data is synthetic (not experimental) and safe to share.

Engine scaling: 6-cyl, ~200–800 Nm torque, 25–55 kg/h fuel flow, 700–1800 kg/h air flow.

The Excel export bundles 18 tables and 200+ plots into a single interactive file.
License

## MIT License — feel free to use, adapt, and build on this work.
