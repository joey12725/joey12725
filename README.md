### Joey Hersh · Agentic Systems Engineer

I build AI agents that work inside clear limits and show proof when they finish.

By day I'm a **Data Engineer III at USAA**, delivering regulated credit-risk data (Snowflake, dbt, Python) where every change has to pass an audit. I also founded **[Guadalupe Automation](https://guadalupeautomation.com)**, where I build agentic systems for operations-heavy businesses. At home, my own agent platform runs nonstop on a server I run myself: a planner, workers and a verifier, pgvector memory, and a self-hosted project board the agents report to. It logged 1,002 scheduled runs in one 18-hour stretch.

**How I build agents**

- Acceptance tests come first.
- Code does the deterministic work. The model handles judgment calls.
- Each agent gets the narrowest permissions that still let it finish the job.
- "Done" needs evidence: a test run, a diff, a readback from production.
- A person reviews anything with real consequences.

### Selected work

| Project | What it does |
|---|---|
| [**directive**](https://github.com/joey12725/directive) | Agent orchestration on a real project board. A PM agent plans the work, dispatches Claude Code, Codex, Gemini CLI and OpenCode workers within compute budgets, and checks their output. About 17k lines of Django, Celery, TypeScript and React. |
| [**peerpass**](https://github.com/joey12725/peerpass) | Scoped, expiring, revocable passes that let other people's agents talk to yours over A2A, MCP, HTTP, Slack, Discord, Telegram and Matrix, with a full audit trail. |
| [**splice**](https://github.com/joey12725/splice) | Plain-English prompts become cached, contract-checked Python functions that run in a hardened sandbox (seatbelt, bubblewrap, Docker) and repair themselves when they break. |
| [**inbox-recall**](https://github.com/joey12725/inbox-recall) | Hybrid semantic and keyword search over every chat you've ever had, served to your agents over MCP. Postgres and pgvector. |
| [**bookworm**](https://github.com/joey12725/bookworm) | A folder of ebooks becomes a citable knowledge base: BM25 plus vector search, grounded answers with chapter and page citations, and an MCP server, all in one DuckDB file. |
| [**focusgroup**](https://github.com/joey12725/focusgroup) | A focus group in your terminal. Statistically controlled AI personas, interviewed in parallel across several model families, with split tests and a Go / No-Go verdict. |
| [**in-the-know**](https://github.com/joey12725/in-the-know) | A weekly local-events newsletter written for one reader at a time, using shared LLM research, Spotify and Calendar context, and a reply-to-steer feedback loop. FastAPI and Next.js. |
| [**youtube-watch-predictor**](https://github.com/joey12725/youtube-watch-predictor) | Predicts which feed videos get watched: seven baselines, channel-held-out evaluation and bootstrap confidence intervals, with an honest look at leakage. |

Hardware and play: [maskcast](https://github.com/joey12725/maskcast) (an LED mask driven by real-time emotion recognition), [wakeword-lab](https://github.com/joey12725/wakeword-lab), [minipupper-operator](https://github.com/joey12725/minipupper-operator) (ROS 2 SLAM), [Arcade-Relay](https://github.com/joey12725/Arcade-Relay), [bubblelink](https://github.com/joey12725/bubblelink), [firesight](https://github.com/joey12725/firesight), [arrdio](https://github.com/joey12725/arrdio).

### Track record

- **USAA:** about 26M records a day through production pipelines. Backfilled 19 years of credit data (2006–2025) without interrupting reporting, and shipped a FICO 10T data asset for CECL on a regulatory deadline. I teach agentic development to my team.
- **USAA, 2023:** built an offline benefits assistant (RAG on ChromaDB and Falcon-40B) and demoed it to hundreds of employees.
- **ReCap Budget:** fine-tuned a GPT-3 classifier on 40,000 receipt items across 100+ categories (85%+ accuracy) and got structured JSON out of LLMs before function calling existed. Raised $46K cash plus about $60K in kind.
- **Fit & Flourish:** an automated Meta Ads pipeline that generated, tested and culled creative daily. It brought in 40,000 leads and cut cost per lead from $2.19 to $0.29.

### Stack

**Agents:** Claude Code · Codex · OpenCode · Gemini CLI · MCP · A2A · OpenRouter · AWS Bedrock
**Data:** Python · SQL · Postgres + pgvector · DuckDB · Snowflake · dbt · Kafka
**Ship:** TypeScript · Next.js · FastAPI · Django · Docker · AWS · Vercel

[Resume](https://resume.joeyhersh.com) · [LinkedIn](https://www.linkedin.com/in/joey-hersh) · me@joeyhersh.com
