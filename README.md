# Awesome Ballet [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of templates, integrations, guides and examples for [Ballet](https://ballet.dev), the agent operations platform for building, running and observing deterministic workflows.

## Contents

- [Template collections](#template-collections)
- [All templates](#all-templates)
- [Concepts](#concepts)
- [Contributing](#contributing)

## Template collections

- [ballet-templates](https://github.com/brainfish-ai/ballet-templates): every official template, with one-click import.
- [ballet-support-playbooks](https://github.com/brainfish-ai/ballet-support-playbooks): Support triage, summaries and reply drafting for Zendesk, Freshdesk and more. One click into Ballet.
- [ballet-sales-playbooks](https://github.com/brainfish-ai/ballet-sales-playbooks): Lead enrichment, scoring and Slack alerts for Salesforce and web forms. One click into Ballet.
- [ballet-ops-playbooks](https://github.com/brainfish-ai/ballet-ops-playbooks): Signed webhooks, scheduled digests and issue triage with retries and observability. One click into Ballet.
- [ballet-mcp-playbooks](https://github.com/brainfish-ai/ballet-mcp-playbooks): Agent workflows that call MCP servers such as Linear and Slack. One click into Ballet.
- [ballet-playbook-starter](https://github.com/brainfish-ai/ballet-playbook-starter): GitHub template repository for publishing your own templates.

## All templates

| Template | What it does | Trigger | Import |
|---|---|---|---|
| [Daily API Digest to Slack](https://github.com/brainfish-ai/ballet-templates/tree/main/templates/daily-api-digest-slack) | Pull records from any JSON API, summarise them, and post a digest to Slack on a schedule. | Manual run, or attach a daily schedule in Studio | [Import](https://app.ballet.dev/import?repo=brainfish-ai/ballet-templates&path=templates/daily-api-digest-slack&ref=main) |
| [Freshdesk Ticket Summary](https://github.com/brainfish-ai/ballet-templates/tree/main/templates/freshdesk-ticket-summary) | Summarise each new Freshdesk ticket in three bullets and add it as a private note for the agent who picks it up. | Freshdesk webhook (ticket created) | [Import](https://app.ballet.dev/import?repo=brainfish-ai/ballet-templates&path=templates/freshdesk-ticket-summary&ref=main) |
| [Generic Webhook Relay](https://github.com/brainfish-ai/ballet-templates/tree/main/templates/generic-webhook-relay) | Verify any signed incoming webhook, reshape it, and forward it to a downstream service with retries. | Generic HMAC webhook | [Import](https://app.ballet.dev/import?repo=brainfish-ai/ballet-templates&path=templates/generic-webhook-relay&ref=main) |
| [GitHub Issue Triage](https://github.com/brainfish-ai/ballet-templates/tree/main/templates/github-issue-triage) | Label every newly opened GitHub issue with an LLM through a signed webhook. | GitHub webhook (issues) | [Import](https://app.ballet.dev/import?repo=brainfish-ai/ballet-templates&path=templates/github-issue-triage&ref=main) |
| [Inbound Lead Slack Alert](https://github.com/brainfish-ai/ballet-templates/tree/main/templates/inbound-lead-slack-alert) | Score every form submission that hits a webhook and post it to Slack, flagging hot leads. | Generic HMAC webhook | [Import](https://app.ballet.dev/import?repo=brainfish-ai/ballet-templates&path=templates/inbound-lead-slack-alert&ref=main) |
| [Linear Weekly Digest via MCP](https://github.com/brainfish-ai/ballet-templates/tree/main/templates/mcp-linear-weekly-digest) | Read recent Linear issues and post a weekly digest to Slack, using the Linear and Slack MCP servers. | Manual run, or attach a weekly schedule in Studio | [Import](https://app.ballet.dev/import?repo=brainfish-ai/ballet-templates&path=templates/mcp-linear-weekly-digest&ref=main) |
| [Slack Thread to Linear Issue via MCP](https://github.com/brainfish-ai/ballet-templates/tree/main/templates/mcp-slack-thread-to-linear) | Turn a Slack thread into a well-formed Linear issue using the Slack and Linear MCP servers. | Manual run | [Import](https://app.ballet.dev/import?repo=brainfish-ai/ballet-templates&path=templates/mcp-slack-thread-to-linear&ref=main) |
| [Salesforce Lead Enrichment](https://github.com/brainfish-ai/ballet-templates/tree/main/templates/salesforce-lead-enrichment) | Research each new Salesforce Lead on the web and write a short brief and rating back to the record. | Salesforce webhook (Lead created) | [Import](https://app.ballet.dev/import?repo=brainfish-ai/ballet-templates&path=templates/salesforce-lead-enrichment&ref=main) |
| [Support Reply Drafter](https://github.com/brainfish-ai/ballet-templates/tree/main/templates/support-reply-drafter) | Paste a customer message and get a polite, source-aware draft reply to review and send. | Manual run | [Import](https://app.ballet.dev/import?repo=brainfish-ai/ballet-templates&path=templates/support-reply-drafter&ref=main) |
| [Zendesk Ticket Triage](https://github.com/brainfish-ai/ballet-templates/tree/main/templates/zendesk-ticket-triage) | Classify every new Zendesk ticket with an LLM and write the priority and tags back as an internal note. | Zendesk webhook (ticket created) | [Import](https://app.ballet.dev/import?repo=brainfish-ai/ballet-templates&path=templates/zendesk-ticket-triage&ref=main) |

## Concepts

- **Playbook**: a workflow of code and HTTP steps with a trigger (webhook, schedule or manual run), versioned and observable.
- **Agent**: an LLM configuration with instructions, optional tools and an output contract, called from a step with `metaphor.agent()`.
- **MCP server**: an external tool server (Linear, Slack, GitHub and others) called from a step with `metaphor.mcp()`.
- **Template**: a playbook folder (`playbook.yaml`, `steps/`, `agents/`, `template.json`) that imports into a workspace with one click.

## Contributing

Add a resource with a pull request: one line per entry, alphabetical within a section, with a short description that says what it does. Templates themselves belong in [ballet-templates](https://github.com/brainfish-ai/ballet-templates).

## License

[CC0](https://creativecommons.org/publicdomain/zero/1.0/)
