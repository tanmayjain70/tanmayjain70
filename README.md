### Tanmay Jain

**Full-stack engineer — React · Python · PostgreSQL**
Eleven years building and running production systems. Available for freelance work.

I care about the unglamorous parts: migrations that can be reversed, error
messages that name the row and the column, permissions the server enforces
rather than the interface hiding, and decisions that stay legible after the
person who made them has moved on.

---

## 🚀 Projects

Both are live. Both have published logins. Neither asks you to take my word for
anything.

| Project | The problem | What it proves | |
|---|---|---|---|
| **ReturnDesk**<br>Returns reconciliation | A DTC apparel brand ran returns on one spreadsheet and could not tell how much money was leaving. | Matches three monthly files that disagree — refunds, warehouse scans, courier invoices — into one queue sorted by money at risk. Surfaced **$79,828** across 1,213 cases in about four seconds. | [Demo](https://returndesk-web.onrender.com) · [Code](https://github.com/tanmayjain70/returndesk) |
| **ServiceLine**<br>Multi-tenant SaaS | Field service scheduling sold to many contractor companies, where none may ever see another's data. | Tenant isolation enforced by PostgreSQL row-level security instead of a `WHERE` clause you have to remember. Ten tables protected; the API refuses to boot if the database is not enforcing it. | [Demo](https://serviceline-web.onrender.com) · [Code](https://github.com/tanmayjain70/serviceline) |

**Sign in and try to break them**

| | |
|---|---|
| ReturnDesk | `ops@harrowvine.demo` / `demo-password` — or sign in as the coordinator and try to resolve a case over $250. The button is right there; the API returns 403. |
| ServiceLine | `owner@northline.demo` / `demo-password` — then sign in as `owner@buckeye.demo`, take a record ID from the first company and request it. You get 404, not 403: confirming the row exists would leak that it does. |

> Both are personal projects, built solo against a written brief rather than paid
> client work. Each repository carries the brief, the scoping questions that
> changed it, and what was cut to fit the budget.

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

**Data** — PostgreSQL 17/18 · row-level security · schema design · reconciliation and reporting

**Delivery** — Docker · GitHub Actions · Neon · Render · infrastructure as code

**Also** — REST API design · RBAC and multi-tenancy · Excel/PDF generation · scheduled jobs

---

## 📋 What the two projects actually demonstrate

| | ReturnDesk | ServiceLine |
|---|---|---|
| Tests | 58, 79% coverage | 112, green in CI |
| End-to-end checks | 21 against a running server | 27 against the live deployment |
| Hard part | Matching three sources that disagree, and being honest about what does not reconcile | Isolation the database enforces, and scheduling across timezones |
| Worth a look | The exception queue sorted by money at risk | The dispatch board — drag to assign, with each job's timezone on the card |

The second one is less obvious than it sounds. A booked window is a promise in
the customer's local time, so it is stored twice — once as written, once as UTC
instants — because two jobs in different timezones can overlap on a wall clock
while not overlapping in reality. One target customer works both sides of the
Ohio/Indiana line, where half of Indiana observes Central.

---

## 💼 Background

- **Eleven years** building and running production software in a large engineering organisation
- Now working with founders and small teams who want that standard applied to their product
- Most useful on the things that are expensive to get wrong later: multi-tenant architecture, access control, data modelling, and integrations that have to survive real-world failure
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
