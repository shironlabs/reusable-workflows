# Reusable Workflows

Reusable GitHub Actions workflows for shironlabs application repositories.

This is a public repository. It must contain workflow definitions and public
documentation only; credentials and other sensitive values must be supplied by
the calling repository as GitHub Actions secrets.

`release-pr.yml` creates Release PRs with release-please. `container-release.yml`
builds and pushes images from `v*` tags. The caller supplies registry credentials
and a newline-separated `name|dockerfile|context` image list.
