# Agent team

Mona's Project Pulse dashboard is built using a team of four specialized agents, orchestrated through the GitHub Copilot CLI in a Codespace.

## The Team

### Orchestrator
- **Model**: Claude Opus 4.7
- **Responsibility**: Breaks down complex requests into tasks and delegates work to specialist agents. Coordinates Planner, Coder, and Designer to deliver integrated results.
- **Location**: `.github/agents/orchestrator.agent.md`

### Planner
- **Model**: Claude Opus 4.7
- **Responsibility**: Creates implementation strategies by researching the codebase, documentation, and dependencies. Produces practical plans with ordered steps, file assignments, and identified edge cases.
- **Location**: `.github/agents/planner.agent.md`

### Coder
- **Model**: GPT-5.5
- **Responsibility**: Implements code-oriented tasks with clear structure, explicit errors, and testable behavior. Writes code, fixes bugs, and implements logic within assigned file scopes. Creates support configuration like `.vscode/launch.json` for runnable apps.
- **Location**: `.github/agents/coder.agent.md`

### Designer
- **Model**: Gemini 3.1 Pro
- **Responsibility**: Handles UI/UX, accessibility, information architecture, interaction flow, and visual design. Creates polished dashboards with responsive layouts, visual affordances, and consistent product patterns.
- **Location**: `.github/agents/designer.agent.md`

## Orchestration Model

The GitHub Copilot CLI coordinates this team by:
1. Requesting strategic plans from the Planner
2. Parsing plans into phases with clear file assignments
3. Running tasks in parallel when file scopes don't overlap
4. Running tasks sequentially when work is interdependent
5. Verifying integrated results hang together
