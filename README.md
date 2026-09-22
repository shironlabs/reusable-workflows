# Reusable Workflows

Reusable GitHub Actions workflows for shironlabs application repositories.

`release-pr.yml` creates Release PRs with release-please. `container-release.yml`
builds and pushes images from `v*` tags. The caller supplies registry credentials
and a newline-separated `name|dockerfile|context` image list.
