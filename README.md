# Small Business Operator

**A free Claude workflow plugin by [Revuity Systems](https://revuitysystems.com).**

![Small Business Operator plugin icon](assets/icon-128.png)

A free Claude plugin that helps a small-business owner run the operating rhythm of the company. It organizes scattered business activity into a practical operating view across sales, customers, cash, operations, people, vendors, commitments, and decisions.

- Plugin name: `small-business-operator`
- Skill: `/small-business-operator:business-operating-rhythm`
- Version: 1.0.0
- License: MIT

## Plugin icon

The plugin icon ships in the assets folder in 512, 256, and 128 pixel versions. The manifest references it with the icon field, which Anthropic's directory reads for the plugin listing and Claude Code ignores at load time.

## Good for

- Daily attention lists: what changed and what needs you today
- Weekly operating reviews
- Monthly business reviews
- Follow-up plans for open items
- Decision briefs with options and tradeoffs
- Owner-ready checklists

## How it works

Operate from eight lenses: Sales, Customers, Cash, Operations, People, Vendors, Commitments, and Decisions. Use the plugin with business information you provide or connect. It distinguishes observed facts, calculated metrics, assumptions, and recommendations, does not fabricate missing metrics, balances, deadlines, or customer status, and says when data is missing or stale. Output is meant to be a short executable operating view, not a long narrative.

## Example requests

Once the plugin is loaded, ask in plain language or invoke the skill directly with `/small-business-operator:business-operating-rhythm`.

- "Give me a daily operator brief from these notes: what changed, what is overdue, and the top three actions today."
- "Run a weekly operating review from this pipeline export and AR list."
- "Build a decision brief for whether to take on this new vendor contract, with options and a labeled recommendation."
- "Turn this pile of open follow-ups into a list with owners, next actions, and due dates."

You supply the information, either by pasting it in or through tools you have already connected to Claude. The plugin does not collect data of its own, does not call any Revuity service, and has no executable code.

## Authority and safety boundaries

The plugin drafts and recommends by default. It does not make payments, transfers, refunds, or credits, change banking details, execute contracts, make commercial commitments, take hiring, firing, compensation, or disciplinary actions, send consequential external communications, make legal, tax, accounting, or insurance determinations, delete records, or change access and security settings. Each of those requires explicit human authorization.

When something is missing, stale, or in conflict, the plugin is written to stop and say so rather than guess.

## Data handling

Share only the business information a task needs. Avoid pasting passwords, full account numbers, or other secrets into prompts. Your own privacy, retention, and records obligations still apply to anything you share with Claude.

## Install

This repository is a single Claude plugin with its manifest at `.claude-plugin/plugin.json` and its skill at `skills/business-operating-rhythm/SKILL.md`.

To try it locally, clone the repository and start Claude Code with the plugin directory:

```bash
git clone https://github.com/revuitysystems/revuity-small-business-operator.git
claude --plugin-dir ./revuity-small-business-operator
```

Then run `/reload-plugins` and confirm `/small-business-operator:business-operating-rhythm` appears. To check the package without running it, use `claude plugin validate ./revuity-small-business-operator`.

## Validation

A GitHub Actions workflow in this repository checks the manifest, semantic version, skill frontmatter, and required documentation on every push and pull request. See `.github/workflows/validate.yml`. Passing validation shows the package is well formed. It does not replace testing the plugin in your own Claude environment against your own policies.

## Built by Revuity Systems

Revuity Systems is an Operations Systems company. These public workflow plugins are free operating tools designed to make real work easier while demonstrating how Revuity thinks about roles, workflows, responsibility, authority, exceptions, outcomes, and operating cadence.

When an organization later needs the workflow adapted to its own systems, policies, data, approvals, integrations, or operating model, Revuity may help design or build that larger system. You do not need to talk to anyone to use this plugin.

More at [revuitysystems.com](https://revuitysystems.com). Questions or security concerns: info@revuitysystems.com.

## Privacy

This plugin does not collect or store data itself. Revuity's privacy policy is at [revuitysystems.com/privacy](https://revuitysystems.com/privacy).

## License

MIT. See [LICENSE](LICENSE).
