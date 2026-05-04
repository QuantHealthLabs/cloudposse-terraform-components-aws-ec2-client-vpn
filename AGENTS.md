# Forked Cloud Posse Terraform Component

- Scope changes to this component. `src/` is the Terraform source.
- Keep patches minimal and upstream-friendly.
- Update `README.yaml` for input/output/docs changes, then regenerate docs with `atmos docs generate readme` and, when needed,
  `atmos docs generate readme-simple`.
- Format with `terraform fmt -recursive`; run TFLint/pre-commit only when the local config exists and the task warrants it.
- `atmos test run` uses Terratest and deploys real AWS resources; run it only when needed or explicitly requested.
- Global AWS resources and service quotas belong in `us-east-1`/`gbl` when applicable.
