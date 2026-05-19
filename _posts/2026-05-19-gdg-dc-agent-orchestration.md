---
layout: post
title: "My First Post: Orchestrating Agents and the A2A Protocol at GDG DC"
date: 2026-05-19
categories: AI events
---

Welcome to my public notebook! For my very first post, I want to share some thoughts from a Google Developer Group (GDG) event I recently attended, co-hosted by George Washington University and Northeastern University. 

The main speaker was Noble Ackerson, a Google Developer Expert for AI/ML, and the talk centered on distributed systems, agent orchestration, and the emerging A2A (Agent-to-Agent) protocol.

### Orchestrating A2A Agents

Noble walked through how to think about multi-agent architectures—not just spinning up a single LLM, but designing systems where agents communicate, delegate, and coordinate across tasks. The A2A protocol is Google's answer to the question of how agents built on different frameworks can interoperate. 

The key ideas he touched on included:
* **Distributed task execution:** Breaking a complex workflow into agent-handled subtasks.
* **Agent discovery and delegation:** Agents knowing when to hand off to a specialized peer.
* **Infrastructure:** Using Google ADK and AgentEngine as the scaffolding for deploying and managing these systems in production.

For anyone working on multi-step data analysis pipelines, this mental model maps incredibly well. Each stage of extraction, validation, and classification could theoretically be handled by an agent with a defined, specialized scope.

### The Standout: Invisible City

The demo that stuck with me the most was his *Invisible City* project. The premise: can an AI read the surface of a street—manholes, hydrants, spray-painted utility codes—and reason about what infrastructure lies underground, the exact way an experienced utility worker would?

He built it as a multi-agent vision system using Google ADK, AgentEngine, and the A2A protocol. Each agent handles a specific piece of the pipeline—detecting markers, matching against known utility codes (like APWA color standards), and synthesizing a ground-level inference about what's below. 

It's explicitly framed as an experiment, not a production utility tool. But as a proof of concept for vision, reasoning, and multi-agent coordination, it's one of the cleaner end-to-end demos I've seen.

### Takeaway

The event was a solid reminder that the most interesting work in agentic AI right now isn't just in making a single model smarter—it's in the orchestration layer. How do agents discover each other? How do they negotiate task boundaries? How do you make the whole system observable and debuggable?

Those are the open engineering problems right now, and GDG DC seems to be a great venue for engaging with people actively building on them. Definitely worth attending the next one.
