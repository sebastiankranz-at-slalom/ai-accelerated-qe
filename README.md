# ai-accelerated-qe
AI-accelerated Quality Engineering workspace with Playwright, Atlassian, and GitHub integrations

## Environment Configuration

This workspace uses a `.env` file to configure the Model Context Protocol (MCP) servers. The environment file is used by both the Atlassian and GitHub MCP servers.

### Setting Up Your .env File

1. Create a `.env` file in the root directory of your workspace
2. Add your configuration variables to the file

Example `.env` file contents:
```env
# Atlassian (Jira/Confluence) Configuration
JIRA_HOST=your-instance.atlassian.net
JIRA_USERNAME=your-email@domain.com
JIRA_API_TOKEN=your-atlassian-api-token

# GitHub Configuration
GITHUB_TOKEN=your-github-personal-access-token
```

### Required Environment Variables

#### For Atlassian Integration
- `JIRA_HOST`: Your Atlassian instance URL
- `JIRA_USERNAME`: Your Atlassian account email
- `JIRA_API_TOKEN`: Your Atlassian API token (can be generated from your Atlassian account settings)

#### For GitHub Integration
- `GITHUB_TOKEN`: Your GitHub Personal Access Token (PAT)

### Security Notes
- Never commit your `.env` file to version control
- Keep your API tokens and credentials secure
- Add `.env` to your `.gitignore` file

The environment variables will be automatically loaded by the Docker containers when running the MCP servers, as configured in the `.vscode/mcp.json` file.
