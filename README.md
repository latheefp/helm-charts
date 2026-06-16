# Helm Charts — latheefp

Public Helm chart repository hosted on GitHub Pages.

## Usage

```bash
helm repo add latheefp https://latheefp.github.io/helm-charts
helm repo update
```

## Available Charts

| Chart | Description | Install |
|---|---|---|
| secureshift | SecureShift Access Control Platform | `helm install myapp latheefp/secureshift` |

## Install a specific chart

```bash
# Latest
helm install myapp latheefp/secureshift

# Specific version
helm install myapp latheefp/secureshift --version 1.0.1

# With custom values
helm install myapp latheefp/secureshift \
  --set image.repository=latheefp/secureshift \
  --set db.password=mysecret \
  --set ingress.enabled=true \
  --set ingress.host=secureshift.example.com
```

## Repository Structure

```
helm-charts/
  index.yaml          ← Helm repo index (auto-generated, covers ALL charts)
  charts/             ← Packaged .tgz files for all apps
  .github/workflows/  ← GitHub Pages deployment
```

Charts are published automatically when a new version tag is pushed
to the corresponding source repository.
