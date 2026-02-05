# AgentWork

Just a tool for manage git worktrees, helpful for when managing multi-agent work on the same codebase

### Usage

1. Go to the codebase folder
2. Create a new agent work by `agentwork new feature-a`, this will create a folder `.worktree/feature-a` using the git worktree tool
3. Spawn an agent there and everything it will do will be scoped there under a branch prefixed with `agent/`
4. Once you are good and you don't need that anymore you can just `agentwork clean feature-a`
5. When managing multiple agents you can check the status by `agentwork status` so you can check modified files and commits ahead

```sh
myproject/project ‹main› » agentwork status
feature-a (main) — 0 commits ahead

feature-b (agent/feature-b) — 0 commits ahead
   M tests/helpers.rs
  ?? newfile.rs
```
6. To know more use `agentwork help`

