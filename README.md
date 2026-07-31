# burnt-labs/.github

Organization-wide **default community health files** for every repository in the
`burnt-labs` organization, plus the org profile page.

When a repository does not contain one of the files below, GitHub falls back to
the copy here and displays it as if it lived in that repository. When a
repository does contain its own copy, that copy wins — the default is never
merged with it.

This repository **must remain public** for the defaults to apply
organization-wide.

## Contents

| Path                                     | Applies to                                                        |
| ---------------------------------------- | ----------------------------------------------------------------- |
| `SECURITY.md`                            | Every repo without its own security policy                        |
| `CONTRIBUTING.md`                        | Every repo without its own contributing guide                     |
| `CODE_OF_CONDUCT.md`                     | Every repo without its own code of conduct                        |
| `SUPPORT.md`                             | Every repo without its own support doc                            |
| `.github/PULL_REQUEST_TEMPLATE.md`       | Every repo without its own PR template                            |
| `.github/ISSUE_TEMPLATE/`                | Every repo without its own issue templates                        |
| `.github/FUNDING.yml`                    | Every repo without its own funding config (all entries commented) |
| `profile/README.md`                      | The [organization profile page](https://github.com/burnt-labs)    |
| `.github/CODEOWNERS`                     | **This repository only** — not inherited                          |

## What Is *Not* Inherited

This is the most common point of confusion. GitHub's default-file mechanism
covers a fixed list, and these are not on it:

- **Workflows.** `.github/workflows/` here runs only for *this* repository. It
  does not execute in any other repo. Central CI lives in
  [`burnt-labs/github-workflows`](https://github.com/burnt-labs/github-workflows)
  and is consumed either by explicit `uses:` reference or by an organization
  ruleset required workflow.
- **`CODEOWNERS`.** Each repository needs its own.
- **`LICENSE`.** GitHub does not support a default license file; every
  repository must carry its own.
- **Repository settings**, branch protection, and rulesets. Those are managed as
  [organization rulesets](https://github.com/organizations/burnt-labs/settings/rules)
  in org settings, not as files in any repository.

## Changing These Files

A change here takes effect immediately across every repository that does not
override the file, with no per-repo pull request and no deploy step. Treat edits
to `SECURITY.md` and `CODE_OF_CONDUCT.md` as policy changes rather than
documentation tweaks — both make public commitments on behalf of the
organization.

`.github/CODEOWNERS` routes review to `@burnt-labs/burnt-devops`.

## Overriding a Default

Add the file to the repository that needs different content. No configuration or
opt-out is required — the presence of the file is the override. Repositories
that already do this include `burnt-labs/xion`, which ships a chain-specific
`SECURITY.md`.

## References

- [Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [Customizing your organization's profile](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile)
