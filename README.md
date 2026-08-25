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
