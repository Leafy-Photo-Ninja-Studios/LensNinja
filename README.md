
# LensNinja – Sprint Drop (Backend-first)

This sprint packages a tested filtering/stats core you can use immediately in FastAPI.
Run `make demo` to see filtering, sorting, pagination, facets, and price bands working
over a realistic sample dataset.

## Layout
- `backend/filtering.py` — pure-Python filter/sort/paginate/facet logic (unit-tested here)
- `backend/stats_demo_runner.py` — executes the core logic and assertions
- `backend/main.py` — FastAPI routes using the same logic (requires deps)
- `backend/models.py` — Pydantic models (v2-style) for API typing
- `backend/data/scraped_json/sample_data.json` — fixture data
- `.github/workflows/ci.yml` — minimal CI running the demo assertions
- `Makefile` — shortcuts for dev

## Next
- Wire scraping to produce JSON matching `models.LensItem`
- Replace file I/O with a database or cached loader
- Add OpenCV image verification flow in a background task
