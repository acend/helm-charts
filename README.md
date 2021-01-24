# Acend Helm Charts

This repository contains the acend helm charts.
The charts are published as helm repository using github-pages on the main branch from the `docs` directory.

## Development

Use the Chart Version

## Package Charts and Deploy

First we want the charts to be well linted:

```bash
helm lint ./charts/*
```

Verify the output and fix errors.

Then let's package the helm charts and move the tgz files into the docs folder

```bash
helm package ./charts/* && mv *.tgz docs/
```

Finally let's create the helm repo index

```bash
helm repo index docs --url https://acend.github.io/helm-charts/ 
```
