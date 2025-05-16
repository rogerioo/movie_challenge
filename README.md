# 🎬 Movie Metadata Data Engineering Challenge

This project demonstrates a complete data engineering pipeline built to process and analyze a movie metadata dataset. The pipeline performs loading, cleaning, enrichment, standardization, flagging, and actor collaboration analysis using Python and modern tooling.

---

## 🚀 Features

- ✅ Data cleaning and deduplication
- 🔗 Enrichment using IMDb public datasets
- 🧼 Data standardization with quality flags
- 🎭 Actor collaboration and performance analysis
- 📊 Directed and undirected graph visualizations
- 🧩 Modular function-based design, Airflow-compatible
- ⚙️ Uses `uv` for modern dependency and environment management

---

## 🗃️ Dataset Sources

- Main movie dataset: `movie_metadata.csv`
- Enrichment datasets are downloaded directly from [IMDb Datasets](https://datasets.imdbws.com/):
  - `title.basics.tsv.gz`
  - `title.principals.tsv.gz`
  - `name.basics.tsv.gz`

Download automation is included in the notebook.

---

## 🛠️ Setup

> This project uses [uv](https://github.com/astral-sh/uv) for dependency management and Python environment handling.

### 1. Clone and enter the repo

```bash
git clone https://github.com/rogerioo/movie_challenge.git
cd movie_challenge
```

### 2. Install dependencies with `uv`

> You should use a virtual environment for this step

```bash
pip install uv
uv sync --active
```

### 3. Start Jupyter Notebook

> It may require to restart your current shell section and activate your virtual environment again to call `jupyter`

```bash
jupyter notebook
```

---

## 📓 Project Structure

```plaintext
├── challenge.ipynb            # Main analysis notebook
├── enrichments/               # IMDb TSV files (auto-downloaded)
├── pyproject.toml             # Project dependencies
├── README.md
└── data/                      # Datasets (optional)
```

---

## 📊 Stage Overview

| Stage | Description |
|-------|-------------|
| 1–2   | Data loading, type casting, deduplication |
| 3–5   | IMDb enrichment and role metadata |
| 6     | Data transformation, normalization, and quality flags |
| 7     | Pipeline design using modular functions |
| 8     | Actor collaboration analysis (graphs, top pairs, clusters) |

---

## 📦 Key Dependencies

- `pandas`, `seaborn`, `networkx`, `scipy`, `fastparquet`
- Python 3.13+ required (see `.toml`)

---

## 📄 License

MIT License (or specify if different)

---

## 🤝 Acknowledgments

This project uses IMDb data which is provided by IMDb and available for non-commercial use at [IMDb Datasets](https://www.imdb.com/interfaces/).
