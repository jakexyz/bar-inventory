# Bar Inventory (Persistent + What to Order)

- Uses **Postgres** via `DATABASE_URL` so data persists across Render deploys.
- Seeds from `bar_inventory_app/bar_inventory_import.csv` **only if DB empty** (disable with `SKIP_SEED=1`).
- "What to Order" page groups by vendor → spirit and shows needed cases; Excel export optional.

## Local run
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
export FLASK_APP=bar_inventory_app.app
flask --app bar_inventory_app.app run
