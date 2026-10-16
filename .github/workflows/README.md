# CI/CD workflow

[`ci-cd.yml`](ci-cd.yml) is the whole pipeline: **"TaskFlow CI/CD + DevSecOps"**.

It runs on every push and pull request to `main`, and on manual
`workflow_dispatch` runs. Jobs: lint-test, validate-iac, sast, sca,
secret-scan, docker-build, image-scan, security-gate, push-images (main only)
and deploy (kind + Helm). See the CI/CD section of the root
[README](../../README.md) for what each job checks.
