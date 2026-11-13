# Contributing to Code Security Scanner MCP

> **The code is not published here yet.** This guide describes how contributions work, so you know what to expect.
> Development setup, testing and code standards arrive with the code. To be notified, select **Watch → Custom →
> Releases** at the top of this page.

Contributions from everyone are welcome: you don't need to work at Thomson Reuters, be a maintainer or ask permission.
Bug reports, fixes, documentation, new scanner integrations and better remediation guidance all help. Small, focused
pull requests are the easiest to review. Participation in this project is governed by the
[Code of Conduct](CODE_OF_CONDUCT.md). Report vulnerabilities through the [security policy](SECURITY.md), not a public
issue.

## Ways to contribute

- **Ask a question or share an idea** in [Discussions](https://github.com/thomsonreuters/code-security-scanner-mcp/discussions):
  Q&A for questions, Ideas for features, scanners and integrations you would like to see.
- **Once the code is published:**
  - report a problem with the bug report form, or a wrong scanner result (false positive or false negative) with the
    "Wrong scanner result" form;
  - pick up an issue labelled `good first issue` or `help wanted`. You don't need to be assigned: comment that you're on
    it, so nobody duplicates the work, and open a pull request;
  - improve the docs: typos, unclear steps and missing examples can go straight to a pull request.

## Before you start

| Change                                                              | What to do first                                                                         |
| ------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| Typo, docs, small bug fix, test                                     | Nothing: open a pull request.                                                            |
| An issue labelled `good first issue` or `help wanted`               | Comment on the issue, then open a pull request.                                          |
| New feature, new scanner, new MCP tool, refactor, dependency change | Start an Idea in Discussions and agree the approach with a maintainer before writing the code. |

Agreeing first saves you from building something we can't merge: maintainers may close feature pull requests that have
no agreed issue, and will point you to one. [MAINTAINERS.md](MAINTAINERS.md) lists who to ask.

## Contribution agreement

This project uses the [Developer Certificate of Origin 1.1](https://developercertificate.org/) instead of a Contributor
License Agreement. Sign off every commit to certify that you have the right to submit the contribution under the
project's license:

```bash
git commit -s -m "feat(scanner): add example scanner"
```

The sign-off adds a `Signed-off-by` trailer using your configured Git name and email. Do not add another contributor's
sign-off.

## Commits and pull requests

Use [Conventional Commits](https://www.conventionalcommits.org/) with a concise description:

```text
feat(scanner): add PHP vulnerability support
fix: handle Snyk scan timeout
docs: clarify scanner configuration
```

Stage only the files that belong to the change rather than using `git add .`. A pull request should:

- explain what changed and why;
- link each issue it closes with `Closes #<number>`;
- include tests for behavior changes;
- update public documentation when needed;
- contain no unrelated refactoring; and
- pass all required checks.

Maintainers may ask for changes or close proposals that do not fit the project scope or security model.

## How pull requests are reviewed

- **Who reviews:** one of the [maintainers](MAINTAINERS.md). `.github/CODEOWNERS` requests the review automatically, so
  you don't need to tag anyone.
- **What is needed to merge:** an approving review from a maintainer and all CI checks passing. A maintainer's own pull
  request needs another maintainer's approval. Changes to CI, the release workflow or the telemetry event format need a
  second maintainer.
- **How it is merged:** squash-merged, with the pull request title as the commit message, so the title follows
  Conventional Commits.
- **Pull requests from forks** run the same CI. A maintainer approves the first run for a new contributor before it
  starts; after that it runs on every push.
- **If a review stalls,** comment on the pull request to ask for a reviewer. Maintainers triage every week.

## AI-assisted contributions

You may use AI tools. Say so in the pull request, review and understand every line you submit, and make sure the tests
cover it. You are responsible for the change, as with any other contribution. Pull requests opened by autonomous agents
with no person behind them will be closed.

## License and copyright

Contributions are licensed under the project's [MIT License](LICENSE). Project-owned files use the repository-level
copyright notice rather than individual file headers. Do not add per-file copyright headers unless a legal or technical
requirement calls for one, and preserve all existing third-party licence and attribution notices.

## Getting help

Ask in [Discussions](https://github.com/thomsonreuters/code-security-scanner-mcp/discussions) (Q&A). Ask contribution
questions in the relevant issue or pull request; a maintainer on triage will answer. For sensitive security reports,
follow [SECURITY.md](SECURITY.md).
