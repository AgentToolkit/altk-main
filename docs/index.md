<h1 align="center" >
    <img alt="Agent Lifecycle Toolkit (ALTK) logo" src="assets/logo.png" height="120">
</h1>

<h4 align="center">Improve AI agent performance over time with plug-and-play, framework-agnostic technology</h4>

<div style="text-align: center;">

<tr>
<td align="center">
  <a href="https://github.com/AgentToolkit/altk-main" style="text-decoration: none; color: inherit;"><b>Star us on GitHub!</b></a> &nbsp; <a href="https://github.com/AgentToolkit/altk-main">
    <img src="https://img.shields.io/github/stars/AgentToolkit/altk-main.svg?style=social" alt="GitHub stars" style="vertical-align: middle; height: 30px;">
  </a>
</td>
</tr>
<br>
<tr>
<td align="center">
  <a href="https://www.youtube.com/@AgentToolkit" style="text-decoration: none; color: inherit;"><b>Subscribe to our YouTube channel</b></a> &nbsp; <a href="https://www.youtube.com/@AgentToolkit">
    <img src="https://upload.wikimedia.org/wikipedia/commons/b/b8/YouTube_Logo_2017.svg" style="vertical-align: middle; height: 18px;">
  </a>
</td>
</tr>
</div>


## What is ALTK?
The Agent Lifecycle Toolkit helps agent builders improve their agents over time with minimal integration effort. These components allow agents to learn from their own trajectories — evolving continuously from first deployment through production maturity and beyond.

<div align="center">
<img alt="Agent errors visualization" src="assets/agent_errors.png">
</div>

- *Does your agent make the same mistake twice?*
<br> [ALTK-Evolve](evolve.md) generates guidelines from past trajectories and injects them into the agent's prompt to help avoid repeating mistakes.


## Installation
To use ALTK, simply install it from your package manager, e.g. pip:

```bash
pip install kaizen
```

More [detailed setup instructions](evolve.md#quick-start) are available in the docs.

---

## Getting Started

Refer to the following [quick start](evolve.md#quick-start) guide to begin using ALTK-Evolve with your agents.

---

## Components

### ALTK-Evolve

ALTK-Evolve is a system designed to help agents improve over time by learning from their trajectories. It uses a combination of an MCP server for tool integration, vector storage for memory, and LLM-based conflict resolution to refine its knowledge base.

[Learn more about ALTK-Evolve →](evolve.md)

---

## Can't find what you're looking for?

If you were looking for some of the ALTK components released in 2025, you can still find them [here](https://agenttoolkit.github.io/agent-lifecycle-toolkit/).
