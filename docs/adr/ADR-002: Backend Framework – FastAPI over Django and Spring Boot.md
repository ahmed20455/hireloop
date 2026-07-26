# ADR-002: Backend Framework – FastAPI over Django and Spring Boot

**Status:** Accepted
**Date:** 2026-07-26

## Context
The backend exposes REST APIs, communicates with AI models, and handles authentication, database operations, and business logic. Since this project also involves AI agents, I wanted to minimize context switching between programming languages while maintaining good performance

## Decision
I chose FastAPI as the backend framework

## Alternatives considered
# Django

Django is a mature framework with many built-in features such as an admin panel and authentication. However, the project does not require many of these features, and FastAPI provides a lighter and more API-focused development experience.

# Spring Boot

Spring Boot is widely used in enterprise Java applications and is highly scalable. However, using Java for the backend while building AI functionality in Python would require switching between two different ecosystems, slowing development

## Consequences
# Benefits
- Uses Python, the same language as the AI components.
- Excellent performance for REST APIs.
- Automatic OpenAPI (Swagger) documentation.
- Strong type checking and validation using Pydantic.
- Easy integration with AI libraries and machine learning models.

# Trade-offs
- Fewer built-in features compared to Django.
- Smaller enterprise ecosystem compared to Spring Boot.
- Some functionality must be implemented manually instead of relying on built-in components.

FastAPI allows me to focus on building APIs and AI features efficiently while strengthening my Python backend skills.
