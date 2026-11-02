# Hi, I'm Krishant

AI engineer and solution architect based in Auckland, New Zealand. I build agentic systems for enterprise clients during the day, and AI products of my own outside of it.

## Surya (what I'm building now)

**[trysurya.com](https://trysurya.com)**

Surya is an AI operator for non-technical founders. You bring the idea and the judgement; Surya does the work. It pressure-tests the idea, builds and ships the software, runs the outreach and operates what it built, checking with you before every step that matters.

What I've built so far:

- **An agent server in Python on the Claude Agent SDK**, with approval gates enforced inside the agent loop, so a human signs off every consequential action.
- **Multi-model routing** across Claude, OpenAI models and local open-source models (via Ollama), with a fallback for each role, plus persistent, searchable agent memory. Backed by 500+ automated tests.
- **Native macOS and iPhone apps** with on-device speech recognition and local text-to-speech, so you can talk to your agent from anywhere.
- **A Windows installer**, shipped across 8 releases ([downloads](https://github.com/KrishantM/surya-releases)).
- **An outbound-only relay on Cloudflare Workers and Durable Objects**, so a browser anywhere can reach the agent on a user's own machine without opening their network.

Surya's source is private. Happy to walk through the architecture.

## Project Eval (in development)

**Does your AI agent actually help? Project Eval measures it.**

Project Eval is a self-hosted platform that evaluates AI agents and measures their impact. It tracks what people actually do with an agent's output, grades quality with an LLM judge calibrated against human review, and compares the same work with and without AI. It's built on LangChain and LangGraph, with a containerised Kubernetes infrastructure so it can run inside a company's own environment.

Project Eval's source is private while it's in development.

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
