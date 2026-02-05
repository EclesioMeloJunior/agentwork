# AgentWork

Just a tool for manage git worktrees, helpful for when managing multi-agent work on the same codebase

### Usage

- Go to the codebase folder
- Create a new agent work by `agentwork new feature-a`, this will create a folder `.worktree/feature-a` using the git worktree tool
  - As a suggestion, include the folder `.worktree` to your `.gitignore` 
- Spawn an agent there and everything it will do will be scoped there under a branch prefixed with `agent/`
- Once you are good and you don't need that anymore you can just `agentwork clean feature-a`, it will remove the folder (conveniance) 
- When managing multiple agents you can check the status by `agentwork status` so you can check modified files and commits ahead

```sh
myproject/project ‹main› » agentwork status
feature-a (main) — 0 commits ahead

feature-b (agent/feature-b) — 0 commits ahead
   M tests/helpers.rs
  ?? newfile.rs
```
- To know more use `agentwork help`

