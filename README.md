# Jupyter setup with `uv` + `requirements.txt`

This project uses **[uv](https://docs.astral.sh/uv/)** to create a virtual environment from an existing `requirements.txt` and expose it to Jupyter notebooks via an IPython kernel.

> Replace `<PATH/TO/requirements.txt>` below with the actual path (e.g. `env/requirements.txt`).

---

## Prerequisites

- **uv** installed (macOS/Linux/Windows).  
  - macOS/Linux: `curl -LsSf https://astral.sh/uv/install.sh | sh`  
  - Windows (PowerShell): `irm https://astral.sh/uv/install.ps1 | iex`

---

## Quick start

```bash
# 1) Create a local virtual environment (".venv" by default)
uv venv

# 2) Install everything from your requirements file
uv pip install -r <PATH/TO/requirements.txt>

# 3) Add this environment as a Jupyter kernel
uv pip install ipykernel
python -m ipykernel install --user --name project-venv --display-name "Python (project-venv)"

# 4) Launch Jupyter (pick the "Python (project-venv)" kernel)
uvx jupyter lab    # or: jupyter lab

