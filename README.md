# GitOps manifests

Push this `gitops/` tree (with the rest of the repo, or at least this path) to the GitHub repository configured in Terraform (`git_repo_url`).

Argo CD Application `demo-nginx` syncs:

- **path:** `gitops/apps/demo-nginx`
- **destination namespace:** `demo-nginx`

Do not `kubectl apply` these manifests for the happy path — let Argo CD reconcile from Git.