# Kubernetes Scripts Collection

## Deploy-Helm

A deployment script of helm-based releases.

- RBAC Support (one tiller per namespace)
- Namespace Admin or Cluster Admin
- Automatic repository installation for CI

### Deploy Helm Installation

```bash
curl -L -o /usr/local/bin/deploy-helm https://raw.githubusercontent.com/PhilippHeuer/kubernetes-deployment-scripts/master/scripts/deploy-helm
or
curl -L -o /usr/local/bin/deploy-helm https://raw.githubusercontent.com/PhilippHeuer/kubernetes-deployment-scripts/v${VERSION}/scripts/deploy-helm
```

## STI (Source To Image) Build

A simple S2I Build Script for use in CI.

### STI Installation

```bash
curl -L -o /usr/local/bin/sti-build https://raw.githubusercontent.com/PhilippHeuer/kubernetes-deployment-scripts/master/scripts/sti-build
or
curl -L -o /usr/local/bin/sti-build https://raw.githubusercontent.com/PhilippHeuer/kubernetes-deployment-scripts/v${VERSION}/scripts/sti-build
```

### STI Configuration

Example `.s2i.yml`

```yml
# S2I Configuration
s2i:
  # Builder
  builder:
    image: s2i-builder:latest
  # Runtime
  runtime:
    image: s2i-runtime:latest
    source: /tmp
    target: .
```
