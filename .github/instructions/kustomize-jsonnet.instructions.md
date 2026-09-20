---
applyTo: "**/kustomize-*/**/*, **/jsonnet-*/**/*"
---

### Kustomize & Jsonnet Architecture Rules

Apply these guidelines when patches, targets, or Jsonnet templates are modified.

### 1. Kustomize Safeguards

- **Resource Paths:** Ensure all entries under the `resources:` list in `kustomization.yaml` point to existing paths or valid relative files.
- **Target Overrides:** Flag catch-all patches that modify resources across the entire namespace without targeted `target` filters.

### 2. Jsonnet Parameters

- **Top-Level Arguments:** For variations matching `jsonnet-guestbook-tla`, ensure top-level parameters are safely handled with clean default values if an argument isn't provided by the caller.
