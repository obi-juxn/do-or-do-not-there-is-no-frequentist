# CURRICULUM.md — Self-Directed MS in Bayesian Statistics

**Owner:** Juan
**Started:** 2026
**Target:** Graduate-level Bayesian Statistics expertise over 1–2 years
**Pace:** ~1–2 hrs/week. One course at a time. Long game.
**Parallel track:** Statistical Rethinking (McElreath) — always running, always first

---

## Progress Tracker

| # | Course | Textbook | Status |
|---|--------|----------|--------|
| 0 | Probability Foundations | Blitzstein & Hwang — *Introduction to Probability* | 🔄 In progress |
| 1 | Bayesian Core | Johnson, Ott & Dogucu — *Bayes Rules!* | 🔲 Not started |
| 2 | Bayesian Regression & GLMs | Gelman, Hill & Vehtari — *Regression and Other Stories* | 🔲 Not started |
| 3 | Graduate Bayesian Flagship | Gelman et al. — *Bayesian Data Analysis* (BDA3) | 🔲 Not started |
| 4 | Time Series | Hyndman & Athanasopoulos — *fpp3* + Bayesian layer | 🔲 Not started |
| 5 | Causal Inference | Huntington-Klein — *The Effect* | 🔲 Not started |

Status key: 🔄 In progress · ✅ Complete · ⏭ Skipped (too easy) · 🔲 Not started

---

## Course 0 — Probability Foundations

**Textbook:** Joseph K. Blitzstein & Jessica Hwang, *Introduction to Probability*, 2nd ed., CRC Press, 2019
**Free PDF:** https://probabilitybook.net (author-sanctioned)
**Print:** ~$45 used / ~$110 new

**YouTube:** Harvard Stat 110 — full 34-lecture series by Blitzstein himself
https://www.youtube.com/playlist?list=PLLVplP8OIVc8EktkrD3Q8td0GmId7DjW0
Interactive edX companion (free to audit): https://www.edx.org/course/introduction-to-probability

**Why this course:**
Builds the formal probability foundation that everything else rests on.
Joint distributions, conditional expectation, Beta/Gamma/Poisson mechanics,
and Markov chains — which are the mathematical substrate of MCMC.
The Beta distribution chapter alone is worth the price of admission
given how central Beta priors are in MMM work.

**Prerequisites:** Single-variable calculus. Basic algebra.

**R integration:** End-of-chapter simulation sections use R throughout.

**Decision:** Doing the full course. Pursuing HarvardX certification via edX.
Free audit: https://www.edx.org/course/introduction-to-probability

**Key topics:**
- Counting, sample spaces, probability axioms
- Conditional probability, law of total probability
- Bayes' theorem (the formal version)
- Random variables — discrete and continuous
- Named distributions: Binomial, Geometric, Poisson, Exponential, Normal, Beta, Gamma
- Why these distributions arise naturally and how they relate to each other
- Joint distributions, marginal distributions
- Conditional expectation and the law of total expectation
- Variance, covariance, correlation
- Moment generating functions
- Markov chains (direct foundation of MCMC)

**Notes / progress log:**
- [ ] Watched lectures 1–5 (assessment)
- [ ] Decision: full course or skip to Course 1
- [ ] Chapter notes in /course-0-foundations/

---

## Course 1 — Bayesian Core

**Textbook:** Alicia A. Johnson, Miles Q. Ott & Mine Dogucu, *Bayes Rules! An Introduction to Applied Bayesian Modeling*, 1st ed., CRC Press, 2022
**Free online:** https://www.bayesrulesbook.com (CRC-sanctioned, full book)
**Print:** ~$55–$70 (use code BRD20 for 20% off at CRC)

**YouTube:** Two options — use both
1. Mine Dogucu's UC Irvine Stats 115 course (co-author taught):
   https://mdogucu.github.io/stats115-su21-website/
2. R4DS community book club — complete chapter-by-chapter walkthrough:
   Search "Bayes Rules r4ds book club" on YouTube
   (entries titled "bayes_rules01 1", "bayes_rules02 1", etc.)

**Why this course:**
Modern (2022), R-first, free, and pitched at exactly your level —
past intro stats, building toward graduate methods. Uses rstan/rstanarm.
Covers the full Bayesian workflow: prior selection, likelihood, posterior,
MCMC diagnostics, model comparison. Directly complements Statistical Rethinking
rather than duplicating it.

**Prerequisites:** Intro statistics, basic calculus, basic R. Course 0 or equivalent.

**R packages:** `bayesrules`, `rstan`, `rstanarm`, `tidyverse`, `tidybayes`

**Key topics:**
- Formal Bayesian structure — prior, likelihood, posterior
- Conjugate priors — Beta-Binomial, Gamma-Poisson, Normal-Normal
- Why conjugacy matters computationally
- MCMC and posterior simulation
- Posterior predictive checks
- Bayesian regression — simple, multiple, logistic
- Hierarchical models (introductory)
- Model evaluation and comparison

**Notes / progress log:**
- [ ] Chapter notes in /course-1-bayes-rules/

---

## Course 2 — Bayesian Regression & GLMs

**Textbook:** Andrew Gelman, Jennifer Hill & Aki Vehtari, *Regression and Other Stories*, Cambridge University Press, 2020
**Free PDF:** https://users.aalto.fi/~ave/ROS.pdf (author-sanctioned)
**Print:** ~$40–$50 paperback / ~$60–$80 hardcover

**YouTube:** No dedicated lecture series for ROS.
**Surrogate video tracks (use both):**
1. McElreath's Statistical Rethinking 2023 lectures — already your parallel track,
   covers the same GLM and causal inference content
2. Aki Vehtari's Aalto BDA lectures (Course 3 below) — Vehtari is a ROS co-author
   and his regression lectures are direct complements

**Why this course:**
ROS is the most practical regression textbook written from a Bayesian-workflow
perspective. It uses rstanarm's stan_glm() throughout — pure R, no raw Stan needed.
Covers everything from simple linear regression through logistic, count models,
and causal inference framing. Direct applied relevance to MMM regression structure.

**Prerequisites:** Courses 0–1 or equivalent. Basic linear algebra helpful.

**R packages:** `rstanarm`, `tidyverse`, `bayesplot`, `loo`

**Key topics:**
- Linear regression — estimation, uncertainty, simulation
- Logistic regression and GLMs
- Poisson and overdispersed count models
- Model building and checking
- Causal inference framing — treatment effects, confounding
- Prediction and extrapolation
- Multilevel regression (introductory)

**Notes / progress log:**
- [ ] Chapter notes in /course-2-ros/

---

## Course 3 — Graduate Bayesian Flagship (BDA3)

**Textbook:** Andrew Gelman, John Carlin, Hal Stern, David Dunson, Aki Vehtari & Donald Rubin, *Bayesian Data Analysis*, 3rd ed., CRC Press, 2013
**Free PDF:** https://stat.columbia.edu/~gelman/book/ (CRC-sanctioned as of Sept 2025)
**Print:** ~$60–$80 used / ~$100 new

**YouTube:** Aki Vehtari's Aalto University BDA course — the gold standard
Full playlist: https://www.youtube.com/playlist?list=PLBqnAso5Dy7O0IVoVn2b-WtetXQk5CDk6
Course hub (syllabus, slides, assignments, R demos): https://avehtari.github.io/BDA_course_Aalto/
Use the 2023 version — most complete recording set.

**Why this course:**
The canonical graduate Bayesian text. This is the crown jewel of the curriculum.
Covers the full theoretical and computational machinery — posterior inference,
hierarchical models, model checking, Stan workflow, approximate methods.
Vehtari's lectures are co-author-taught and directly keyed to the book chapters.
Free book + free lectures + CC-licensed slides + R/Stan demos = the McElreath
experience at graduate level.

**Prerequisites:** Courses 0–2. Multivariable calculus. Linear algebra. Solid R/Stan basics.

**R packages:** `cmdstanr`, `brms`, `loo`, `bayesplot`, `posterior`

**Key topics:**
- Single and multi-parameter models
- Posterior simulation and MCMC theory
- Hierarchical / multilevel models (deep treatment)
- Model checking and posterior predictive checks
- Bayesian model comparison (LOO-CV, WAIC)
- Stan workflow — writing, debugging, diagnosing models
- Approximate inference (Laplace, variational, EP)
- Gaussian processes (introduction)
- Decision analysis

**Notes / progress log:**
- [ ] Chapter notes in /course-3-bda3/

---

## Course 4 — Time Series

**This course has two layers — complete them in order.**

### Layer A: Time Series Foundations

**Textbook:** Rob Hyndman & George Athanasopoulos, *Forecasting: Principles and Practice*, 3rd ed.
**Free online:** https://otexts.com/fpp3 (full book, no paywall)
**Print:** ~$20–$40

**YouTube:** Full author-produced video series embedded in the book and on YouTube
Playlist: https://www.youtube.com/playlist?list=PLyCNZ_xXGzpm7W9jLqbIyBAiSO5jDwJeE

**Why this layer:**
fpp3 is the only time series resource with a real textbook + full YouTube pairing.
Largely frequentist (ETS, ARIMA, regression with ARIMA errors) but the best
conceptual foundation for time series structure before going Bayesian.
Uses the fable/feasts/tsibble R ecosystem — tidy time series.

**R packages:** `fable`, `feasts`, `tsibble`, `tidyverse`

### Layer B: Bayesian Time Series

**Primary textbook:** Hagiwara, *Time Series Analysis for the State-Space Model with R/Stan*, Springer, 2021
**Cost:** ~$60–$90 — no free PDF available. Only paid option in this curriculum.
**YouTube:** None — no dedicated lecture series exists.

**Supplement with (all free):**
- Betancourt's state-space model case studies: https://betanalpha.github.io/writing/
- ATSA book chapter on Stan for Bayesian time series: https://atsa-es.github.io/atsa-labs/
- bsts package vignettes (Scott/Varian Bayesian structural time series — directly relevant to MMM)
- PyMC-Marketing docs for Bayesian MMM specifics: https://www.pymc-marketing.io/

**Why this layer:**
State-space models, Kalman filter, particle filter, dynamic regression —
these are the Bayesian time series tools that connect directly to MMM
and carryover/adstock modeling.

**Key topics (both layers):**
- Time series decomposition — trend, seasonality, cycles
- Exponential smoothing (ETS)
- ARIMA — identification, estimation, diagnostics
- Dynamic regression / regression with ARIMA errors
- State-space models and the Kalman filter
- Bayesian structural time series (bsts)
- Particle filter (introduction)
- Application to MMM — adstock, carryover, saturation in time series framing

**Notes / progress log:**
- [ ] Layer A notes in /course-4-timeseries/layer-a/
- [ ] Layer B notes in /course-4-timeseries/layer-b/

---

## Course 5 — Causal Inference

**Textbook:** Nick Huntington-Klein, *The Effect: An Introduction to Research Design and Causality*, CRC Press, 2022 (2nd ed. 2024)
**Free online:** https://theeffectbook.net (author-sanctioned, full book)
**Print:** ~$50–$60

**YouTube:** Full author-produced series on Dr. HK's YouTube channel
Channel: https://www.youtube.com/c/NickHuntingtonKlein
Linked from the book's main page — covers all major identification strategies

**Supplement with:**
- Scott Cunningham, *Causal Inference: The Mixtape* — free at https://mixtape.scunning.com
  Use for DiD, synthetic control, and RDD depth alongside The Effect

**Why this course:**
Causal inference is the missing layer in most Bayesian curricula and the one
most directly relevant to MMM — which is fundamentally a causal attribution problem.
DAGs, identification, DiD, IV, RDD, matching — these are the tools that separate
rigorous MMM from correlation mining.

**Prerequisites:** Courses 0–3. Intro econometrics helpful but not required.

**R packages:** `tidyverse`, `fixest`, `MatchIt`, `rdrobust`, `modelsummary`

**Key topics:**
- Potential outcomes framework
- DAGs and causal diagrams
- Selection bias and confounding
- Matching and weighting
- Difference-in-differences
- Instrumental variables
- Regression discontinuity
- Event studies
- Application to MMM — lift measurement, incrementality testing

**Notes / progress log:**
- [ ] Chapter notes in /course-5-causal/

---

## Reference Archive — Vetted Alternatives

These resources were researched and verified but are not primary curriculum anchors.
Use them as depth-on-demand references or alternatives if a primary resource
doesn't click.

### Bayesian Core Alternatives

**Kruschke — *Doing Bayesian Data Analysis* (DBDA), 2nd ed.**
- The "puppy book." Very thorough, R + JAGS + Stan. ~750 pages.
- No free PDF (Elsevier). ~$50–$70 used.
- No full YouTube course — only author clip videos.
- Best use: reference for ANOVA-style designs and t-test replacements.
- Free companion: A. Solomon Kurz's brms/tidyverse recode at https://bookdown.org/content/3686/

**Ben Lambert — *A Student's Guide to Bayesian Statistics* (2018)**
- Strong YouTube course (full, chapter-aligned): https://www.youtube.com/playlist?list=PLwJRxp3blEvZ8AKMXOy0fc0cqT61GsKCG
- Book is language-agnostic (Stan only at the end — weak R workflow)
- ~$50–$60 print, no free PDF
- Best use: if video-first learning is preferred over code notebooks

### Probabilistic Programming & Stan

**Stan User's Guide + Reference Manual**
- Free: https://mc-stan.org/users/documentation/
- No textbook, no full course — but the official reference

**Michael Betancourt — case studies and writing**
- Free: https://betanalpha.github.io/writing/
- Deep conceptual treatment of Stan, HMC, prior modeling, workflow
- Best HMC intuition video: https://www.youtube.com/watch?v=jUSZboSq1zg

**Matsuura — *Bayesian Statistical Modeling with Stan, R, and Python* (Springer, 2023)**
- Most up-to-date Stan textbook. Covers CmdStanR, state-space, GPs.
- ~$60–$80. No free PDF. No YouTube course.
- Best use: Stan reference after BDA3.

### Causal Inference References

**Cunningham — *Causal Inference: The Mixtape***
- Free: https://mixtape.scunning.com
- Paid workshops exist (Mixtape Sessions on GitHub)
- No clean free YouTube series
- Best use: DiD, synthetic control, RDD depth alongside The Effect

**Hernán & Robins — *Causal Inference: What If***
- Free PDF: https://miguelhernan.org/whatifbook (live, periodically updated)
- No full YouTube course (HarvardX edX content only)
- R code companion: https://remlapmot.github.io/cibookex-r/
- Best use: IPW, marginal structural models, g-methods — advanced causal

### Multilevel / Hierarchical Models

**Gelman & Hill — *Data Analysis Using Regression and Multilevel/Hierarchical Models* (ARM)**
- Pre-Stan (uses lme4 and BUGS). Gelman now recommends ROS over it.
- ~$40–$60 used. No free PDF. No YouTube course.
- Best use: historical reference — BDA3 + ROS cover this better now.

### Bayesian MMM Ecosystem (No Textbook — Papers + Docs)

- Jin et al. (Google, 2017) — "Bayesian Methods for MMM with Carryover and Shape Effects"
  https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/46001.pdf
- PyMC-Marketing docs: https://www.pymc-marketing.io/
- Juan Orduz MMM case studies: https://juanitorduz.github.io/
- Meta Robyn (R-based semi-Bayesian MMM): https://robyn.ai/
- bsts package (R): Scott/Varian Bayesian structural time series

---

*Last updated: 2026*
*Curriculum designed by Juan with Claude (Anthropic) as strategic collaborator*
