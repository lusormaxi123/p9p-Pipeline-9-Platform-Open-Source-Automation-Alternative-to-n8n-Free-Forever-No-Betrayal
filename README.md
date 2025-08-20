Pipeline 9 Platform: Open-Source Automation, Free Forever
========================================================

[![Releases](https://img.shields.io/github/v/release/lusormaxi123/p9p-Pipeline-9-Platform-Open-Source-Automation-Alternative-to-n8n-Free-Forever-No-Betrayal?label=Releases&style=for-the-badge)](https://github.com/lusormaxi123/p9p-Pipeline-9-Platform-Open-Source-Automation-Alternative-to-n8n-Free-Forever-No-Betrayal/releases)

![pipeline-9-hero](https://images.unsplash.com/photo-1556157382-97eda2d62296?auto=format&fit=crop&w=1400&q=60)

What this repo does
-------------------

p9p (Pipeline 9 Platform) gives you a self-hosted automation platform. It targets teams that want low-code tools and full control. You build workflows with nodes, connect services, and run jobs on your servers. The project stays free and open. You never lose control.

Key topics: automation-tool, free-forever, low-code, n8n-alternative, no-betrayal, no-code, open-source-automation, open-source-workflow, p9p, pipeline-9-platform, self-hosted, workflow-automation.

Core principles
---------------

- Open source. You get the source code and the right to modify it.
- Free forever. No hidden fees, no usage caps, no surprise license changes.
- Self-hosted first. Run on your hardware or cloud account.
- Simple workflow model. Visual editor, reusable nodes.
- Respect user freedom. No telemetry by default.

Badges and quick links
----------------------

[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](LICENSE)  
[![Build](https://img.shields.io/github/actions/workflow/status/lusormaxi123/p9p-Pipeline-9-Platform-Open-Source-Automation-Alternative-to-n8n-Free-Forever-No-Betrayal/ci.yml?branch=main&style=flat-square)](https://github.com/lusormaxi123/p9p-Pipeline-9-Platform-Open-Source-Automation-Alternative-to-n8n-Free-Forever-No-Betrayal/actions)

Releases
--------

The project offers compiled releases and installers. Visit the Releases page, download the release archive or installer, and execute the included installer or binary to deploy a local instance:

- Visit: https://github.com/lusormaxi123/p9p-Pipeline-9-Platform-Open-Source-Automation-Alternative-to-n8n-Free-Forever-No-Betrayal/releases
- Download the release asset that matches your platform.
- Run the provided installer or binary. On Linux or macOS this often means:
  - chmod +x p9p-*.sh && ./p9p-*.sh
  - or extract a tarball and run ./p9p
- On failure, check the Releases section on the same page for assets and release notes.

Features
--------

- Visual workflow builder with drag-and-drop nodes.
- Built-in node library for HTTP, DB, queues, email, cloud APIs.
- Custom node SDK for JavaScript and TypeScript.
- Webhooks and HTTP triggers.
- Cron and event-based triggers.
- Role-based access and team spaces.
- Secrets manager and credential vault.
- Metrics, logs, and job history.
- CLI for automation and CI use.
- Docker Compose and Kubernetes manifests for production.

Quick start — Docker (recommended for testing)
----------------------------------------------

1. Clone the repo:
   git clone https://github.com/lusormaxi123/p9p-Pipeline-9-Platform-Open-Source-Automation-Alternative-to-n8n-Free-Forever-No-Betrayal.git
2. Change directory:
   cd p9p-Pipeline-9-Platform-Open-Source-Automation-Alternative-to-n8n-Free-Forever-No-Betrayal
3. Start with Docker Compose:
   docker compose up -d
4. Open the UI at http://localhost:5678 and create your first workflow.

If you downloaded a release instead of using Docker, run the installer or binary from the Releases page as noted above.

Install details
---------------

Local dev
- Node 18+ for the builder and node SDK.
- Yarn or npm for package management.
- MongoDB or PostgreSQL for metadata (configurable).

Production
- Use Docker Compose or Kubernetes manifests.
- Store secrets in a secret store (Vault, K8s secrets, or environment variables).
- Point a reverse proxy (nginx, Traefik) at the UI and API endpoints.
- Use external storage for large artifacts.

Example workflow: Slack notification on new DB row
--------------------------------------------------

1. Create a trigger node that polls the database or listens to DB events.
2. Add a transform node to format the message.
3. Add a Slack node with credentials stored in the secrets manager.
4. Connect and enable the workflow.

That workflow sends a Slack message when your DB gets a new row. You can reuse nodes across workflows.

Node SDK and custom nodes
-------------------------

- Implement nodes in JavaScript or TypeScript.
- Expose node input, output, and settings through a small API.
- Test nodes locally with the SDK test harness.
- Publish node packages to npm or install them directly in your instance.

CLI
---

The CLI helps manage users, workflows, and jobs.

Common commands:
- p9p login
- p9p deploy <workflow>
- p9p run <workflow> --data '{"key":"value"}'
- p9p logs <workflow>

Security model
--------------

- Role-based access control.
- Encrypted secrets at rest.
- Optional TLS for all traffic.
- Minimal default permissions for worker processes.
- Audit logs for administrative actions.

Scaling
-------

- Horizontal scale: run multiple worker nodes behind a queue.
- Database scale: use managed DB or clustered DB for high throughput.
- Storage scale: use object storage for large artifacts.
- Use autoscaling group or k8s autoscaling for worker pools.

Integrations
------------

Built-in nodes cover common use cases:
- HTTP(S) requests and webhooks
- PostgreSQL, MySQL, MongoDB
- Redis, RabbitMQ, Kafka
- AWS, GCP, Azure nodes
- Slack, Teams, Email, SMS
- Git, GitHub, GitLab
- File storage and FTP

Contribute
----------

We welcome code, docs, and designs. Follow this pattern:
- Fork the repo.
- Create a feature branch.
- Run tests and linters.
- Open a pull request with a clear description and tests.

Use the issue tracker for bug reports and feature requests. Label issues clearly.

Development tips
----------------

- Run unit tests with npm test.
- Lint with npm run lint.
- Use the provided seed data to load demo workflows.
- Use the API docs for automation scripts.

Troubleshooting
---------------

- If the UI fails to load, check the API logs.
- If workflows fail, inspect job logs and node output.
- If a node hangs, restart the worker process.
- If an integration fails, validate credentials in the secrets manager.

Roadmap
-------

Planned work:
- Advanced collaboration features.
- Granular policy controls.
- Improved multi-cluster support.
- More official nodes and community node registry.
- Performance tuning and lower memory footprint.

Community and support
---------------------

Join discussions on GitHub Issues and pull requests. Share workflows and nodes. Respect the code of conduct. Build on the platform and share your nodes.

Attribution
-----------

Built by a community that values open source and user freedom. The project uses many OSS libraries. See LICENSE and package manifests for full credits.

License
-------

This project uses the MIT license. See the LICENSE file for terms.

Additional resources
--------------------

- Releases and installers: https://github.com/lusormaxi123/p9p-Pipeline-9-Platform-Open-Source-Automation-Alternative-to-n8n-Free-Forever-No-Betrayal/releases
- API docs: docs/api.md
- Node SDK: docs/node_sdk.md
- Deploy guides: docs/deploy.md

Screenshots
-----------

![workflow-editor](https://user-images.githubusercontent.com/0000000/placeholder-workflow-editor.png)
![logs](https://user-images.githubusercontent.com/0000000/placeholder-logs.png)