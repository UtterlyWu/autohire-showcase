# AutoHire

AI-powered job-search and resume-tailoring application that combines job-fit analysis, agentic resume generation, automated quality checks, and reliable asynchronous workflow execution.

> Source code is maintained in a private repository. This repository provides a technical overview of the project, architecture, and engineering decisions.

## What It Does

AutoHire helps streamline the job application workflow by combining job analysis and resume tailoring in one application.

Key capabilities include:

- Evaluating job descriptions against a user's experience
- Producing evidence-based job-fit scores
- Generating tailored resumes grounded in verified experience
- Rendering and evaluating generated resumes
- Automatically repairing outputs that fail quality checks
- Tracking long-running workflow progress across multiple services
- Recovering safely from interrupted or retried runs

## Architecture

```text
React / TypeScript
       │
       ▼
Cloudflare Workers
       │
       ▼
Supabase / PostgreSQL
       │
       ▼
      Modal
       │
       ▼
Python / LangGraph Workflows
