# Rudra Patel

Solo founder. I build and run production software while studying at UC San Diego.

San Diego, CA. Cognitive Science with a Machine Learning & Neural Computation specialization at UC San Diego.

---

## DealerScope AI

Revenue intelligence for car dealerships. Live at **[dealerscope.app](https://dealerscope.app)**.

Dealerships sit on DMS and CRM exports full of revenue nobody actioned: leads that never got a second call, declined service work that was never followed up, leases running to term with no outreach. DealerScope ingests those exports, surfaces the specific records worth a phone call, and generates a call script for each one.

**Stack**

| Layer | Technology |
|---|---|
| Backend | Python 3.11, FastAPI, file-based JSON storage, Railway |
| Frontend | React 19, Vite 8, React Router v7, Vercel |
| AI | NVIDIA NIM API for call script generation, with deterministic fallbacks when no model is available |
| Auth | Bearer tokens, bcrypt hashing with transparent legacy rehash |
| Notifications | Telegram Bot API, SMTP |

Things I had to solve that were harder than they looked:

- **Every dealership exports data differently.** Tekion, DealerSocket, CDK and Reynolds all name the same field five different ways. The CSV adapter maps unknown headers to a canonical schema by keyword matching, then falls back to LLM inference for genuinely ambiguous columns.
- **Small stores have no training data.** The lead close-probability model is Naive Bayes trained on the store's own closed-versus-lost history. Under 20 closed deals it refuses to pretend, returning stated industry priors with an explicit disclaimer instead of a made-up score.
- **An analytics product that invents numbers is worthless.** The test suite has a dedicated `test_no_fabricated_data.py` that fails the build if an endpoint starts returning figures no data supports.

Public showcase repo: **[dealerscope-ai](https://github.com/Rudra-C-Patel/dealerscope-ai)**. Production source is private.

---

## Quantitative Strategy Research Platform

**[trading-bot](https://github.com/Rudra-C-Patel/trading-bot)**: an event-driven backtester and 7-fold walk-forward validation harness over ~5,300 US stocks. Its main result is a negative one: a 10.5% in-sample CAGR fell to -0.8% out of sample, and 8 strategy configurations were rejected before any capital was deployed. Paper trading only.

---

## Tools I reach for

```
languages   Python, JavaScript, SQL, C++, Bash
backend     FastAPI, uvicorn, pandas, pytest
frontend    React, Vite, Tailwind
infra       Linux, Railway, Vercel, systemd, Tailscale, GitHub Actions
ai          NVIDIA NIM, Playwright, scikit-style modeling by hand
```

---

## Background

- UC San Diego, B.S. Cognitive Science (ML & Neural Computation), expected 2028
- Santiago Canyon College, A.S. Math & Sciences with Honors
- HSI STEM Intern, Student Help Desk (Project RAISE), Santiago Canyon College
- Google Cybersecurity and Google Data Analytics certificates
- English, Gujarati, Hindi, Spanish
- Permanent Resident, no sponsorship required

---

## Contact

[LinkedIn](https://linkedin.com/in/rudra-patel-a0a115354) · [rcppatel24@gmail.com](mailto:rcppatel24@gmail.com) · [dealerscope.app](https://dealerscope.app)
