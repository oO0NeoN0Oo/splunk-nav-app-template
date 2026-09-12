# Splunk App Template

This repository provides a standardised starting point for all Splunk applications
developed using a GitOps workflow.

## Structure

- default/        → Splunk default configuration files
- local/          → Local overrides
- bin/            → Python scripts
- static/         → CSS, JS, images
- metadata/       → Permissions and visibility
- appserver/      → Modern UI assets (React/Node builds)

## Development Workflow

1. Clone this template into a new repository.
2. Rename the app folder and update `app.conf`.
3. Develop your app in VS Code.
4. Use your deploy script to push the app into Splunk.
5. Commit changes to GitHub as the single source of truth.

## Packaging

Apps can be packaged using:

    splunk pack app <path>

## Dashboard Studio Policy

Dashboard Studio dashboards (JSON-based) are not included in this template and
must not be committed to Git. All dashboards for this application must be
implemented using Custom XML or SimpleXML only.

This ensures:
- GitOps compatibility
- Automated deployment
- No GUI-only CRUD operations
- No drift between Splunk and GitHub


## Notes

This template is designed for GitOps workflows and CI/CD pipelines.
