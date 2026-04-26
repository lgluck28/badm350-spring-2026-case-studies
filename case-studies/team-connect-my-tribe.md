# Team Connect My Tribe — User Feedback Analyzer

**Project:** [Connect My Tribe](https://connect-my-tribe-95.lovable.app/) — a Chicago-focused community app that helps people discover events, find shared-interest groups, and make real in-person connections.
**Built by:** Lindsay Gluck
**Automation type:** Operations

---

## Product

Connect My Tribe is a Chicago-first community app designed to help people discover local events and meet others with shared interests. The product is meant to make belonging easier in a big city by helping users move from browsing to real in-person connection.

## Automation

I used Codex to build an internal feedback-analysis workflow for Connect My Tribe after user testing. Instead of changing the live app directly, the automation took raw tester observations and converted them into an executive summary, a categorized analysis of issues, a prioritized backlog, and a recommended build order for the team.

This helped turn messy feedback into concrete operating decisions. The output highlighted that the most urgent issue before launch was hiding admin controls from non-admin users, followed by fixing the profile-name bug and reducing choice overload in event and group discovery.

## Prompt used

This is the final working instruction set reflected in the saved files from my Module 3 workflow:

```text
Analyze Connect My Tribe user-testing feedback from our pre-launch testers.

Take the raw feedback and produce:
- an executive summary of what is working and what is highest risk
- a categorized feedback analysis by tester, issue type, and severity
- a prioritized action plan with P0, P1, and P2 items
- a backlog table the team can use to plan implementation

Focus on what matters most before launch. Separate praise, bugs, privacy or access-control issues, UX friction, and feature requests. Make the output useful for product and engineering decisions, not just a summary of comments.
```

## Inner / outer loop

- **Inner loop (AI execution):** Codex organized the tester feedback, classified each comment by category and severity, identified repeated themes, and turned the notes into an executive summary, a prioritized action plan, and a structured backlog.
- **Outer loop (human judgment):** I had to judge whether the prioritization actually matched our launch risk, decide which issues were truly blocking, and choose what the team should fix first given time and product goals.

## Anthropic agent pattern

Which of these fits best? Pick one and defend in 1-2 sentences.

- [x] Prompt chaining
- [ ] Routing
- [ ] Parallelization
- [ ] Orchestrator-worker
- [ ] Evaluator-optimizer

**Why this one:** The workflow moved from raw input to progressively more decision-ready outputs: tester observations became a categorized analysis, then an executive summary, then a prioritized action plan and backlog. Each stage depended on the structure created in the previous one.

## What required human judgment

The automation was not fully autonomous because I still had to judge product risk, especially around trust and privacy. For example, Codex correctly surfaced admin visibility as critical, but I had to decide whether that issue was truly launch-blocking, whether the profile-name bug was a data issue or a UI-sync issue, and how much weight to give feature requests like an RSVPd-events tab compared with privacy and usability problems.

If I had let Codex run end-to-end without checking it, I could have ended up with a neat-looking plan that over- or under-prioritized the wrong issues. The human role was deciding what actually threatens launch readiness versus what can wait.

## What didn't work

The biggest limitation is that the automation only works as well as the quality of the raw feedback. We only had three testers, so patterns were useful but still based on a small sample. That means the analysis was helpful for prioritization, but not enough to treat every recommendation as universally true.

Another limitation is that Codex can classify and summarize issues well, but it cannot fully infer technical root cause from user comments alone. The analysis could tell us that admin visibility was a critical trust issue, but not whether the fix belonged in frontend rendering, auth rules, or backend permissions without additional inspection from us.

---

*Submitted for BADM 350, Spring 2026.*
