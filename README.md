# Gluu Open Banking on RHEL 9 documentation

This directory is a self-contained MkDocs project containing the reviewed RHEL 9 installation guide.

## Preview locally

```bash
python3 -m venv .venv
. .venv/bin/activate
python -m pip install -r requirements.txt
mkdocs serve
```

Open `http://127.0.0.1:8000/`.

## Build the static site

```bash
mkdocs build --strict
```

The generated site is written to `site/`.

## Publish with GitHub Pages

1. Copy the complete project—including `.github/workflows/deploy.yml`—to the root of a GitHub repository.
2. Commit and push to the `main` branch.
3. In **Settings → Pages**, select **Deploy from a branch**, then select the `gh-pages` branch and `/ (root)` after the workflow creates it.

The included workflow validates the MkDocs build and publishes the generated site to `gh-pages` on every push to `main`. The workflow can also be started manually from the Actions tab.
