# Activating the data pipeline

The file `update-data.yml` in this folder is a GitHub Actions workflow that
auto-updates the site whenever `data/scholar.pdf` or `data/patents.xlsx` changes.

It could not be installed automatically because the access token used for
publishing lacks the `workflow` scope. To activate it (one time, ~30 seconds):

1. In this repo on github.com, click **Add file → Create new file**
2. Name it exactly:  .github/workflows/update-data.yml
3. Paste the contents of `automation/update-data.yml`
4. Commit to main

From then on: replace data/scholar.pdf with a fresh "print to PDF" of the
Google Scholar profile, or edit data/patents.xlsx, commit — and the site
numbers/patent rows update themselves within a minute.
