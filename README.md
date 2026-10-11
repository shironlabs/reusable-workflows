# Reusable Workflows

Reusable GitHub Actions workflows for shironlabs application repositories.

This is a public repository. It must contain workflow definitions and public
documentation only; credentials and other sensitive values must be supplied by
the calling repository as GitHub Actions secrets.

`release-pr.yml` creates Release PRs with release-please. `container-release.yml`
builds and pushes images from `v*` tags. `renovate-approver.yml` approves PRs only
when their author is Renovate. The caller supplies registry credentials and a
newline-separated `name|dockerfile|context` image list.

For `release-pr.yml`, callers may provide `MELISIA_BOT_APP_ID` and
`MELISIA_BOT_APP_PRIVATE_KEY` to mint a short-lived GitHub App token with
contents and pull-request write access. Existing callers may continue to use
`RELEASE_PLEASE_TOKEN` instead. The App must be installed on the calling
repository with those permissions.
