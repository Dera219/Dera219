## Chidera Onyebu

CS & Applied Mathematics at the University of Maryland (2028). I build systems that have to be
right when nobody is watching — and I spend most of my time on the part where they're wrong.

The through-line: a result that looks good is a claim, not a fact. A ledger that balances in the
demo, an in-sample Sharpe, a validation accuracy, an agent that says "no" to a jailbreak — each
one is a number you can get by accident. So I try to make the property hold by construction
rather than by discipline, then write the test that fails if anyone removes it.

---

**[ToolBelt](https://github.com/Dera219/toolbelt)** — a two-sided gig marketplace, built and
deployed end to end: a 7,800-line FastAPI/PostgreSQL API and a 4,300-line TypeScript Expo client
shipping from one codebase to iOS, Android, and web. It ran on its own domain over TLS until I
retired the hosting in September 2026, rather than keep renting a demo with no users. I built it
to be correct, not to be operated. The interesting half is the money. Every money-moving Stripe call is journaled on a
second connection *before* the call goes out, because Stripe prunes idempotency keys after 24
hours and a retried refund past that window is not a retry — it's a second real charge. Three of
the defects I fixed were invisible to a mocked test suite and only appeared against the live API,
and all three lived in the same gap: between telling a provider to move money and recording that
you did. FastAPI · PostgreSQL · TypeScript · Stripe · Docker.

**[crucible](https://github.com/Dera219/crucible)** — a cross-sectional research platform whose
causality checker proves a signal cannot see the future: perturb every observation after time
*t*, recompute, assert nothing before *t* moved. That catches full-sample normalisation, the
lookahead bug that survives review because it looks like the textbook. I logged every defect
found *after* the tests were already green — thirteen, and twelve of them made results look
better than reality. Research bugs are asymmetric that way: one that loses information gets
noticed when the strategy stops working, one that adds information looks like a discovery, and
nobody debugs a good result. 408 tests, ruff and mypy strict clean.

**[TradeDesk](https://github.com/Dera219/tradedesk)** — a conversational trading agent whose
confirmation gate is enforced by the graph's shape. There is no edge from proposing an order to
filling one, so a model that decides to skip the confirmation has nowhere to go; a test fails if
anyone adds the shortcut. Authorization is Python decorators that raise, not instructions the
model can be argued out of. 18 adversarial scenarios assert on behavior — the strongest check is
a spy recording that the broker was never called, which is a different claim from "the agent
refused." Python · LangGraph · FastAPI · RAG · MCP. AI.Accelerate FY26 capstone.

**[Apex](https://github.com/Dera219/apex-trading-agent)** — an event-driven backtester where
lookahead bias is structurally hard to introduce, with a cost model for commission, spread, and
market impact, and walk-forward validation. Its own demo beats buy-and-hold in-sample and loses
out-of-sample. I left that in: it's the framework demonstrating the thing it exists to catch.

**[Nutrition5k audit](https://github.com/Dera219/ai4all-ml-project)** — a calorie CNN, and an
audit that changed how the team's numbers should be read. The split passed a dish-ID overlap
check but leaked at the capture-session level. A controlled experiment across 5 seeds and 2
architectures put the inflation at ~3 accuracy points. On a clean session-grouped split the model
reaches ~74%, 2.2× the majority baseline — lower than the original number, and the one I'd defend.

---

Mentoring CS students through **ColorStack** and **Alpha Lambda Delta** — explaining an idea
cleanly is still the fastest way to find the hole in it. Grew up in Lagos, Nigeria.

If you're building something where correctness outlives the demo — money that has to reconcile, a
model that has to generalize, an agent that has to stay inside its limits — I'd like to talk.

**[Portfolio](https://dera219.github.io/dera-portfolio/)** ·
**[LinkedIn](https://www.linkedin.com/in/chideraonyebu/)** ·
conyebu@terpmail.umd.edu
