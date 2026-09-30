# git-hub-actions

# GitHub Actions CI Workflow

## Description
This project demonstrates the fundamentals of GitHub Actions by creating and executing a basic Continuous Integration (CI) workflow.

The workflow automatically runs when code is pushed to the repository or when a pull request is created.

## Objectives
- Understand GitHub Actions fundamentals.
- Learn workflows, jobs, steps, runners, and actions.
- Configure push and pull_request triggers.
- Use GitHub-hosted Ubuntu runners.
- Understand YAML syntax.
- Configure environment variables.
- Learn how to manage GitHub Secrets securely.
- Execute and verify workflow runs.

## Project Structure
```text
.github/
└── workflows/
    └── ci.yml
README.md
```

## Workflow Configuration
The workflow is defined in `.github/workflows/ci.yml`.

### Triggers
- `push`: Executes the workflow when code is pushed.
- `pull_request`: Executes the workflow when a pull request event occurs.

### Runner
- `ubuntu-latest`: Uses a GitHub-hosted Ubuntu virtual machine.

### Steps
1. Checkout the repository using `actions/checkout@v4`.
2. Display the configured environment variable.
3. Verify that the CI workflow executes successfully.

## Environment Variables
Environment variables store configuration values used during workflow execution.

Example:
```yaml
env:
  APP_ENV: development
```

## GitHub Secrets
GitHub Secrets securely store sensitive information such as API keys, access tokens, and credentials.

Secrets can be configured under:

**Repository → Settings → Secrets and variables → Actions**

Secrets should not be hardcoded in workflow files or committed to the repository.

## Commands Used
```bash
git status
mkdir -p .github/workflows
touch .github/workflows/ci.yml
git add .github/workflows/ci.yml
git commit -m "Add GitHub Actions CI workflow"
git push origin main
```

## Verification
1. Push the workflow file to GitHub.
2. Open the repository's Actions tab.
3. Select the CI Workflow.
4. Review the workflow logs.
5. Verify that the job completes successfully.

## Expected Result
The GitHub Actions workflow should execute automatically on push and pull request events, run on an Ubuntu runner, and complete all configured steps successfully.

## Technologies Used
- Git
- GitHub
- GitHub Actions
- YAML
- Ubuntu GitHub-hosted runner

## Learning Outcome
Gained practical knowledge of basic CI workflow creation, automation triggers, workflow execution, environment variables, GitHub Secrets, and workflow verification.