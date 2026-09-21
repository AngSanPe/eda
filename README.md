# Letterboxd Reviews EDA

Exploratory data analysis of `resenas_completo.jsonl` — 710K Letterboxd film
reviews (rating, text, likes, language, spoiler/rewatch flags, etc.).

## Run with Docker (recommended for sharing)

```bash
docker compose up --build
```

Then open http://localhost:8888 and run `eda_resenas.ipynb` (no token/password
required). The dataset (`resenas_completo.jsonl`) and notebook are mounted as
volumes, not baked into the image, so the image stays small and your notebook
edits persist to disk.

To hand this off to someone else, share this folder (Dockerfile,
docker-compose.yml, requirements.txt, eda_resenas.ipynb, README.md) plus the
`resenas_completo.jsonl` data file — they just run the command above.

## Run locally without Docker

```bash
pip install -r requirements.txt
jupyter notebook eda_resenas.ipynb
```

The notebook auto-detects `resenas_completo.jsonl` in the working directory,
or reads the path from the `DATA_PATH` environment variable.
