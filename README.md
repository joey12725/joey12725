## Hey, I'm Joey.

By day I'm a data engineer at USAA shipping regulated credit-risk pipelines (~26M records a day, the kind where auditors actually read your diffs) and helping the team figure out how to build with agents. By night I run [Guadalupe Automation](https://guadalupeautomation.com) (building agent systems for real businesses) and babysit twelve agent environments on my own hardware so they don't burn my house down.

Check out **[resume.joeyhersh.com](https://resume.joeyhersh.com)** for the full resume, architecture write-ups, and receipts (including the slightly embarrassing math behind ~250B tokens across basically every model and harness since GPT-2, [here's how I count](https://resume.joeyhersh.com/evidence/)).

### How I think about building with AI

I've been tinkering with language models since 2019, so the magic trick wore off a while ago. The engineering part that's left is way more fun:

- **Put the rules in code (or Postgres), not in a prayer circle of prompts.** Exact math, state transitions, and access boundaries belong in deterministic code. Let the model handle the messy stuff it's actually good at (extraction, synthesis, bounded planning), and keep it far away from being your accountant.
- **Make the agents prove it.** Turning agents loose on a sloppy loop just produces slop faster. Most of my energy goes into the harness around the model: clear specs, small bounded changes, and verification steps where an agent has to show evidence instead of saying "looks good!" and gaslighting my git history.
- **Your agent needs real memory, not a junk drawer of embeddings.** Half the "personal AI" setups out there dump raw chunks into a vector store and hope for the best. Memory should have provenance, real identity resolution, honest coverage gaps, and database-enforced privacy. Eventually our agents should talk directly to each other without anyone handing over API keys.
- **If something annoys me twice, it's becoming a script or a cron job.** Execution is basically free now, so I'm unapologetic about building hyper-specific tools for an audience of one, plus whatever weird hardware side quest sounds fun that weekend.

### What I'm building

#### Agents & Memory

- **Throughline** *(private repo for now)* — My current obsession: a self-hosted personal data hub on PostgreSQL + pgvector that ingests messages, email, voice transcripts, calendar, health, Spotify, Plex, Reddit, YouTube, and more via HTTP plugins into one immutable, privacy-gated database built for AI agents to search and verify.
- **[directive](https://github.com/joey12725/directive)** — An AI engineering org running on a real project board (Plane). A PM agent breaks goals into stories and spends your Claude Code, Codex, Gemini CLI, and OpenCode budgets like a team.
- **[peerpass](https://github.com/joey12725/peerpass)** — Scoped, expiring, revocable passes so other people's agents can talk to yours over A2A, MCP, Slack, Discord, Telegram, or Matrix without ever holding your keys.
- **[inbox-recall](https://github.com/joey12725/inbox-recall)** — Hybrid semantic + keyword search over every chat you've ever had (WhatsApp, iMessage, Signal, Instagram, and more) served to your agents over MCP.
- **[splice](https://github.com/joey12725/splice)** — Describe a function in plain English, call it like normal Python. Generated once, contract-checked, cached, and locked in a sandbox.
- **[bookworm](https://github.com/joey12725/bookworm)** — Turns a folder of ebooks and PDFs into a cited, offline knowledge base and MCP server inside a single DuckDB file.
- **[focusgroup](https://github.com/joey12725/focusgroup)** — A focus group in your terminal. Spins up synthetic personas across four model families, split-tests your pitch, and hands back a verdict.
- **[cyrus-agent-framework](https://github.com/joey12725/cyrus-agent-framework)** — My early multi-agent state machine built back on the original LangChain release, and the spiritual ancestor of `directive`.

#### Products & Tools

- **[firesight-v2](https://github.com/joey12725/firesight-v2)** — Monte Carlo early-retirement planner rewritten from scratch in Rust → WebAssembly. Simulates 100,000 whole household lifetimes in ~6 seconds in your browser with real 2026 tax law, paired scenarios, and a Claude assistant that isn't allowed to make up numbers. ([Try it live](https://firesight-v2.vercel.app))
- **[in-the-know](https://github.com/joey12725/in-the-know)** — A weekly local-events newsletter written for one reader at a time. Reply "less rodeo stuff" and next week's issue actually listens. ([Live](https://itk-nine.vercel.app))
- **[3d-print-visualizer](https://github.com/joey12725/3d-print-visualizer)** — Preview sliced G-code in 3D on your phone, with print time and filament grams per color. ([Live](https://sleek-nirvana-3mxh.here.now/))
- **[arrdio](https://github.com/joey12725/arrdio)** — Self-hosted ebook, audiobook, and manga request manager for the `*arr` stack, written in Go.

#### Hardware, ML & Shenanigans

- **[rayneo-travel](https://github.com/joey12725/rayneo-travel)** — Flight tracking (delays, gates, boarding estimates, connection alerts) built for my RayNeo iO smart-glasses companion HUD (540×220 monochrome green screens over reverse-engineered Bluetooth).
- **[Arcade-Relay](https://github.com/joey12725/Arcade-Relay)** — Turns a physical arcade cabinet into a remote-controlled smart-home device over WebSockets, with config-as-code, controller remapping, and attract-mode screensavers.
- **[youtube-watch-predictor](https://github.com/joey12725/youtube-watch-predictor)** — Predicts which videos in my YouTube feed I'll actually click, scored properly with channel-held-out splits and bootstrap CIs.
- **[wakeword-lab](https://github.com/joey12725/wakeword-lab)** — Train a custom wake word from synthetic speech, score it against confusable phrases, and run it live on your mic.
- **[maskcast](https://github.com/joey12725/maskcast)** — An anime LED face mask driven by real-time facial emotion recognition and Whisper keywords.
- **[bubblelink](https://github.com/joey12725/bubblelink)** — Open-hardware wearable bubble guns with a custom analog PCB and a 90 Wh backpack. Yes, really.
- **[minipupper-operator](https://github.com/joey12725/minipupper-operator)** — ROS 2 SLAM and teleop tooling for a tiny quadruped robot dog.
- **[samoiloff-effect](https://github.com/joey12725/samoiloff-effect)** — Hides three completely different images in one print, revealed one at a time under red, green, or blue light.
- Also kicking around: **[makerspace-tools](https://github.com/joey12725/makerspace-tools)**, **[beeper-pg-sync](https://github.com/joey12725/beeper-pg-sync)**, **[fit-calculator](https://github.com/joey12725/fit-calculator)**, and **[st-repeating-field-group](https://pypi.org/project/st-repeating-field-group/)** (on PyPI).

### Been at this a while

- **2020:** Fine-tuned GPT-2 (124M up to 1.5B, started messing with it in 2019) on Colab to mimic friends' texting styles. Learned what overfitting actually means when 9.6% of the outputs came back verbatim.
- **2021:** Started [ReCap Budget](https://resume.joeyhersh.com/systems/recap-budget/) and ran self-hosted OPT-1.3B deployments back when running your own language model for a student startup was a slightly unhinged way to spend a weekend.
- **2022:** Kept scaling OPT-1.3B and GPT-3 at ReCap: curated 40,000 receipt items for a fine-tuned classifier, bullied LLMs into returning structured JSON before function calling existed, raised $46K cash + ~$60K in-kind, and shipped a [pre-ChatGPT document Q&A tool](https://github.com/joey12725/document-assistant) to help write our 60-page business plan.
- **2023:** Interned at USAA and somehow talked a regulated bank into letting an intern demo an offline Falcon-40B RAG assistant to hundreds of employees.
- **2024:** Joined USAA full-time on credit-risk pipelines, built [cyrus-agent-framework](https://github.com/joey12725/cyrus-agent-framework) (concurrent multi-agent state machines), and co-founded Fit & Flourish with an automated Meta Ads creative loop (human kill switch in Discord).
- **2025:** That Meta Ads loop hit 40,000 waitlist leads and drove cost per lead from $2.19 down to $0.29. Backfilled 19 years of credit-risk history at USAA and started living inside Claude Code, Codex, and my own scheduled agent loops full-time.
- **2026:** Founded [Guadalupe Automation](https://guadalupeautomation.com) to ship agent systems for real businesses, running 12 agent environments around the clock (1,002 scheduled runs in one 18-hour stretch), and building Throughline, FIRESight v2, and smart-glasses software on top.

---

**Stack:** TypeScript · Python · Rust · Go · SQL · Postgres + pgvector · Next.js · FastAPI · Docker · AWS · Claude Code · Codex · Gemini CLI · OpenCode · MCP · A2A

[resume.joeyhersh.com](https://resume.joeyhersh.com) · [Guadalupe Automation](https://guadalupeautomation.com) · me@joeyhersh.com
