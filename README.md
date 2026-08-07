## Chidera Onyebu

CS & Applied Mathematics at the University of Maryland (2028). I build systems that make
decisions under uncertainty — and I spend most of my time on the part where they're wrong.

The through-line: a result that looks good is a claim, not a fact. An in-sample Sharpe, a
validation accuracy, an agent that says "no" to a jailbreak — each one is a number you can get
by accident. I care about the harness that tells you which ones you got on purpose.

---

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

If you're building systematic strategies and want someone who treats an out-of-sample loss as the
most useful result in the room, I'd like to talk.

**[Portfolio](https://dera219.github.io/dera-portfolio/)** ·
**[LinkedIn](https://www.linkedin.com/in/chideraonyebu/)** ·
conyebu@terpmail.umd.edu
