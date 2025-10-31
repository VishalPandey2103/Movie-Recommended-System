# movie_recommend

Simple Streamlit-based movie recommender that uses precomputed similarity data and TheMovieDB to fetch posters.

## What this repo contains

- `app.py` - Streamlit app that shows recommendations for a selected movie.
- `movies.pkl` - Pickled movie metadata used by the app.
- `similarity.pkl.gz` - Gzipped pickle containing the similarity matrix.
- `requirements.txt` - Python dependencies.

> Note: The dataset files are large (several MB). Keep them in the same directory as `app.py`.

## Quick setup (Windows, PowerShell)

1. Create and activate a virtual environment (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Upgrade pip and install dependencies:

```powershell
python -m pip install --upgrade pip setuptools wheel
pip install -r requirements.txt
```

3. Run the Streamlit app from the project directory so relative data files are resolved:

```powershell
streamlit run app.py --server.port 8501 --server.headless true
```

4. Open the URL printed by Streamlit (usually http://localhost:8501) in your browser.

## Notes & troubleshooting

- If you see a `FileNotFoundError` for `similarity.pkl.gz` or `movies.pkl`, ensure those files are present in the same folder as `app.py` and not moved.
- The app uses TheMovieDB API (a public API key is embedded in the code). If poster fetching fails, the app will show a placeholder image.
- If Streamlit reports port-in-use, change `--server.port` to another port (e.g., 8502).

## License

This project is provided under the MIT License — see `LICENSE` for details.



# Movie-Recommended-System
