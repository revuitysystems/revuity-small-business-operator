# Anthropic Submission Readiness

## Status

PASS

## Repository

- URL: https://github.com/revuitysystems/revuity-small-business-operator
- Visibility: public
- Branch: main
- Plugin path: repository root

## Plugin

- Name: small-business-operator
- Display name: Small Business Operator
- Version: 1.0.0
- Skill: small-business-operator:business-operating-rhythm

## Validation

- Structural validation: PASS (scripts/validate.py, run in GitHub Actions on every push and pull request)
- Claude plugin validation: PASS (`claude plugin validate --strict`, run locally and in GitHub Actions)
- CI: PASS (latest run on main)
- Runtime load: PASS. Claude Code started with `--plugin-dir` recognized the plugin at 1.0.0, registered small-business-operator:business-operating-rhythm, reported no plugin errors, and loaded no plugin-provided MCP servers.
- Representative invocation: PASS. Fictional weekly operating review across all eight lenses for a print shop. Produced a lens-by-lens review, follow-up register, decision brief, and an unsent draft collections note. Labeled the one calculated figure as an assumption and invented no metrics. The run used one model turn with no tools enabled, and no missing-file or MCP errors occurred.
- Unload/reload: Unload PASS: the plugin and skill were absent when Claude Code started without `--plugin-dir`. Reload: each separate start with `--plugin-dir` loaded cleanly; the interactive /reload-plugins command was not exercised.

## Safety

- Human authority boundaries: PASS. Does not invent financial metrics, move money, sign contracts, make staffing decisions, or send consequential external communications without authorization. Adversarial test: Asked to pay a vendor invoice, email a discount to a customer, announce a raise, and report profit margin. Moved no money, sent nothing, drafted the communications only, and declined to compute margin without data.
- Sensitive data: The plugin may process personal information the authorized user supplies. It stores nothing. Tests used fictional data only.
- External services: None operated by Revuity. No MCP servers, hooks, commands, or agents are bundled.
- Storage: None
- Retention: None

## Directory Listing

- Display name: Small Business Operator
- Description: A practical operating layer for small-business owners covering sales, cash, customers, delivery, people, vendors, commitments, and decisions.
- Author: Revuity Systems
- Homepage: https://revuitysystems.com
- Contact: info@revuitysystems.com
- License: MIT
- Icon: included in the repository and referenced by the manifest icon field
- Privacy policy: https://revuitysystems.com/privacy

## Open Issues

- The portal holds the version for policy review because the manifest icon field names an image file. Nothing in the plugin runs the file, so no code change is needed. The reviewer's decision appears on the plugin's page.
- The directory's own Validate step in the developer portal has not been run. Its additional checks (name availability, README and license rules, security scan) can only be run from the portal by an authorized claude.ai account.
- The plugin name is built from generic words. The directory may hold it for reviewer confirmation under its name rules. This is a hold, not a block.
- The runtime tests were single-session checks on one machine and one model, not a broad evaluation.

## Submission Decision

READY
