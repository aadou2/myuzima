# Single-page group dashboard (separate proposal)

This is a new proposed `app.py` and data folder. It does **not** modify the existing group repository.

## Run

```bash
python3 -m pip install -r requirements.txt
python3 -m streamlit run app.py
```

## What is included
- One page, neighborhood/year filters, shooting map, hospital markers, trends, regression, hypothetical scenarios, hospital finances.
- Stroger/Cook County and Rush may have identical rounded coordinates in supplied hospital data; hover at their shared location lists both.
- Pooled negative-binomial GLM uses population offset, poverty and unemployment, and year indicators. Dispersion alpha=1 is assumed, not estimated. Exploratory only; validate source definitions, model fit and out-of-sample accuracy before client use.
- No new 2008–2012 Census file merged into current-year variables because its time period differs.
- Hospital finances are hospital-wide, not gunshot-specific. Travel times are estimates, not measured EMS response.
