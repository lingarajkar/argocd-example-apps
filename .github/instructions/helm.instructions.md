---
applyTo: "**/helm-*/**/*, **/blue-green/**/*"
---

### Helm Chart Custom Review Rules

Apply these guidelines exclusively when changes are made to Helm charts, dependencies, or values files.

### 1. Chart Best Practices

- **Explicit Dependencies:** If `Chart.yaml` imports upstream charts (like `helm-dependency`), verify that the `version` and `repository` fields are explicitly locked down.
- **Values Validation:** Ensure variables introduced in `values.yaml` have accompanying placeholders or explanations in the chart's documentation blocks.
- **Helm Hooks:** When reviewing directories matching `helm-hooks`, check that `helm.sh/hook` annotations match valid lifecycle hooks (e.g., `pre-install`, `post-sync`).
