# Hi, I'm Krishant

AI engineer and solution architect based in Auckland, New Zealand. I build agentic systems for enterprise clients during the day, and AI products of my own outside of it.

## Project Eval (open source)

**[krishantm.github.io/project-eval](https://krishantm.github.io/project-eval)** · [repo](https://github.com/KrishantM/project-eval)

Does your AI agent actually help? Project Eval measures it: tasks done, time spent by the agent and by you, cost, how often its work is kept or fixed, and quality scored by an LLM judge that is checked against blind human review. Every number says whether it was measured, inferred or estimated.

- **In the browser.** Drop in Claude Code or Codex session logs, or a CSV of agent inputs and outputs, and get a report. Parsed on your machine, nothing uploaded.
- **Self-hosted.** A FastAPI server that takes OpenTelemetry from Claude Code with no code change, imports past sessions and grades them in a LangGraph flow with a local judge. Postgres and Redis Streams underneath.
- **For a team.** A Helm chart for Kubernetes, with workers that scale on the grading backlog (KEDA) and a network policy that keeps data inside the cluster.

Released under Apache-2.0 in November 2026.

## Surya Voice (open source)

**[github.com/KrishantM/surya-voice](https://github.com/KrishantM/surya-voice)**

A free, local alternative to VoiceOS for macOS, built to plug into the agent and the memory you already use. VoiceOS is a paid subscription with its own agent and cloud speech recognition. Surya Voice sends your question to your own coding agent (Claude Code, Codex or any command) in your project folder, with its instructions, MCP servers and memory, so what you say by voice and what you type in the terminal end up in one memory. Hold fn to dictate into any app, or hold fn + control to ask and hear the answer.

- **Your harness, your memory.** Adapters for Claude Code and Codex, a stdin/stdout contract for any other agent, and an editor for the agent's Markdown memory. Voice turns read and write the same memory files as terminal sessions.
- **Dictation anywhere.** On-device speech recognition, with fillers and self-corrections cleaned up by rules or a local model, pasted at the cursor.
- **A spoken agent.** Runs Claude Code headless and streams each step (files read, commands, web results) into a panel in the notch. Replies are spoken a sentence at a time by Kokoro, a text-to-speech model that runs on the Mac.
- **Voice approvals.** Anything consequential the agent tries waits on a confirmation card you answer by saying yes or no.

How I made it: I started it in October 2026 as a daily tool for myself and built it by directing Claude Code from Surya. It is a native Swift app of about 6,000 lines, built with `swiftc` and no Xcode project. One audio engine handles the microphone and the voice, with echo cancellation so you can talk over a reply. A small MCP server inside the same binary turns Claude Code's permission prompts into voice approvals. Kokoro runs as a long-lived Python sidecar, and reusing one phonemiser backend took each spoken sentence from about 650 ms to 190 ms. The demo film is HTML rendered to video with HyperFrames.

Released under MIT in November 2026.

## Surya Memory (open source)

**[github.com/KrishantM/surya-memory](https://github.com/KrishantM/surya-memory)**

One memory, in plain Markdown files you own, for Claude Code, Codex and your other AI tools. It syncs across your machines through your own private GitHub repo, with no account to create and no server. You can see what each tool remembered, correct it, and undo anything an AI wrote.

- **One store.** Every project and every tool reads and writes the same folder. Setup shows its plan first, leaves the originals where they are and keeps both versions when two notes clash.
- **Plugs into your tools.** An MCP server with nine memory tools, run for real with Claude Code and Codex, plus configs for Claude Desktop, Cursor, Windsurf and Gemini CLI.
- **Nothing is lost.** Each write is one git commit named for the tool that made it, and forgetting moves a note to an archive. When two machines change the same note, both versions are kept. It never writes conflict markers into a note, because AI tools read memory as fact.
- **An app to check it.** Browse and edit memories, ask them questions through the Claude or Codex you are already signed in to, and see the exact diff of what each tool changed, with undo beside it. It runs as a local page or a native Mac app.

How I made it: I built it to keep my own agent memory in step between a Mac and a Windows PC, directing Claude Code from Surya. It uses the Python standard library and git, and nothing else. The first version came out of a real bug, two hooks racing to sync the same folder, so every sync now takes a lock and an interrupted one is undone and redone on the next run. 94 Python tests cover the store, the MCP server and the app's API, and 36 more simulate two machines sharing a remote. The app only listens on 127.0.0.1, with a token per launch and a strict content security policy, because a memory note is untrusted text.

Released under MIT in November 2026.

## Surya

**[trysurya.com](https://trysurya.com)**

Surya is an AI operator for non-technical founders. You bring the idea and the judgement, and Surya does the work. It pressure-tests the idea, builds and ships the software, runs the outreach and operates what it built, checking with you before every step that matters.

What I've built so far:

- **An agent server in Python on the Claude Agent SDK**, with approval gates enforced inside the agent loop, so a human signs off every consequential action.
- **Multi-model routing** across Claude, OpenAI models and local open-source models (via Ollama), with a fallback for each role, plus persistent, searchable agent memory. Backed by 500+ automated tests.
- **Native macOS and iPhone apps** with on-device speech recognition and local text-to-speech, so you can talk to your agent from anywhere.
- **A Windows installer**, shipped across 8 releases ([downloads](https://github.com/KrishantM/surya-releases)).
- **An outbound-only relay on Cloudflare Workers and Durable Objects**, so a browser anywhere can reach the agent on a user's own machine without opening their network.

Surya's source is private. Happy to walk through the architecture.

## Gradual (my previous startup)

**[gradual.co.nz](https://www.gradual.co.nz)** · [repo](https://github.com/KrishantM/Gradual)

A career operating system for NZ students and early-career professionals: an AI career copilot, CV scoring, a planner and an opportunities feed that all update each other. Built with Next.js, Firebase and GPT-4o, with a weekly pipeline that pulls in 800+ opportunities from 7 sources. Live from 2025 to 2026.

## Other projects

- **Hiko** · technical co-founder of a hiking planner for New Zealand's tracks, huts and campsites. I built the Department of Conservation API pipeline (pagination, retries, backoff and rate limiting) into Firestore with scheduled Cloud Functions, plus an Expo mobile app. [Repo](https://github.com/KrishantM/Hikodev)
- **CreatorHQ** · direct-to-fan hub apps for fitness creators: memberships, challenges and leaderboards, a community feed and a store hand-off. Built as pitch demos with Next.js, Supabase, Stripe, the Shopify Storefront API and the YouTube Data API.

## Day job

Associate Solution Architect at PwC New Zealand (Digital Strategy & Architecture). I work on agentic engineering, context engineering and cloud architecture for enterprise clients, building and rolling out AI agents and reusable AI skills.

## Tools I work with

Python · TypeScript · SQL · Claude Agent SDK · MCP · RAG and vector databases · LangChain · LangGraph · Docker · Kubernetes · Azure · AWS · Terraform · Databricks · Cloudflare Workers · Next.js · Firebase · Claude Code · Cursor · GitHub Copilot

**Certifications:** AWS Certified Solutions Architect – Associate · Azure Databricks Platform Architect · Microsoft Azure Fundamentals

## Elsewhere

[LinkedIn](https://www.linkedin.com/in/krishant-maharaj) · [krishant.org](https://www.krishant.org)
