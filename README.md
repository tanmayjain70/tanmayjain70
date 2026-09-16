### Tanmay Jain

**Full-stack engineer — React · Python · PostgreSQL**
Twelve years building and running production systems.

I care about the unglamorous parts: migrations that can be reversed, error
messages that name the row and the column, permissions the server enforces
rather than the interface hiding, and decisions that stay legible after the
person who made them has moved on.

---

## 🚀 Projects

All four are live, each with a published login. None of them asks you to take
my word for anything.

| Project | The problem | What it proves | |
|---|---|---|---|
| **Footnote**<br>Document question answering | A property firm's chat-with-your-PDFs tool said a lease's break notice was three months. It was six. They acted on it and were locked in for another five years. | Every answer cites the page it came from, and each citation is checked against the passage that was actually retrieved. With nothing verified to point at, it says **not answerable** instead of guessing. Hybrid search in PostgreSQL — pgvector plus full-text — a register of seventeen lease terms a person confirms, and an evaluation harness: the right page is found **94%** of the time. | [Demo](https://footnote-web-xgu5.onrender.com) · [Code](https://github.com/tanmayjain70/footnote) |
| **ReturnDesk**<br>Returns reconciliation | A DTC apparel brand ran returns on one spreadsheet and could not tell how much money was leaving. | Matches three monthly files that disagree — refunds, warehouse scans, courier invoices — into one queue sorted by money at risk. Surfaced **$79,828** across 1,213 cases in about four seconds. | [Demo](https://returndesk-web.onrender.com) · [Code](https://github.com/tanmayjain70/returndesk) |
| **ServiceLine**<br>Multi-tenant SaaS | Field service scheduling sold to many contractor companies, where none may ever see another's data. | Tenant isolation enforced by PostgreSQL row-level security instead of a `WHERE` clause you have to remember. Ten tables protected; the API refuses to boot if the database is not enforcing it. | [Demo](https://serviceline-web.onrender.com) · [Code](https://github.com/tanmayjain70/serviceline) |
| **Driftwatch**<br>Integration integrity | A roaster's sync to Shopify and Stripe stopped in February. Nobody noticed for eleven days: the dashboards kept showing numbers, just the same numbers. | Signed webhook ingest that survives duplicate delivery, a resumable backfill paced to the providers' rate limits, and a drift check that names the specific missing records — and reports **unknown** rather than clean when it cannot reach a provider. | [Demo](https://driftwatch-web.onrender.com) · [Code](https://github.com/tanmayjain70/driftwatch) |

**Sign in and try to break them**

| | |
|---|---|
| Footnote | `director@hallampryce.demo` / `demo-password` — ask when a lease ends, then ask for the landlord's bank details. The first comes back citing the page; the second comes back *not answerable*, with nothing cited. Then sign in as `manager@hallampryce.demo` and open a document from the confidential portfolio: 404. |
| ReturnDesk | `ops@harrowvine.demo` / `demo-password` — or sign in as the coordinator and try to resolve a case over $250. The button is right there; the API returns 403. |
| ServiceLine | `owner@northline.demo` / `demo-password` — then sign in as `owner@buckeye.demo`, take a record ID from the first company and request it. You get 404, not 403: confirming the row exists would leak that it does. |
| Driftwatch | `owner@kettleford.demo` / `demo-password` — press "Simulate live traffic" and watch one webhook arrive twice and be marked a duplicate rather than applied again. Then open a drift finding: it lists the exact records that are missing. |

> All four are personal projects, built solo against a written brief rather than
> paid client work. Each brief records the scoping questions that changed it and
> what was cut to fit the budget; the public repositories carry theirs.

Footnote's public demo answers by quoting the retrieved passages rather than
calling a paid language model, so it costs nothing to try; the model integration
is one setting away.

Hosted on free tiers that sleep when idle, so **the first request can take up to
a minute** while the server wakes.

---

## 🏗️ How I build

Enforce it in the layer that cannot be bypassed · reversible migrations ·
tests that attack the thing rather than confirm it · errors that say what to do
next · the deployment pipeline on day one, not the last week · write down why,
not just what · cut scope, never rigour

---

## 🧠 Tech stack

**Backend** — Python · FastAPI · SQLAlchemy 2 · Alembic · psycopg 3 · Pydantic · pytest

**Frontend** — React 19 · TypeScript · Vite · TanStack Query · Tailwind

**Data** — PostgreSQL 17/18 · pgvector · row-level security · schema design · reconciliation and reporting

**AI & search** — retrieval-augmented generation · hybrid vector and full-text search with rank fusion · local embeddings · citation-grounded LLM answers (Anthropic API) · evaluation harnesses for retrieval quality

**Delivery** — Docker · GitHub Actions · Neon · Render · infrastructure as code

**Also** — REST API design · RBAC and multi-tenancy · webhooks, retries and idempotency · PDF ingestion · LLM cost metering and budgets · job queues in PostgreSQL · Excel/PDF generation · scheduled jobs

---

## 📋 What the projects actually demonstrate

| | Footnote | ReturnDesk | ServiceLine | Driftwatch |
|---|---|---|---|---|
| Tests | 325, 96% coverage | 58, 79% coverage | 112, green in CI | 40, 82% coverage |
| End-to-end checks | 28 against the live deployment | 21 against a running server | 27 against the live deployment | 18 against a running server |
| Hard part | Knowing when not to answer, and proving every citation points at a passage that was really retrieved | Matching three sources that disagree, and being honest about what does not reconcile | Isolation the database enforces, and scheduling across timezones | Telling "in sync" apart from "nothing reported a problem" |
| Worth a look | An answer with its cited passages beside it, and a question it declines | The exception queue sorted by money at risk | The dispatch board — drag to assign, with each job's timezone on the card | A drift finding that names the exact missing records |

ServiceLine's scheduling is less obvious than it sounds. A booked window is a
promise in the customer's local time, so it is stored twice — once as written,
once as UTC instants — because two jobs in different timezones can overlap on a
wall clock while not overlapping in reality. One target customer works both
sides of the Ohio/Indiana line, where half of Indiana observes Central.

---

## 💼 Background

- **12+ years** building and running production software in a large engineering organisation
- Now working with founders and small teams who want that standard applied to their product
- Most useful on the things that are expensive to get wrong later: multi-tenant architecture, access control, data modelling, integrations that have to survive real-world failure, and AI features whose answers have to be checkable
- Comfortable owning a piece end to end — schema, API, interface, pipeline, deploy

---

## 📫 Reach me

[tanmayjain70@gmail.com](mailto:tanmayjain70@gmail.com)

---

<!-- ─────────────────────────────────────────────────────────────────────────
     GITHUB STATS CARD — commented out on purpose.

     github-readme-stats is a free third-party service on Vercel and it was
     returning 503 on every attempt when this was written. A broken image at the
     bottom of a profile is worse than no image, and nobody notices their own
     profile is broken because their browser has the old one cached.

     To turn it on, delete this comment's opening and closing lines. Check it
     renders in a private window afterwards, and check again occasionally --
     when the service is rate-limited it fails silently.

![Tanmay's GitHub stats](https://github-readme-stats.vercel.app/api?username=tanmayjain70&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&hide_title=true)

     ───────────────────────────────────────────────────────────────────────── -->

## Available for work

Contract and freelance — billing and reconciliation, multi-tenant SaaS, data migrations, document AI with verifiable answers, and inherited codebases that need to become safe to change.

https://www.linkedin.com/in/tanmayjain70/ · https://www.upwork.com/freelancers/tanmayjain · tanmayjain70@gmail.com
