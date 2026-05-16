# Repository Instructions

## Project

FollowFrame is an agentic meeting accountability system.

Core loop:

1. Transcript in.
2. Extract cited action items, owners, deadlines, decisions, and missing-info flags.
3. Store persistent meeting/task state.
4. Draft follow-up emails or reminders.
5. Require human approval before sending.
6. Check pending and overdue tasks over time.
7. Measure extraction quality with evals.

Positioning:

- Not just meeting notes.
- Not just summarization.
- The product is accountability automation: turning meeting commitments into tracked follow-through.

## Planned Stack

- Backend: FastAPI
- Agent workflow: LangGraph
- Database: Supabase/Postgres
- Email: Resend
- Tracing: Langfuse
- Scheduler: APScheduler
- Frontend: React
- Deployment: decide later, likely a simple hosted MVP first

## Build Sequence

1. Repo and environment setup.
2. Database schema.
3. Seed eval set with 5 labeled transcripts.
4. Core extraction pipeline.
5. Basic validation, confidence, and citation checks.
6. FastAPI backend.
7. Langfuse tracing.
8. Email draft approval flow.
9. Async follow-up engine.
10. Frontend.
11. Deploy.
12. Expand eval suite and CI.

Key rule: evals early, frontend late, deploy before over-polish.

## Engineering Preferences

- Prefer small, shippable steps.
- Inspect the codebase before making assumptions.
- Use the repo's existing patterns once they exist.
- Keep MVP scope protected.
- New findings can change implementation, but not randomly change the goal.
- Classify new findings as blocker, improvement, later enhancement, or ignore.
- For code changes, run relevant tests or clearly say why they were not run.
- Keep explanations concise and implementation-focused.
- Verify external claims before adding them to docs or product positioning.

## Quality Bar

The project should demonstrate real AI engineering:

- structured LLM extraction
- workflow orchestration
- tool use
- persistent state
- human-in-the-loop approval
- scheduled automation
- observability
- evals with precision/recall-style metrics
- clear README and architecture notes
