# Derek Burns

Fourth-year Bachelor of Information Technology (Networking) student at Carleton University in Ottawa, Ontario, graduating April 2028. My background is network infrastructure: routing, switching, BGP, MPLS and enterprise IT administration. I bring that same discipline to software, with a focus on automation, DevOps practice, secure design and AI-assisted engineering.

**Looking for co-op roles for Winter 2027 (January) and Summer 2027** in Linux, DevOps, networking, software engineering or software development.

## Currently building: FairShuffle

[**FairShuffle**](https://github.com/derekburnz/fairshuffle) is a Windows 11 system tray app that gives a Spotify playlist a true uniform random shuffle. Spotify's built-in shuffle is not uniformly random, so FairShuffle rewrites the playlist's order itself with a Fisher-Yates shuffle and a cryptographically secure random source.

- **Secure sign-in.** OAuth 2.0 Authorization Code with PKCE, so there is no client secret anywhere. The refresh token lives only in Windows Credential Manager, and logs mask tokens before anything is written.
- **Safe writes.** Every shuffle backs up the current order first, writes through the Spotify Web API, reads the playlist back to verify nothing was lost or duplicated, and can be undone.
- **Tested for fairness.** A chi-square test checks that every possible order comes up equally often, and the tests run against a fake Spotify so CI never touches the real API.
- **A real team workflow.** Protected `main`, every change through a pull request linked to an issue, Conventional Commits, CI on Windows (ruff, pyright, pytest), gitleaks secret scanning, Dependabot, milestones, a project board and SemVer releases (v0.1.0 to v0.4.0 so far).

Stack: Python 3.14, PySide6 (Qt), uv, GitHub Actions.

### Built with Claude Code and AI agents

I build FairShuffle with [Claude Code](https://claude.com/claude-code) as an AI pair programmer, and I set it up the way an engineering team would set up a new hire: with clear rules, specialists and guardrails. Everything lives in the repo's [`.claude/`](https://github.com/derekburnz/fairshuffle/tree/main/.claude) folder and [`CLAUDE.md`](https://github.com/derekburnz/fairshuffle/blob/main/CLAUDE.md).

- **Specialist subagents.** A security reviewer checks every pull request before merge, a test engineer writes tests, an API researcher verifies Spotify facts against the official docs before any code depends on them, plus a docs writer and a UI designer.
- **Skills.** Reusable playbooks for shipping a change end to end, writing phase reports, presenting decisions and keeping verified Spotify API notes.
- **Hooks and permissions.** A hook formats Python after every edit, and permission rules block the agent from reading secrets, force-pushing or tagging releases without my approval.
- **MCP connectors and remote control.** The agent works with GitHub through the GitHub MCP server and runs tests on my Windows PC through Remote Control.
- **Human in the loop.** I make every design decision. The agent brings options with a recommendation, and over 80 decisions are logged in [`DECISIONS.md`](https://github.com/derekburnz/fairshuffle/blob/main/docs/planning/DECISIONS.md).

## Earlier projects

| Project | What it is | Language |
|---------|------------|----------|
| [Network performance prediction GNN](https://github.com/derekburnz/Network-Performance-Prediction-GNN) | Team course project (NET3006A): a graph neural network based on RouteNet-Fermi that predicts per-flow delay in packet-switched networks, with 9.72% error on unseen 240-node topologies | Python, PyTorch |
| [DHCPServer](https://github.com/derekburnz/DHCPServer) | Emulates the basics of a DHCP server: IP offer, release, lease time check and renewal | Python |
| [Docker word guessing game](https://github.com/derekburnz/Docker-Containerized-WordGuessing-Game) | A small game used to practise containerizing code and running it on Docker | Python |
| [Windows 10 context menu script](https://github.com/derekburnz/Windows-10-Context-menu-script) | Restores the Windows 10 right-click menu on Windows 11 | Batch |
| [BitcoinConverter](https://github.com/derekburnz/BitcoinConverter) | Bitcoin price lookup in USD, GBP and EUR | Python |

## Skills

**Networking:** routing, switching, BGP, MPLS, enterprise IT administration<br>
**Languages:** Python, JavaScript, Batch<br>
**Machine learning:** PyTorch, graph neural networks<br>
**DevOps and tools:** Git, GitHub Actions, Docker, uv, pre-commit<br>
**AI-assisted engineering:** Claude Code, subagents, skills, hooks, MCP servers

## Contact

[LinkedIn](https://linkedin.com/in/derek-burns-) · [257335.burns@gmail.com](mailto:257335.burns@gmail.com)
