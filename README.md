# open-jira-bug-action
GitHub action for opening a bug on Jira.

This Github Action enables you to open a Jira bug in a specified project, with a summary, description, and optional attachment.

## Inputs
 - jira-base-url (required): The base URL for your Jira instance.
 - jira-user-email (required): The email of the Jira user that will be used to create the bug.
 - jira-api-token (required): The API token for the Jira user that will be used to create the bug.
 - jira-project-key (required): The project key for the Jira project in which the bug will be created.
 - bug-summary (required): A brief summary of the bug.
 - bug-description (required): A detailed description of the bug.
 - attachment-path (required): The path to the attachment you want to include with the bug.
 - attachment-name (required): The name you want to give the attachment.
 - assignee (optional): The display name of the assignee for the bug. If not provided, the bug will be auto-assigned to the default user.

## Usage
```yaml

- name: Open Jira Bug
  uses: my-org/open-jira-bug@v1
  with:
    jira-base-url: 'https://my-jira-instance.com'
    jira-user-email: 'my-jira-user@example.com'
    jira-api-token: ${{ secrets.JIRA_API_TOKEN }}
    jira-project-key: 'MYPROJ'
    bug-summary: 'Bug summary'
    bug-description: 'Detailed description of the bug'
    attachment-path: './logs.zip'
    attachment-name: 'logs.zip'
    assignee: 'John Smith'
```