# GitOps Demo Manifests

GitOps-style repository layout (Argo CD / Flux friendly):
- apps split by environment
- image tag updates as commits
- sync waves / basic health annotations

## Idea
Git is source of truth. Cluster controllers sync desired state from this repo.

```text
apps/
  web/
    base/
    overlays/dev|prod
bootstrap/
  argocd-app-of-apps.yaml
```
