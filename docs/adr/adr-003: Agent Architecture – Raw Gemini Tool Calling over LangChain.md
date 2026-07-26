# ADR-003: Agent Architecture – Raw Gemini Tool Calling over LangChain

**Status:** Accepted
**Date:** 2026-07-26

## Context
The project includes AI agent functionality. I wanted to understand how an AI agent works internally instead of depending entirely on a framework. Building the core workflow myself would help me understand prompting, tool calling, function execution, and response handling before introducing additional abstractions.

## Decision
I chose to implement the first version of the agent using Gemini's native tool-calling capabilities instead of building it with LangChain.

## Alternatives considered
# LangChain

LangChain provides many useful abstractions and integrations that simplify agent development. However, using it immediately can hide many implementation details, making it harder to understand how tool calling actually works

## Consequences

# Benefits
- Better understanding of the complete AI agent workflow.
- Less framework overhead.
- Easier debugging because every step is implemented explicitly.
- Stronger foundation before learning higher-level frameworks like LangGraph and LangChain.

# Trade-offs
- More code must be written manually.
- Some features that frameworks provide out of the box need to be implemented independently.
- Additional effort is required as the project grows.

After gaining a solid understanding of native tool calling, future versions of the project can adopt LangGraph or LangChain where they provide clear advantages.
