# Contributing to Burnt Labs

Thanks for your interest in contributing. This is the organization-wide default
guide. Individual repositories may publish their own `CONTRIBUTING.md`, which
takes precedence, and many carry an `AGENTS.md` with repository-specific
conventions — read it before you start.

## Before You Start

- **Search first.** Check existing issues and pull requests before opening a new
  one.
- **Discuss large changes.** For anything substantial, open an issue describing
  the problem before writing code. It is cheaper to align on approach than to
  rework a finished branch.
- **Security issues do not belong here.** See [SECURITY.md](SECURITY.md) and
  report privately to [security@burnt.com](mailto:security@burnt.com).

## Requirements Enforced on Every Repository

Our organization rulesets apply to the default branch of every repository. These
are enforced by GitHub, not by reviewer discretion, so a branch that does not
meet them cannot merge.

- **Commits must be signed and verified.** Unsigned commits are rejected. See
  [Signing commits](https://docs.github.com/en/authentication/managing-commit-signature-verification/signing-commits)
  to set up GPG, SSH, or S/MIME signing.
- **Changes land through a pull request.** Direct pushes to the default branch
  are blocked.
- **Code owner review is required** where a `CODEOWNERS` file applies.
- **Force pushes and branch deletion are blocked** on protected branches.
- **Approvals are dismissed when new commits are pushed**, so re-request review
  after changes.
- Automated review runs on pull requests alongside human review.

A few repositories require additional approvals — `xion` and `xion.js` each
require one approving review beyond the code owner baseline.

## Pull Requests

1. Fork or branch from the repository's default branch.
2. Make your change, keeping commits focused and messages descriptive.
3. Ensure the repository's own checks pass locally — lint, type-check, tests,
   and build, as applicable.
4. Open the pull request and fill in the template. Explain **what** changed,
   **why**, and the **impact** on users or the system.
5. Link related issues (for example `Closes #123`).
6. Respond to review feedback; re-request review once you have pushed updates.

Keep pull requests as small as they can reasonably be. A large diff that mixes
refactoring with behavior change is difficult to review and difficult to revert.

## Style

Follow the conventions already present in the code you are editing — matching
the surrounding naming, structure, and comment density matters more than any
global rule. Where a repository ships formatter or linter configuration, that
configuration is the authority.

## License

Unless a repository states otherwise, contributions are made under that
repository's license. Check the `LICENSE` file in the repository you are
contributing to; there is no organization-wide default license.
