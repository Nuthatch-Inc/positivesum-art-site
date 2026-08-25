# Positive Sum Art Site Deployment

This repository deploys the public Positive Sum Art website to GitHub Pages.
The website source remains in
[`Nuthatch-Inc/nuthatch-desktop`](https://github.com/Nuthatch-Inc/nuthatch-desktop).
No application source or generated website files are duplicated here.

## Deployment

`source-ref.txt` contains the exact `nuthatch-desktop` commit used for the
deployment. The GitHub Pages workflow checks out that commit, builds the
public-only Positive Sum artifact, and deploys `dist/positivesum`.

During preview, the website is built for this project URL:

<https://nuthatch-inc.github.io/positivesum-art-site/>

The custom `positivesum.art` domain is intentionally not configured yet.
Before moving the domain, the deployment build must change from the project
base `/positivesum-art-site/` to the root base `/`.

## Publishing a Website Update

1. Edit and test the website in `Nuthatch-Inc/nuthatch-desktop`.
2. Commit and push the source changes.
3. Copy the full 40-character source commit SHA.
4. Replace the value in this repository's `source-ref.txt` with that SHA.
5. Commit and push the `source-ref.txt` change.
6. Open this repository's **Actions** page and confirm that **Deploy Positive
   Sum Art preview** completes successfully.
7. Test the deployed website, including any page or interaction changed by the
   source commit.

The deployment workflow installs dependencies, builds the public-only site,
checks the artifact, and publishes it. Generated website files are never
committed to this repository.

The private source repository is accessed through a repository-scoped,
read-only deploy key. Its private half is stored only in the encrypted Actions
secret `NUTHATCH_SOURCE_DEPLOY_KEY`.
