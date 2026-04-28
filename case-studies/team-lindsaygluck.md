# Team Lindsay Gluck — Connect My Tribe Teaser Campaign + Feedback Loop

**Project:** [Connect My Tribe live app](https://connect-my-tribe-95.lovable.app/) and [launch landing page](https://lgluck28.github.io/connect-my-tribe-landing/)
**Built by:** Lindsay Gluck
**Automation type:** Marketing

---

## Product

Connect My Tribe is a Chicago-focused community app that helps users discover local events, find groups around shared interests, and build real in-person connection. The target user is someone who wants more intentional community than a generic event-listing or social feed can provide.

## Automation

This automation created a public-facing teaser campaign system around the product. It generated a launch landing page, a teaser content hub with five pre-launch posts, an anonymous Google Form feedback loop, and a daily reporting workflow that turns new feedback into recurring product recommendations. The problem it solved was not just "make a page," but "create a repeatable way to attract early users, capture signals, and learn what to improve before launch."

## Prompt used

Final working instruction:

> Build a Connect My Tribe launch landing page and teaser content hub that routes users into the live app, captures reminder-list signups, and adds an anonymous feedback form asking what worked well, what did not, and what we should improve next. Then connect that feedback loop to a daily 8:00 AM recommendation report so we can see the most common praise, friction points, and requests without manually reviewing every response.

## Inner / outer loop

- **Inner loop (AI execution):** Codex drafted the landing page HTML, teaser content hub, feedback-form wiring, Google Form template, response-sheet CSV setup, and the daily feedback-report automation spec. It also published the static landing-page repo and connected the recurring report workflow.
- **Outer loop (human judgment):** I decided the product positioning, approved the live copy, supplied the real Google Form and response-sheet links, checked whether the feedback questions felt right, and judged whether the recommendations matched what the product actually needed.

## Anthropic agent pattern

- [ ] Prompt chaining
- [ ] Routing
- [ ] Parallelization
- [ ] Orchestrator-worker
- [x] Evaluator-optimizer

**Why this one:** The work was iterative and feedback-driven. Codex produced a first version of the launch pages and feedback workflow, then I evaluated the outputs, swapped in real links, checked live behavior, and used actual user submissions to refine the reporting loop.

## What required human judgment

Human judgment was necessary for product messaging, trust, and scope. Codex could generate persuasive landing-page copy and summarize feedback, but it could not know whether the value proposition was true to the product, whether the Google Form questions felt appropriate for real users, or whether the app should emphasize recommendations, privacy, or onboarding first. Without review, the system also would not have had the correct live Google Form link or the right response-sheet tab to read.

## What didn't work

Several things broke or needed manual correction. First, Google Sheets access was not immediately readable by automation because the initial response-sheet link and `gid` were wrong, so the CSV export failed until the exact response tab was shared. Second, the live landing-page repo ended up with duplicate page paths (`index.html` and `landing-page-preview.html`), which made the publishing flow messier than expected. Third, the earliest user feedback showed that although the site looked polished, some users still did not understand what the product actually did, which means the first draft of the teaser messaging was visually strong but not yet clear enough. The project worked, but only after multiple iterations and explicit human corrections.

---

*Submitted for BADM 350, Spring 2026.*
