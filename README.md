# Rudra Patel

Cognitive Science (Machine Learning & Neural Computation) student at UC San Diego and founder of [DealerScope AI](https://dealerscope.app).

---

## Projects

### [DealerScope AI](https://github.com/Rudra-C-Patel/dealerscope-ai) · live at [dealerscope.app](https://dealerscope.app)

Revenue intelligence for car dealerships. It reads DMS and CRM exports and points to the records worth a phone call: leads that got one call and then nothing, declined service work nobody followed up on, and leases running to term with no outreach. Each finding comes with a generated call script.

- **Every dealership exports data differently.** A universal CSV adapter maps Tekion, DealerSocket, CDK and arbitrary headers to one schema, and sends genuinely ambiguous columns to an LLM.
- **It won't make up a score.** The close-probability model is Naive Bayes trained on the store's own closed-versus-lost leads. With fewer than 20 closed deals, it shows labeled industry priors instead of a per-lead score.
- **A test enforces honesty.** `test_no_fabricated_data.py` fails the build if an endpoint returns figures that no data supports.

`Python 3.11` `FastAPI` `React 19` `Vite` `NVIDIA NIM` `Railway` `Vercel`. The repo is a public showcase; the production source is private.

### [Momentum strategy walk-forward test](https://github.com/Rudra-C-Patel/trading-bot)

An event-driven backtester and walk-forward harness over 5,309 US-listed stocks (4,317 with usable price history), 2020–2024. The result is negative, and the harness is what caught it.

- An in-sample backtest showed **+10.5% CAGR**. Most of that came from two filter bugs. With the filters fixed, the same backtest earns **−0.7%**.
- Across 7 folds where the cutoff was picked on past data only, the strategy earned **−3.9% CAGR** out of sample (13 trades).
- Under the same protocol, all **5** follow-up strategy and instrument tests also failed out of sample. No capital was risked; it is paper trading only.

`Python` `pandas` `pytest` (35 unit tests)

### [Data pipeline and web-scraping agent](https://github.com/Rudra-C-Patel/internship-automation-agent) (retired)

A pipeline that collected listings from 7 job-board sources, normalized them to one schema, ranked them with an LLM, and processed the queue overnight with Playwright, capped at 8 records per night. It ran as systemd services on a self-hosted Ubuntu box until that host was decommissioned in June 2026, and the source code was lost with it. The repo keeps the architecture record and the lesson.

`Python` `Playwright` `NVIDIA NIM` `systemd` `Tailscale`

---

## Background

- UC San Diego, B.S. Cognitive Science (ML & Neural Computation), expected 2028
- Santiago Canyon College, A.S. Math & Sciences with Honors
- IT Intern, HSI STEM (Project RAISE), Nov 2025 – Aug 2026
- Google Cybersecurity and Google Data Analytics certificates
- English, Gujarati, Hindi, Spanish
- Permanent Resident, no sponsorship required

**Tools:** Python, JavaScript, SQL, C++, Bash · FastAPI, pandas, pytest · React, Vite, Tailwind · Linux, Railway, Vercel, GitHub Actions

---

## Contact

[LinkedIn](https://linkedin.com/in/rudra-patel-a0a115354) · [rcppatel24@gmail.com](mailto:rcppatel24@gmail.com) · [dealerscope.app](https://dealerscope.app)
