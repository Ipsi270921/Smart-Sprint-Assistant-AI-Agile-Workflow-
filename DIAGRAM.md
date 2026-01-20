# System Architecture Flowchart

Below is the automation logic for the AI-Agile-Workflow assistant.

```mermaid
graph TD
    A[Slack: #dev-updates] -->|New Message| B(Zapier Trigger)
    B --> C{ChatGPT AI Analysis}
    C -->|Identify Category| D[Bug/Feature/Task]
    C -->|Assign Priority| E[High/Med/Low]
    D & E --> F(Trello Action)
    F --> G[New Backlog Card Created]
