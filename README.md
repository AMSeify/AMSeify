<div align="center">

<img alt="Amir Seify — Python Developer to MLOps" src="https://capsule-render.vercel.app/api?type=waving&color=0:6366F1,50:8B5CF6,100:14B8A6&height=190&section=header&text=Amir%20Seify&fontSize=54&fontColor=ffffff&fontAlignY=36&desc=Python%20Developer%20%E2%86%92%20MLOps%20%C2%B7%20AI%20Agent%20Engineer&descSize=18&descAlignY=58&animation=fadeIn" />

<p>
  <a href="https://AMSeify.me"><img alt="Website" src="https://img.shields.io/badge/AMSeify.me-6366F1?style=for-the-badge&logo=hugo&logoColor=white" /></a>
  <a href="https://twitter.com/AMSeify"><img alt="X" src="https://img.shields.io/badge/@AMSeify-000000?style=for-the-badge&logo=x&logoColor=white" /></a>
  <a href="mailto:amh.seify@gmail.com"><img alt="Email" src="https://img.shields.io/badge/amh.seify@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <img alt="Location" src="https://img.shields.io/badge/Tehran-14B8A6?style=for-the-badge&logo=googlemaps&logoColor=white" />
</p>

<sub>🐍 Python · 🐧 Arch & Manjaro · 🤖 LLM agents · 🏦 Financial data · 🚢 Docker all the way down</sub>

</div>

---

## 👋 whoami

```python
class AmirSeify:
    role      = "Python Developer → MLOps"
    based_in  = "Tehran, Iran"
    building  = "theRadioCode.com"
    daily     = ["LLM agents", "financial data pipelines", "things in containers"]
    daily_os  = ["Manjaro 🟢", "Arch 💙"]
    obsession = "doing more with fewer tokens"
    motto     = "Let's Rock'n'Roll 🤘"
```

I started as a Python developer and drifted into **MLOps** — and never came back. These days
my work sits in the overlap between two worlds: **messy financial data** on one side, and
**LLM agent systems** on the other. I pull market data into shape, build agent graphs on top
of it, and ship the whole thing behind Docker, Nginx and Postgres.

A recurring theme in everything I build: **token efficiency**. Context windows are a budget,
not a bucket — so I keep writing tools that say the same thing in fewer tokens.

---

## 🧠 The stack I live in

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#EEF2FF','primaryTextColor':'#1E1B4B','primaryBorderColor':'#6366F1','lineColor':'#8B5CF6','fontSize':'15px'}}}%%
mindmap
  root((Amir))
    AI and LLM
      LangGraph agent systems
      MCP servers and tools
      RAG and document research
      OpenRouter multi-model
      Prompt and token engineering
    Backend
      Python and FastAPI
      PostgreSQL and Alembic
      Async workers and queues
      REST and web services
    Data
      Financial and market data
      Pandas and time series
      ETL and scrapers
      Dashboards and reporting
    Platform
      Docker and Compose
      Nginx gateways
      Linux — Arch and Manjaro
      CI/CD and observability
    Frontend
      TypeScript and React
      shadcn/ui and Tailwind
      Admin panels
```

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Linux](https://img.shields.io/badge/Arch_Linux-1793D1?style=flat-square&logo=archlinux&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-D97757?style=flat-square&logo=anthropic&logoColor=white)

</div>

---

## 🏗️ How I usually build

Most of my systems end up looking like this — ingest the mess, normalize it, put an agent
layer on top, and serve it through one door.

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#EEF2FF','primaryTextColor':'#1E1B4B','primaryBorderColor':'#6366F1','lineColor':'#8B5CF6','fontSize':'14px','clusterBkg':'#F8FAFC','clusterBorder':'#CBD5E1'}}}%%
flowchart LR
    subgraph INGEST["📥 Ingest"]
        A1[Market & filing sources]
        A2[Docs, PDFs, audio, web]
        A3[Scrapers & fetchers]
    end

    subgraph CORE["⚙️ Core"]
        B1[(PostgreSQL<br/>+ Alembic)]
        B2[DAL / service layer]
        B3[Async workers]
    end

    subgraph BRAIN["🤖 Agent layer"]
        C1[LLM core client<br/>multi-provider]
        C2[LangGraph graphs<br/>tools & memory]
        C3[MCP tools]
    end

    subgraph SERVE["🚀 Serve"]
        D1[FastAPI]
        D2[Nginx gateway<br/>single port]
        D3[Dashboards &<br/>admin panels]
    end

    A1 --> A3
    A2 --> A3
    A3 --> B1
    B1 --> B2
    B2 --> B3
    B2 --> C2
    C1 --> C2
    C3 --> C2
    C2 --> D1
    B2 --> D1
    D1 --> D2
    D2 --> D3

    classDef ingest fill:#DBEAFE,stroke:#2563EB,color:#0C1E3E
    classDef core fill:#E0E7FF,stroke:#4F46E5,color:#1E1B4B
    classDef brain fill:#F3E8FF,stroke:#9333EA,color:#3B0764
    classDef serve fill:#CCFBF1,stroke:#0D9488,color:#042F2E

    class A1,A2,A3 ingest
    class B1,B2,B3 core
    class C1,C2,C3 brain
    class D1,D2,D3 serve
```

---

## 🗺️ The road so far

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#EEF2FF','primaryTextColor':'#3730A3','primaryBorderColor':'#6366F1','lineColor':'#8B5CF6','fontSize':'14px'}}}%%
timeline
    2018 : Landed on GitHub
         : Python, Linux, and a lot of curiosity
    2024 : Financial data engineering
         : Data access layers and market data fetchers
         : Postgres schemas that survive real data
    2025 : Into LLM territory
         : An in-house LLM core client, multi-provider
         : LangGraph servers for financial reasoning
         : Document research and extraction agents
         : Voice — AI call center and VoIP experiments
    2026 : Agent infrastructure and open source
         : MCP tooling built for token budgets
         : Token-oriented data formats for pandas
         : Deployment templates so shipping is boring
```

---

## 💼 What I actually work on

<table>
<tr><td width="34%"><b>🏦 Financial data platforms</b></td>
<td>Data access layers, market-data fetchers, disclosure/filing web services, business-segment extraction, time-series tooling and the dashboards that sit on top.</td></tr>

<tr><td><b>🤖 LLM & agent systems</b></td>
<td>A reusable multi-provider LLM core client, LangGraph-based reasoning servers, document research agents, chat products, and AI call-center / VoIP experiments.</td></tr>

<tr><td><b>🧰 Token-efficient AI tooling</b></td>
<td>Open-source libraries and MCP servers built around one question: how do we hand an agent the same information for a fraction of the context?</td></tr>

<tr><td><b>🚢 Platform & delivery</b></td>
<td>Docker Compose stacks, Nginx single-port gateways, Alembic migrations, background workers, backup/restore tooling and centralized logging.</td></tr>

<tr><td><b>🎛️ Full-stack when it's needed</b></td>
<td>TypeScript + React admin panels, shadcn/ui component kits and financial dashboards — because a backend nobody can see doesn't ship.</td></tr>
</table>

---

## 🌟 Featured open source

<table>
<tr>
<td width="50%" valign="top">

### 🌐 [lean-browser](https://github.com/AMSeify/lean-browser)
`Python` · `Playwright` · `MCP`

Token-efficient browser MCP for AI agents. Chromium via
Playwright, terse tools, and **diffs instead of full page
snapshots** — targeting ~30k tokens for a 10-step task where
a standard browser MCP burns ~114k.

</td>
<td width="50%" valign="top">

### 🐼 [pandas-toon](https://github.com/AMSeify/pandas-toon)
`Python` · `pandas` · `LLM`

TOON — Token-Oriented Object Notation — support for pandas.
`pd.read_toon()` and `df.to_toon()`, with type inference, for
when JSON and CSV are too expensive to put in a prompt.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🎩 [fundas](https://github.com/AMSeify/fundas)
`Python` · `pandas` · `OpenRouter`

**Fun**damental **Da**ta **S**ource — pandas that reads the
unstructured world. Point it at PDFs, images, audio, video or
webpages, describe what you want in plain language, get a
DataFrame back.

</td>
<td width="50%" valign="top">

### 📦 [deploy_template](https://github.com/AMSeify/deploy_template)
`Docker` · `Nginx` · `PostgreSQL`

Production-style starter: frontend + backend + worker +
Postgres, one Nginx gateway on a single port, Alembic
migrations and a Makefile for lifecycle and backup/restore.

</td>
</tr>
</table>

---

## 📊 Where the time goes

```mermaid
%%{init: {'theme':'base','themeVariables':{'pie1':'#8B5CF6','pie2':'#6366F1','pie3':'#0EA5E9','pie4':'#14B8A6','pie5':'#F59E0B','pieSectionTextSize':'15px','pieStrokeColor':'#64748B','pieOuterStrokeColor':'#64748B','pieSectionTextColor':'#ffffff','pieLegendTextColor':'#64748B'}}}%%
pie showData
    "LLM & agent systems" : 35
    "Data engineering" : 25
    "Backend & APIs" : 20
    "DevOps & delivery" : 12
    "Frontend" : 8
```

---

## 📈 GitHub

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=AMSeify&show_icons=true&hide_border=true&theme=tokyonight&icon_color=8B5CF6&title_color=8B5CF6&include_all_commits=true" />
  <img alt="Amir's GitHub stats" src="https://github-readme-stats.vercel.app/api?username=AMSeify&show_icons=true&hide_border=true&theme=default&icon_color=6366F1&title_color=6366F1&include_all_commits=true" height="165" />
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=AMSeify&layout=compact&hide_border=true&theme=tokyonight&title_color=8B5CF6&langs_count=8" />
  <img alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=AMSeify&layout=compact&hide_border=true&theme=default&title_color=6366F1&langs_count=8" height="165" />
</picture>

</div>

---

## 🤝 Let's talk

I'm always up for a conversation about **agent architectures**, **squeezing context windows**,
**financial data that refuses to be clean**, or **which Linux distro you should actually be running**.

<div align="center">

<a href="https://AMSeify.me"><img alt="Website" src="https://img.shields.io/badge/Blog-AMSeify.me-6366F1?style=for-the-badge&logo=googlechrome&logoColor=white" /></a>
<a href="https://twitter.com/AMSeify"><img alt="X" src="https://img.shields.io/badge/X-@AMSeify-000000?style=for-the-badge&logo=x&logoColor=white" /></a>
<a href="mailto:amh.seify@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-amh.seify@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>

<br/><br/>

<i>“Let's Rock'n'Roll” 🤘</i>

<img alt="" src="https://capsule-render.vercel.app/api?type=waving&color=0:14B8A6,50:8B5CF6,100:6366F1&height=120&section=footer" />

</div>
