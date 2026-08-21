### Tanmay Jain

Full-stack engineer, eleven years building and running production systems.
Available for freelance work in **React, Python and PostgreSQL**.

I tend to care about the unglamorous parts: imports that tell you what they are
about to do before they do it, migrations that can be reversed, error messages
that name the row and the column, and decisions that stay visible after the
person who made them has moved on.

---

#### ReturnDesk — returns reconciliation

A DTC apparel brand ran its returns on one Excel file and could not tell how
much money was walking out of the door. Three monthly exports — refunds, the
warehouse scan log, the courier invoice — matched against each other, with
everything that does not reconcile in one queue sorted by value.

On seven months of data it surfaces **$79,828** the spreadsheet could not see:
refunds for parcels that never arrived, customers who returned goods and were
never paid, and refunds issued twice.

[Live demo](https://returndesk-web.onrender.com) ·
[Source](https://github.com/tanmayjain70/returndesk) ·
sign in with `ops@harrowvine.demo` / `demo-password`

#### ServiceLine — multi-tenant SaaS

Field service scheduling for HVAC and plumbing contractors. Tenant isolation is
enforced by PostgreSQL row-level security rather than by remembering a `WHERE`
clause in every query — so the failure that usually leaks one customer's data
into another customer's screen is not possible to write.

[Live demo](https://serviceline-web.onrender.com) ·
[Source](https://github.com/tanmayjain70/serviceline) ·
sign in with `owner@northline.demo` / `demo-password`

> Both are personal projects, built against a written brief rather than paid
> client work. The briefs, the scoping questions that changed them, and the
> trade-offs behind each decision are documented in the repositories — that
> part is usually more interesting than the code.

---

React · TypeScript · Python (FastAPI, SQLAlchemy) · PostgreSQL · Docker ·
GitHub Actions

📫 tanmayjain70@gmail.com

<sub>The demos are on a free tier that sleeps when idle, so the first sign-in
can take up to a minute while the server wakes.</sub>
