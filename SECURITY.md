# Security Policy

## Supported versions

Security updates are provided for the latest release. Fixes are developed on the default branch and included in the next
release; older releases are not supported.

## Reporting a vulnerability

Do not open a public issue for a suspected vulnerability. Report it privately through GitHub's private vulnerability
reporting on this repository:
[Report a vulnerability](https://github.com/thomsonreuters/code-security-scanner-mcp/security/advisories/new). Include:

- a description of the issue and its potential impact;
- the affected version or commit;
- reproduction steps or a proof of concept; and
- any suggested mitigation, if known.

Do not include credentials, personal data, proprietary source code, or other unnecessary sensitive material. The project
security maintainers will acknowledge the report, assess it, and keep the reporter informed of progress until the report
is resolved or a coordinated-disclosure plan is agreed. We do not publish target response times.

Report vulnerabilities in projects scanned by Code Security Scanner MCP to those projects' maintainers. Contact us when
the issue is in Code Security Scanner MCP itself, including its handling of paths, scanner credentials, scan results, or
MCP requests.

## Security model

Code Security Scanner MCP runs with the permissions of its host process. It reads user-selected project directories,
invokes configured scanner command-line tools, and exposes scan results to the connected MCP client. It is not a
sandbox: any path accessible to the process may be scanned, and findings may contain file paths or source snippets.

Scanner services, MCP clients, and AI providers are separate trust boundaries. They may transmit source code, dependency
metadata, or findings according to their own configuration and terms. Review those services before scanning sensitive
code, use narrowly scoped credentials, and do not expose the SSE transport to untrusted networks or clients.

The built-in Snyk integrations invoke the Snyk CLI with argument lists rather than a shell. Authentication material is
read from existing Snyk CLI configuration, environment variables, or Code Security Scanner MCP configuration and passed
to the scanner process. Do not commit tokens or other credentials to the repository.

## Disclosure process

We will validate the report, agree on communication and disclosure timing with the reporter, and credit the reporter
when requested and appropriate. Please allow time for a fix and affected-user communication before publishing details.
