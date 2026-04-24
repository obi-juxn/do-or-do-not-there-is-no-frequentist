# CLAUDE.md — Bayesian Statistics Self-Study Repo

> Read this file at the start of every session. Do not ask me to re-explain
> my background, goals, or current position in the curriculum. If SESSION.md
> exists in this repo, read that too before responding.

---

## Who I Am

- **Name:** Juan
- **Day job:** Data Analyst and MMM maintainer at a company that builds
  production Bayesian Marketing Mix Models
- **Stack:** R, RStudio, tidyverse, cmdstanr, brms — R-first, always
- **Stats background:** 100–200 level coursework. Strong intuition,
  gaps in formal probability theory and graduate-level methods
- **Current work context:** I maintain and contribute to a production
  Bayesian MMM pipeline. I understand the outputs and the workflow.
  I am here to own the underlying math and modeling theory.

---

## The Parallel Track — Always Running, Always First

**Statistical Rethinking** by Richard McElreath is my permanent parallel
track. I read it with coworkers as a group study. It is NOT a curriculum
course. It runs independently and takes precedence over everything else.

- Lectures: McElreath's full YouTube series (2023/2024 versions)
- R packages: `rethinking`, `cmdstanr`, `tidybayes`
- When I bring Rethinking questions: answer them directly, no preamble,
  no "great question", just engage with the content

---

## What This Repo Is

A self-directed graduate-level Bayesian statistics curriculum, designed
to be equivalent to a self-taught MS in Bayesian Statistics over 1–2 years.

Every course is anchored by:
- A real textbook (free PDF where available)
- A full YouTube lecture series tied to that textbook
- R-based exercises and notes

Pace: light (~1–2 hrs/week study time available). One course at a time.
Roughly 12–16 weeks per course. Long game is fine.

---

## Curriculum Position

See CURRICULUM.md for full detail.

**Current course:** Course 0 — Probability Foundations (Blitzstein, Stat 110)
**Current status:** Assessing — watching lectures 1–5 to determine whether
to complete the full course or advance to Course 1

---

## How We Work Together

### Session startup
- I tell you what I'm working on or paste where I left off
- You orient immediately — no recap, no cheerleading
- If I haven't left a note, ask only: "Where did we leave off?"

### My communication style
- Brief, informal, shorthand — match my energy
- I think out loud, follow the thread
- Challenge me when I'm wrong
- I want to understand deeply, not just move forward

### Code rules
- **R by default. Always.**
- Python only when a specific resource has no R equivalent (rare)
- Explain confusing lines of code line by line — never skip
- Use tidyverse style throughout
- Prefer `brms` before going raw Stan
- Prefer `cmdstanr` over `rstan`

### Explanations
- Go deep before going wide
- Connect new concepts to MMM work when relevant — that is my anchor
- Do not simplify unless I ask
- If I am missing a prerequisite, say so directly and point me to it
- Never over-explain things I already know (see below)

---

## What I Already Know — Don't Over-Explain

- Prior, likelihood, posterior — conceptually solid
- Bayes' theorem — can apply it
- MCMC — know what it does, not the full math yet
- MMM structure — adstock, saturation, media contribution, baseline
- tidyverse, ggplot2, dplyr, purrr — fluent
- R Markdown / Quarto — comfortable
- Basic probability — distributions by name, not always by deep mechanics

---

## What I Am Building

- Formal probability theory — joint distributions, conditional expectation,
  moment generating functions, Markov chain foundations
- Conjugate priors and why they matter computationally
- Full Stan fluency — syntax, debugging, efficiency
- Variational inference
- Hierarchical model construction from scratch
- Bayesian time series modeling
- Causal identification strategies for MMM

---

## Repo Structure

```
/
├── CLAUDE.md              <- This file. Read every session.
├── CURRICULUM.md          <- Full course map with resources and progress
├── SESSION.md             <- Notes from last session — read if present
├── course-0-foundations/  <- Blitzstein Stat 110
├── course-1-bayes-rules/  <- Johnson, Ott & Dogucu — Bayes Rules!
├── course-2-ros/          <- Gelman, Hill & Vehtari — Regression and Other Stories
├── course-3-bda3/         <- Gelman et al. — Bayesian Data Analysis 3rd ed.
├── course-4-timeseries/   <- Hyndman & Athanasopoulos — fpp3 + Bayesian layer
└── course-5-causal/       <- Huntington-Klein — The Effect
```
