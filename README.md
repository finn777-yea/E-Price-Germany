# E-Price-Germany
Leveraging machine learning methods to predict future electricity price in hourly resolution⚡

## Setup

This project uses [uv](https://docs.astral.sh/uv/) for environment and dependency management.

### Prerequisites

Install `uv` if you don't have it already:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### Install dependencies

```bash
uv sync
```

This creates a `.venv` virtual environment and installs all required packages automatically.

### Activate the environment

```bash
source .venv/bin/activate
```

### Run Jupyter notebooks

With the environment activated:

```bash
jupyter lab
```

Or without activating, using `uv run`:

```bash
uv run jupyter lab
```

## Clean notebook commits

This project uses [nbstripout](https://github.com/kynan/nbstripout) to automatically strip cell outputs and execution counts from notebooks before each commit, keeping diffs readable.

After cloning, run once to install the git filter:

```bash
uv run nbstripout --install
git config filter.nbstripout.extrakeys "metadata.kernelspec.display_name metadata.language_info.version"
```

This registers the filter in your local `.git/config`. The `.gitattributes` file already tells git which files to apply it to, so no further configuration is needed.