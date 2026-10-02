# Changelog

## Unreleased

- Added `SUBMISSION_READINESS.md` recording validation, runtime load, and invocation results. No change to plugin behavior.
- Added a privacy policy link to the manifest and README.
- Added `displayName` to the manifest and `SUBMISSION.md` for the directory submission. Switched the README icon to Markdown image syntax. No change to plugin behavior.
- Added the plugin icon files, an icon field in the manifest for the Anthropic directory listing, and a README icon section. No change to plugin behavior.

## 1.0.0 — Initial public release

- Initial public release of Small Business Operator as a standalone plugin repository.
- Added the `small-business-operator` plugin with the `business-operating-rhythm` skill covering daily operator briefs, weekly operating reviews, monthly business reviews, follow-up workflow, and decision briefs.
- Organizes work around eight lenses: sales, customers, cash, operations, people, vendors, commitments, and decisions.
- Includes evidence rules against fabricated metrics and explicit authorization boundaries for payments, contracts, personnel actions, external communications, and legal, tax, or accounting determinations.
- Added a GitHub Actions workflow that validates the manifest, semantic version, skill frontmatter, and required documentation.

### Verification

Package validation runs in GitHub Actions. This release has not been installed or exercised in a user's Claude runtime by its authors; smoke-test the plugin in your own Claude environment after installing it.
