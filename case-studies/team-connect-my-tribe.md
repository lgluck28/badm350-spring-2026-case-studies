# Team Connect My Tribe — Waitlist Teaser Campaign

**Project:** [Connect My Tribe](https://connect-my-tribe-95.lovable.app/) — a Chicago-focused community app that helps people discover events, find shared-interest groups, and make real in-person connections.
**Built by:** Lindsay Gluck
**Automation type:** Marketing

---

## Product

Connect My Tribe is a Chicago-first community app designed to help people discover local events and meet others with shared interests. The product is meant to make belonging easier in a big city by helping users move from browsing to real in-person connection.

## Automation

I used Codex to build a pre-launch marketing workflow for Connect My Tribe instead of just one asset. The automation produced a landing page that acts as a front door into the live app, an email reminder signup flow, a teaser content hub, a 5-post content calendar, a confirmation email template, a nurture sequence, and a launch checklist so I could turn product positioning into something I could actually share.

The clearest proof of work is the landing page preview in my Module 3 folder. That page explains the product, routes users into the live app, and includes a reminder form that saves submissions locally now and is ready to post the same payload to a real webhook later.

## Prompt used

This is the final working instruction set reflected in the saved files from my Module 3 workflow:

```text
Create a launch-ready waitlist teaser campaign for Connect My Tribe, a Chicago-focused app that helps people discover local events, meet others with shared interests, and build real in-person community.

Build a clean landing page that:
- explains what the product does and who it is for
- gives users a simple path into the live app
- includes primary and secondary calls to action for sign in and account creation
- adds trust signals and short sections for the problem, solution, how it works, and differentiation
- also includes an email reminder signup form for people who are interested but not ready to enter the app yet

Also create:
- a 5-post teaser content calendar for Instagram, LinkedIn, and X
- a waitlist confirmation email
- a short nurture email sequence
- a simple launch checklist

Keep the tone practical and launch-oriented, optimized for real users in Chicago. Make the reminder form demo-ready with local storage and make it easy to swap in a real webhook endpoint later.
```

## Inner / outer loop

- **Inner loop (AI execution):** Codex generated the landing page structure and copy, built the reminder form behavior, created the content calendar, drafted the confirmation email and nurture sequence, and assembled the launch checklist and supporting campaign assets.
- **Outer loop (human judgment):** I decided the product positioning, checked whether the copy actually matched Connect My Tribe, reviewed the CTA flow into the live app, and determined what still needed to be connected manually before this could be used in a real campaign.

## Anthropic agent pattern

Which of these fits best? Pick one and defend in 1-2 sentences.

- [x] Prompt chaining
- [ ] Routing
- [ ] Parallelization
- [ ] Orchestrator-worker
- [ ] Evaluator-optimizer

**Why this one:** The work happened as a sequence of connected outputs: first a landing-page brief and positioning, then the landing page itself, then supporting campaign assets like reminder signup logic, content posts, emails, and a launch checklist. Each artifact depended on the messaging decisions established in the earlier step.

## What required human judgment

The automation was not fully autonomous because I still had to judge whether the messaging fit the actual product and whether the calls to action reflected the real app flow. I also had to decide what counts as a credible trust signal, whether the Chicago-first positioning was strong enough, and how the page should connect to production tools like sign-in routes and an email platform.

If I had let Codex run end-to-end without checking it, I could have ended up with polished but inaccurate product copy, incorrect auth links, or a reminder flow that looked finished even though it was only saving submissions locally in the browser.

## What didn't work

The first limitation was that the landing page did not have the app's exact sign-in and sign-up route paths available in the workspace, so the CTAs point to the live app root instead of separate auth screens. The second limitation was that the reminder signup flow is only partially production-ready: it stores submissions in browser local storage and still needs a real webhook or backend endpoint connected.

More broadly, the automation was strong at packaging and copy generation, but it still needed manual review to avoid overclaiming traction or assuming too much about user behavior. The output looked polished quickly, but the human work was in deciding what was actually true, what was technically connected, and what still needed to be implemented before launch.

---

*Submitted for BADM 350, Spring 2026.*
