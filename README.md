# kubeconform-ci

> Validate every manifest against the right schema on every PR.

**Status:** 🚧 In development

## Overview

Drop-in GitHub Action wrapping kubeconform for Kubernetes manifest validation.

## Features

- Runs kubeconform with CRD schema support
- Auto-detects target k8s version or set explicitly
- Handles Helm-rendered and Kustomize output
- Summary annotations on PR
- Configurable ignore paths

## Stack

Composite GitHub Action + kubeconform + yq.

## Usage

```yaml
- uses: cybercapybara/kubeconform-ci@v1
  with:
    kubernetes-version: '1.30'
    dirs: manifests/
```

## License

MIT
