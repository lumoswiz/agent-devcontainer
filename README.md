# Agent Devcontainer

Personal fork of [trailofbits/claude-code-devcontainer](https://github.com/trailofbits/claude-code-devcontainer) adding OpenAI Codex CLI and omp (oh-my-pi). See upstream for the original setup and security documentation.

This fork is for personal use and is not intended for upstream submission.

## Install

Requires Docker and the [Dev Container CLI](https://github.com/devcontainers/cli).

```bash
npm install -g @devcontainers/cli
git clone https://github.com/lumoswiz/agent-devcontainer ~/.claude-devcontainer
~/.claude-devcontainer/install.sh self-install

cd /path/to/project
devc .
devc shell
```

## Added Harnesses

| Harness | Authentication | Persistent state |
|---------|----------------|------------------|
| Claude Code | Run `claude` and sign in with your Claude subscription. No API key is passed in from the host | `~/.claude` |
| Codex | Run `codex login`, or export `OPENAI_API_KEY` before `devc rebuild` | `~/.codex` |
| omp | Sign in during first-run setup, or export `OPENAI_API_KEY` before `devc rebuild`. Runs in yolo approval mode | `~/.omp` |

## Acknowledgements

Based on [Trail of Bits' Claude Code devcontainer](https://github.com/trailofbits/claude-code-devcontainer).
