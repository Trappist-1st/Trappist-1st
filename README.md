<!-- ┌─────────────────────────────────────────────────────────────────┐ -->
<!-- │  PROFILE INTERFACE v2.0 — HOLOGRAPHIC DISPLAY ACTIVE           │ -->
<!-- └─────────────────────────────────────────────────────────────────┘ -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:04040A,40:0E0029,75:0D0A2E,100:04040A&height=180&section=header&text=TRAPPIST-1ST&fontSize=52&fontColor=9DCDE4&animation=fadeIn&fontAlignY=42&desc=Systems%20Engineer%20·%20Backend%20Architect%20·%20AI%20Infrastructure&descAlignY=65&descSize=13&descColor=5A7A8A" alt="header" />

<br/>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=500&size=18&duration=3500&pause=1500&color=4FC3F7&center=true&vCenter=true&width=720&height=60&lines=Building+scalable+distributed+systems;Designing+AI+agent+infrastructure;Backend+engineering+at+depth;Systems+that+think+in+scale" alt="typing" />
</a>

<br/>

<img src="https://komarev.com/ghpvc/?username=Trappist-1st&label=SIGNAL+RECEIVED&color=1C2A4A&style=flat-square&labelColor=0A0A14" alt="profile views" />

</div>

<br/>

---

<!-- ════════════════════ SYSTEM IDENTITY ════════════════════ -->

```
┌─ SYSTEM IDENTITY ────────────────────────────────────────────────────┐
│  Focus      : Distributed Systems · Backend Engineering · AI Agents  │
│  Stack Core : Java · Python · TypeScript                             │
│  Current    : Building intelligent agent infrastructure              │
│  Pursuing   : Graduate research in LLMs and scalable systems         │
│  Contact    : trappist.1st@gmail.com                                 │
└──────────────────────────────────────────────────────────────────────┘
```

A systems engineer building robust distributed backends — while preparing the infrastructure for the next generation of intelligent systems. Interested in the intersection of large language models, autonomous agents, and the architecture required to run them at scale.

<br/>

---

<!-- ════════════════════ FEATURED SYSTEMS ════════════════════ -->

## Featured Systems

> *Selected projects — architecture, decisions, and outcomes.*

<br/>

<!-- ─── PROJECT 1: Distributed Lite Scheduler ─── -->
<table>
<tr>
<td width="58%">

### [Distributed Lite Scheduler](https://github.com/Trappist-1st/Distributed-Lite-Scheduler)

A production-grade lightweight distributed task scheduling platform for small-to-medium teams. Benchmarked against XXL-Job, Kubernetes Job Scheduler, and Apache Airflow — designed to be leaner and easier to operate than all three.

**Architecture highlights:**
- Multi-instance Scheduler layer with Redis-based distributed lock for automatic leader election — zero single-point-of-failure
- DAG workflow engine for complex task dependency resolution
- Resource-aware scheduling: CPU/GPU/memory quotas enforced at dispatch time, preventing task starvation under load
- Multi-tenant resource isolation with per-tenant quota management
- Pluggable executor model: Shell / Python / Docker / HTTP

**Engineering decisions:**
- Optimistic locking + idempotency keys on all state transitions ensure exactly-once execution semantics
- Async processing pipeline with Redis task queue decouples scheduling decisions from executor availability
- Spring Cloud Gateway as API surface — rate limiting, circuit breaking, and distributed tracing from the start

</td>
<td width="42%" align="center">

![Java](https://img.shields.io/badge/Java-0A0A14?style=flat-square&logo=openjdk&logoColor=4FC3F7)
![Spring](https://img.shields.io/badge/Spring_Boot_4-0A0A14?style=flat-square&logo=springboot&logoColor=9DCDE4)
![Redis](https://img.shields.io/badge/Redis-0A0A14?style=flat-square&logo=redis&logoColor=4FC3F7)
![MySQL](https://img.shields.io/badge/MySQL-0A0A14?style=flat-square&logo=mysql&logoColor=9DCDE4)
![Docker](https://img.shields.io/badge/Docker-0A0A14?style=flat-square&logo=docker&logoColor=4FC3F7)

```
High Availability  ████████████████  HA
Resource-Aware     ████████████████  ✓
DAG Support        ██████████████░░  ✓
Multi-tenant       ████████████████  ✓
```

[![Repo](https://img.shields.io/badge/→_View_Repository-1C2A4A?style=flat-square)](https://github.com/Trappist-1st/Distributed-Lite-Scheduler)

</td>
</tr>
</table>

<br/>

<!-- ─── PROJECT 2: AstroGuide ─── -->
<table>
<tr>
<td width="58%">

### [AstroGuide — Intelligent Astronomy Platform](https://github.com/Trappist-1st/AstroGuide----An-Intelligent-Astronomy-Knowledge-Platform-backend-)

An AI-powered astronomy knowledge platform backend. Combines RAG, tool-calling, and real-time streaming to deliver expert-level responses on undergraduate astronomy content.

**Architecture highlights:**
- RAG pipeline: knowledge vectorized and stored in Qdrant; retrieved at query time and injected into prompt context
- SSE (Server-Sent Events) streaming endpoint for real-time AI response delivery with sub-second first-token latency
- Tool-calling layer integrates Wikipedia search, vector knowledge base queries, and concept card lookups — model selects tools autonomously or via explicit user directives (`@wiki:`, `@kb:`, `@card:`)
- Configurable advisor chain: Memory + RAG + Wikipedia advisors compose in runtime, each independently toggleable

**Engineering decisions:**
- OpenAI-compatible API abstraction layer allows hot-swapping between DeepSeek, SiliconFlow, and other providers without code changes
- Per-tool disable flag on explicit invocations prevents duplicate calls when the user prefetches a tool result manually
- Session-scoped conversation history enables coherent multi-turn dialogue without client-side state management

</td>
<td width="42%" align="center">

![Java](https://img.shields.io/badge/Java-0A0A14?style=flat-square&logo=openjdk&logoColor=4FC3F7)
![Spring](https://img.shields.io/badge/Spring_AI_1.1-0A0A14?style=flat-square&logo=springboot&logoColor=9DCDE4)
![MySQL](https://img.shields.io/badge/MySQL-0A0A14?style=flat-square&logo=mysql&logoColor=4FC3F7)
![Qdrant](https://img.shields.io/badge/Qdrant-0A0A14?style=flat-square&logoColor=9DCDE4)
![Docker](https://img.shields.io/badge/Docker-0A0A14?style=flat-square&logo=docker&logoColor=4FC3F7)

```
RAG Pipeline       ████████████████  ✓
SSE Streaming      ████████████████  ✓
Tool Calling       ██████████████░░  ✓
Session Memory     ████████████████  ✓
```

[![Repo](https://img.shields.io/badge/→_View_Repository-1C2A4A?style=flat-square)](https://github.com/Trappist-1st/AstroGuide----An-Intelligent-Astronomy-Knowledge-Platform-backend-)

</td>
</tr>
</table>

<br/>

<!-- ─── PROJECT 3: Deep Research Agent ─── -->
<table>
<tr>
<td width="58%">

### [Deep Research Agent](https://github.com/Trappist-1st/Deep-Research-Agent)

An autonomous AI agent that conducts deep multi-source research and generates structured reports. Given a query, it plans, crawls, analyses, and writes — without human intervention at any step.

**Architecture highlights:**
- Four-stage pipeline: `planner.py` → `crawler.py` → `analyzer.py` → `report.py` — each stage is independently testable and replaceable
- Parallelized web crawling with Selenium headless Chrome; automatic quality filtering rejects low-signal pages before analysis
- Multi-modal analysis: text via o3-mini for summarization; screenshot capture + vision model for tables and figures that can't be parsed as text
- Outline-first report generation: LLM builds a hierarchical section structure with weighted priorities before writing any prose

**Engineering decisions:**
- Separating planning from execution (distinct `planner.py` / `research_agent.py`) keeps the agent loop auditable — every search decision is traceable back to an explicit plan step
- Source citation embedded throughout generation, not appended at the end — ensures claims remain grounded even during iterative rewrites

</td>
<td width="42%" align="center">

![Python](https://img.shields.io/badge/Python-0A0A14?style=flat-square&logo=python&logoColor=4FC3F7)
![OpenAI](https://img.shields.io/badge/OpenAI_o3-0A0A14?style=flat-square&logo=openai&logoColor=9DCDE4)
![Selenium](https://img.shields.io/badge/Selenium-0A0A14?style=flat-square&logo=selenium&logoColor=4FC3F7)
![Google](https://img.shields.io/badge/Google_Search_API-0A0A14?style=flat-square&logo=google&logoColor=9DCDE4)

```
Autonomy           ████████████████  Full
Multi-modal        ██████████████░░  ✓
Source-grounded    ████████████████  ✓
Parallelised       ████████████████  ✓
```

[![Repo](https://img.shields.io/badge/→_View_Repository-1C2A4A?style=flat-square)](https://github.com/Trappist-1st/Deep-Research-Agent)

</td>
</tr>
</table>

<br/>

<!-- ─── PROJECT 4: Multimodal AI Assistant ─── -->
<table>
<tr>
<td width="58%">

### [Multimodal AI Assistant](https://github.com/Trappist-1st/Multimodal-AI-Assistant)

A real-time voice conversation system with speech-to-text, LLM inference, and text-to-speech in a single low-latency pipeline. Supports multiple languages with minimal perceptible delay.

**Architecture highlights:**
- WebSocket-based full-duplex audio stream between browser and Node.js backend — no HTTP polling, no round-trip overhead
- `audioWorklet.js` runs in the browser's audio thread for Voice Activity Detection (VAD), sending only speech segments — reduces upstream bandwidth and LLM prompt noise
- LLaMA inference integrated server-side; response text piped directly into TTS synthesis before the full reply is complete (streaming TTS)

**Engineering decisions:**
- Decoupling VAD into the AudioWorklet (off main thread) prevents UI jank during continuous recording
- Next.js frontend with Tailwind CSS keeps the interface latency-free; no heavy state management framework needed for a single-session voice app
- Real-time latency monitoring logged per-session — latency data used to tune VAD silence threshold and chunk sizes

</td>
<td width="42%" align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-0A0A14?style=flat-square&logo=typescript&logoColor=4FC3F7)
![Node.js](https://img.shields.io/badge/Node.js-0A0A14?style=flat-square&logo=nodedotjs&logoColor=9DCDE4)
![Next.js](https://img.shields.io/badge/Next.js-0A0A14?style=flat-square&logo=nextdotjs&logoColor=4FC3F7)
![Tailwind](https://img.shields.io/badge/Tailwind-0A0A14?style=flat-square&logo=tailwindcss&logoColor=9DCDE4)

```
Latency            ██████████████░░  Low
Streaming TTS      ████████████████  ✓
VAD (off-thread)   ████████████████  ✓
Multilingual       ████████████████  ✓
```

[![Repo](https://img.shields.io/badge/→_View_Repository-1C2A4A?style=flat-square)](https://github.com/Trappist-1st/Multimodal-AI-Assistant)

</td>
</tr>
</table>

<br/>

<!-- ─── Additional Projects ─── -->

<details>
<summary><b>More Projects</b></summary>

<br/>

**[Message Broker](https://github.com/Trappist-1st/message-broker)** — A self-built publish/subscribe message middleware from scratch in Java using raw sockets. No frameworks — pure protocol design, Broker server, and a client SDK. Includes throughput/latency/fanout benchmarks. A systems-fundamentals exercise in network programming and concurrent state management.

`Java` `Raw Sockets` `Pub/Sub` `Maven`

<br/>

**[Halo CE TCG — Game Engine](https://github.com/Trappist-1st/Halo-Combat-Evolved-TCG)** — A TCP-networked trading card game engine built in Java. Implements a full event bus + listener pipeline, damage resolution with a modifier stack, DAG-like phase state machine (`DRAW → DEPLOY → SKIRMISH → ENDSTEP`), multi-room server with JSON-over-TCP command protocol, and a client SDK. A game rules engine is a strict distributed state synchronisation problem in disguise.

`Java` `TCP Networking` `Event Bus` `State Machine` `Maven`

</details>

<br/>

---

<!-- ════════════════════ TECHNICAL INFRASTRUCTURE ════════════════════ -->

## Technical Infrastructure

<details>
<summary><b>Languages</b></summary>
<br/>

<p align="center">
  <a href="https://www.python.org"><img src="https://skillicons.dev/icons?i=py" width="36" height="36" alt="Python"/></a>&nbsp;
  <a href="https://www.java.com"><img src="https://skillicons.dev/icons?i=java" width="36" height="36" alt="Java"/></a>&nbsp;
  <a href="https://www.typescriptlang.org/"><img src="https://skillicons.dev/icons?i=ts" width="36" height="36" alt="TypeScript"/></a>&nbsp;
  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"><img src="https://skillicons.dev/icons?i=js" width="36" height="36" alt="JavaScript"/></a>&nbsp;
  <a href="https://www.cplusplus.com"><img src="https://skillicons.dev/icons?i=cpp" width="36" height="36" alt="C++"/></a>
</p>

</details>

<details>
<summary><b>Backend & Infrastructure</b></summary>
<br/>

<p align="center">
  <a href="https://fastapi.tiangolo.com/"><img src="https://skillicons.dev/icons?i=fastapi" width="36" height="36" alt="FastAPI"/></a>&nbsp;
  <a href="https://spring.io/"><img src="https://skillicons.dev/icons?i=spring" width="36" height="36" alt="Spring Boot"/></a>&nbsp;
  <a href="https://www.docker.com/"><img src="https://skillicons.dev/icons?i=docker" width="36" height="36" alt="Docker"/></a>&nbsp;
  <a href="https://kubernetes.io"><img src="https://skillicons.dev/icons?i=kubernetes" width="36" height="36" alt="Kubernetes"/></a>&nbsp;
  <a href="https://aws.amazon.com"><img src="https://skillicons.dev/icons?i=aws" width="36" height="36" alt="AWS"/></a>&nbsp;
  <a href="https://www.nginx.com"><img src="https://skillicons.dev/icons?i=nginx" width="36" height="36" alt="Nginx"/></a>&nbsp;
  <a href="https://kafka.apache.org/"><img src="https://skillicons.dev/icons?i=kafka" width="36" height="36" alt="Kafka"/></a>&nbsp;
  <a href="https://www.rabbitmq.com"><img src="https://skillicons.dev/icons?i=rabbitmq" width="36" height="36" alt="RabbitMQ"/></a>&nbsp;
  <a href="https://www.jenkins.io"><img src="https://skillicons.dev/icons?i=jenkins" width="36" height="36" alt="Jenkins"/></a>&nbsp;
  <a href="https://grafana.com"><img src="https://skillicons.dev/icons?i=grafana" width="36" height="36" alt="Grafana"/></a>
</p>

</details>

<details>
<summary><b>AI / Machine Learning</b></summary>
<br/>

<p align="center">
  <a href="https://pytorch.org/"><img src="https://skillicons.dev/icons?i=pytorch" width="36" height="36" alt="PyTorch"/></a>&nbsp;
  <a href="https://www.tensorflow.org"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tensorflow/tensorflow-original.svg" width="36" height="36" alt="TensorFlow"/></a>&nbsp;
  <a href="https://scikit-learn.org/"><img src="https://skillicons.dev/icons?i=scikitlearn" width="36" height="36" alt="scikit-learn"/></a>&nbsp;
  <a href="https://opencv.org/"><img src="https://skillicons.dev/icons?i=opencv" width="36" height="36" alt="OpenCV"/></a>&nbsp;
  <a href="https://www.langchain.com/"><img src="https://cdn.simpleicons.org/langchain/4FC3F7" width="36" height="36" alt="LangChain"/></a>&nbsp;
  <a href="https://huggingface.co/"><img src="https://cdn.simpleicons.org/huggingface" width="36" height="36" alt="HuggingFace"/></a>&nbsp;
  <a href="https://numpy.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" width="36" height="36" alt="NumPy"/></a>
</p>

</details>

<details>
<summary><b>Data Layer</b></summary>
<br/>

<p align="center">
  <a href="https://www.postgresql.org"><img src="https://skillicons.dev/icons?i=postgres" width="36" height="36" alt="PostgreSQL"/></a>&nbsp;
  <a href="https://www.mysql.com/"><img src="https://skillicons.dev/icons?i=mysql" width="36" height="36" alt="MySQL"/></a>&nbsp;
  <a href="https://www.mongodb.com/"><img src="https://skillicons.dev/icons?i=mongodb" width="36" height="36" alt="MongoDB"/></a>&nbsp;
  <a href="https://redis.io"><img src="https://skillicons.dev/icons?i=redis" width="36" height="36" alt="Redis"/></a>&nbsp;
  <a href="https://www.elastic.co"><img src="https://skillicons.dev/icons?i=elasticsearch" width="36" height="36" alt="Elasticsearch"/></a>&nbsp;
  <a href="https://www.sqlite.org/"><img src="https://skillicons.dev/icons?i=sqlite" width="36" height="36" alt="SQLite"/></a>
</p>

</details>

<details>
<summary><b>Frontend & Tooling</b></summary>
<br/>

<p align="center">
  <a href="https://vuejs.org/"><img src="https://skillicons.dev/icons?i=vue" width="36" height="36" alt="Vue.js"/></a>&nbsp;
  <a href="https://tailwindcss.com/"><img src="https://skillicons.dev/icons?i=tailwind" width="36" height="36" alt="Tailwind"/></a>&nbsp;
  <a href="https://git-scm.com/"><img src="https://skillicons.dev/icons?i=git" width="36" height="36" alt="Git"/></a>&nbsp;
  <a href="https://www.linux.org/"><img src="https://skillicons.dev/icons?i=linux" width="36" height="36" alt="Linux"/></a>&nbsp;
  <a href="https://postman.com"><img src="https://skillicons.dev/icons?i=postman" width="36" height="36" alt="Postman"/></a>&nbsp;
  <a href="https://jupyter.org/"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original-wordmark.svg" width="36" height="36" alt="Jupyter"/></a>
</p>

</details>

<br/>

---

<!-- ════════════════════ COMMAND TELEMETRY ════════════════════ -->

## Command Telemetry

<div align="center">
  <img height="170em" src="https://github-readme-stats.vercel.app/api?username=Trappist-1st&show_icons=true&theme=radical&include_all_commits=true&count_private=true&hide_border=true&card_width=320&title_color=4FC3F7&icon_color=9DCDE4&text_color=A0B4C0&bg_color=04040A" alt="GitHub Stats"/>
  <img height="170em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Trappist-1st&layout=compact&langs_count=8&theme=radical&hide_border=true&card_width=320&title_color=4FC3F7&text_color=A0B4C0&bg_color=04040A" alt="Top Languages"/>
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Trappist-1st&theme=radical&hide_border=true&background=04040A&ring=4FC3F7&fire=9DCDE4&currStreakLabel=4FC3F7&sideLabels=A0B4C0&dates=5A7A8A" alt="Streak Stats"/>
</div>

<br/>

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Trappist-1st&theme=react-dark&hide_border=true&area=true&bg_color=04040A&color=9DCDE4&line=4FC3F7&point=9DCDE4" alt="Contribution Graph"/>
</div>

<br/>

---

<!-- ════════════════════ TRANSMISSION ════════════════════ -->

## Transmission

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-Trappist--1st-0A0A14?style=flat-square&logo=github&logoColor=9DCDE4&labelColor=1C2A4A)](https://github.com/Trappist-1st)
&nbsp;
[![Email](https://img.shields.io/badge/Email-trappist.1st%40gmail.com-0A0A14?style=flat-square&logo=gmail&logoColor=9DCDE4&labelColor=1C2A4A)](mailto:trappist.1st@gmail.com)

</div>

<br/>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:04040A,50:0E0029,100:04040A&height=110&section=footer&text=Systems+built+to+last.&fontSize=16&fontColor=5A7A8A&fontAlignY=65" alt="footer" />

</div>
