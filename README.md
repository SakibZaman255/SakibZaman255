<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:000000,45:1A0A00,75:8C3A08,100:D97757&height=260&section=header&text=Rafiqul%20Hasan%20Sakib&fontSize=58&fontColor=FFFFFF&animation=fadeIn&fontAlignY=40&desc=Full-Stack%20Software%20Engineer%20%C2%B7%20SaaS%20Architect%20%C2%B7%20Production%20Engineer&descAlignY=60&descSize=17&descColor=FFD4A8" width="100%" />

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://rafiqulhasansakib.vercel.app/)
[![Email](https://img.shields.io/badge/Email-D97757?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sakibzaman255@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sakibzaman255/)
[![CV](https://img.shields.io/badge/Download_CV-181717?style=for-the-badge&logo=readdotcv&logoColor=white)](https://rafiqulhasansakib.vercel.app/cv/Rafiqul_Hasan_Sakib_Cv.pdf)

**Dhaka, Bangladesh · GMT+6 · Replies within 2 hours · Open to freelance and full-time**

</div>

---

## The numbers

I'd rather show evidence than claim skills. Everything below is running in production.

<div align="center">

| | |
|---:|:---|
| **188,000+** | answer sheets processed by SmartOMR |
| **80+** | paying institutions on recurring plans |
| **12** | applications deployed and in use |
| **99.9%** | uptime on a VPS I manage myself |
| **400+** | employees tracked across 4 offices |
| **1,639** | exam questions authored, bilingual |
| **3+ yrs** | in software · **5+ yrs** running two retail businesses before it |

</div>

---

## About

I build **multi-tenant SaaS that runs in production and stays there.** Two of the platforms I lead — an OMR grading engine and a biometric HR system — serve 80+ institutions and 400+ tracked employees between them. The rest I built solo, from a blank Prisma schema up to the interface people operate.

**I learned business before I learned software.** Five years co-founding and running two retail companies came first — procurement, pricing, suppliers, staff, and the very specific education you get from a deadline that costs money. It's why I read a brief for the business problem first and the ticket second, and why I'd rather ask an awkward question in week one than find the answer in production.

I don't just ship features. I own the Ubuntu boxes, read the logs, and fix what breaks.

> *I turn what the world already prints — an answer sheet, a fingerprint punch, a textbook chapter — into systems people trust with real work.*

---

## Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=typescript,javascript,nextjs,react,nodejs,express,tailwind,prisma,jest&theme=dark" />
<br/>
<img src="https://skillicons.dev/icons?i=mysql,postgres,mongodb,sqlite,redis,electron,docker,nginx,linux&theme=dark" />
<br/>
<img src="https://skillicons.dev/icons?i=git,github,vercel,bash,postman,figma,html,css,vscode&theme=dark" />

</div>

> Listed because I've shipped production code with it — not because I read the docs once.

<div align="center">

| | |
|:---|:---|
| **Languages** | TypeScript · JavaScript (ES6+) · SQL · HTML5 · CSS3 |
| **Frontend** | Next.js 16 (App Router) · React 19 · Tailwind CSS · shadcn/ui · Zustand · GSAP · Framer Motion · Fabric.js · Canvas API · Chart.js · Recharts · TanStack Table · TipTap · MDX · i18n |
| **Backend & APIs** | Node.js · Express · Route Handlers · REST design · NextAuth v5 · JWT & sessions · Middleware · Sharp · node-cron · Jest |
| **Database & ORM** | PostgreSQL · MySQL · MongoDB · SQLite · Redis · Prisma ORM · Schema design · Query optimisation · Indexing |
| **Desktop & Hardware** | Electron · electron-builder · TWAIN scanners · node-zklib · ZKTeco ADMS · Service Workers · Offline-first PWAs |
| **DevOps** | Ubuntu VPS · Nginx · PM2 · Docker · Vercel · CI/CD · SSL · Git & PR flow · Bash · Postman · Figma |
| **Architecture** | Multi-tenancy · RBAC & guards · Tenant isolation · Audit logging · Rate limiting · Batch pipelines · Image processing · Offline-first |

</div>

---

## Flagship work

### SmartOMR — commercial OMR processing SaaS
`smartomr.cloud` · **80+ institutions · 188,000+ sheets · 95% grading time removed · 99.9% uptime**

Institutions still grade multiple-choice exams by hand, one sheet at a time. SmartOMR takes the scanned stack instead: it detects every filled bubble with an image pipeline, grades against a configurable key, and returns per-student PDFs before the invigilator has left the hall.

> **The hard part was never the reading** — it was making one codebase serve eighty institutions that each design their own sheet, run their own sets, and must never see each other's data.

- Visual OMR designer on a Fabric.js canvas — schools lay out their own bubble grids, corner anchors and answer regions, at A4 or A5
- Image pipeline over Canvas API and Sharp, resolving marks under skew, smudge and inconsistent scan exposure
- Batch engine grading 500+ sheets per run with automatic set detection across Sets A–E
- Multi-tenant MySQL with per-organisation isolation, RBAC, credit balances and a full audit trail

**Hardest problems:** anchor detection on torn, folded and faintly photocopied sheets · mapping a scan back to the right student *and* question set every time · two operators uploading into one batch without corrupting either run.

<sub>`Next.js 16` `TypeScript` `MySQL` `Prisma` `Fabric.js` `Sharp` `NextAuth` · Ubuntu VPS · Nginx · PM2</sub>

<br/>

### HajiraPro — HR, attendance & payroll platform
`hajirapro.com` · **400+ employees · 4 offices · real-time sync**

Attendance data lives inside biometric hardware, not the browser. HajiraPro runs **its own ADMS server** that ZKTeco fingerprint terminals push to directly, so punches from four offices land in the payroll engine the moment a finger touches the sensor.

> **Payroll is where a rounding error becomes someone's rent.** Every rule — overtime bands, weekend and holiday handling, late grace, leave accrual — is modelled explicitly and covered by tests, because "roughly right" is not a payroll outcome.

- A dedicated ADMS server process — a terse device push protocol, not a REST API, so the parser and handshake are hand-built
- Duplicate and out-of-order punch reconciliation across offices with flaky connectivity
- Tenant isolation audited route by route, not assumed
- Nightly `node-cron` jobs reconciling absences against weekends and holidays

<sub>`Next.js 16` `TypeScript` `PostgreSQL` `Prisma` `NextAuth v5` `node-zklib` `node-cron` `Jest`</sub>

<br/>

### ICT Shikhi — bilingual HSC ICT learning platform
`hscict.vercel.app` · **145 syllabus sections · 1,639 questions · 45 interactive labs**

The entire NCTB HSC ICT syllabus rewritten as structured bilingual content, then given something to look at. Every idea that's hard to picture gets a worked example, a textbook figure, or an animation that shows the mechanism instead of asserting it.

> **Understand ICT, don't just memorise it.** That tagline is the architecture: content is typed data, not markup, so one `Topic` object feeds the lesson page, the search index, the quiz pool, the board exam paper, the revision sheet and progress tracking at once.

- Every content string is a `{ en, bn }` value resolved by the `/[locale]/` route segment — a topic can't exist in one language only
- 1,639 questions from a **single pool**, so six practice surfaces can never drift out of sync
- A board exam simulator with a real MCQ paper, an OMR sheet and a clock
- `npm run validate` self-checks the content — a topic pointing at a missing lab fails before the build does

<sub>`Next.js 16` `React 19` `TypeScript` `Tailwind CSS` `i18n` `Canvas API`</sub>

<br/>

### PROGRESS MIS — enterprise MIS for Swisscontact
*Internal deployment* · **9 roles · 20 × 12 permission matrix · 6-stage approval chain**

A management information system for Swisscontact's PROGRESS programme — green growth in Bangladesh's ready-made garments sector. It tracks factory interventions, training, partner contracts and ESG metrics through a four-stage approval chain.

> **Development-sector reporting is a permissions problem wearing a data-entry costume.** A local consultancy submits; the lead consultancy reviews; the programme team approves; the monitoring team validates. Every actor sees a different slice of the same record.

- Nine roles over a `{resource}.{action}` matrix, wildcard-aware, enforced through one API guard
- A dynamic form builder with calculated fields, a formula language, and Excel import that infers the schema from a spreadsheet
- Field-level review comments, so a reviewer can query one cell rather than reject a whole submission

<sub>`Next.js 16` `TypeScript` `MySQL` `Prisma` `NextAuth` `shadcn/ui` `TanStack Table`</sub>

<br/>

### SmartOMR Desktop — offline Electron build
*v4.5 · built solo · no connection required*

The whole grading pipeline packaged as an Electron application that talks to a **TWAIN scanner directly** and stores everything in local SQLite — for institutions that own a scanner and have no reliable internet.

> Not a thin wrapper: the desktop build swaps MySQL for SQLite behind a second Prisma client, drives the scanner over a native TWAIN binding, and ships `sharp` and `canvas` as rebuilt native modules inside the installer.

**Hardest problems:** `sharp` and `canvas` won't load from inside an ASAR archive without explicit unpacking and a rebuild against Electron's own headers · running Next.js as a desktop process with no server to call · driving a decades-old TWAIN C API from JavaScript.

<sub>`Electron` `Next.js` `TypeScript` `SQLite` `Prisma` `TWAIN` `Sharp` `electron-builder`</sub>

---

## Also in production

<div align="center">

| Project | What it is | Stack |
|:---|:---|:---|
| **[BBS Pay Commission 2025](https://v0-bbss-urvey-ft.vercel.app/)** | Nationwide opinion survey for the **Bangladesh Bureau of Statistics** — multi-step resumable forms, strict server-side validation, rate limiting, audit logging. Runs in government at `opinionsurvey.paycommission2025.gov.bd` | `Next.js` `PostgreSQL` |
| **[AlgoViz](https://algo-viz-peach.vercel.app/)** | 155+ NeetCode problems played back step by step — the pointer moving, the window sliding, the tree unfolding. 17 categories, Bengali and English | `Next.js 16` `Zustand` `Framer Motion` |
| **[NurApp](https://prayertime-two.vercel.app/)** | Offline-first Islamic companion PWA. **No backend, no database, no account, no tracking.** Prayer times from trigonometry, Qibla from a bearing calculation, all scripture bundled | `Next.js 15` `Zustand` `adhan.js` |
| **[FlowTrack](https://flow-track-nu.vercel.app)** | Eleven finance modules that usually sit behind a subscription — transactions, loans, savings goals, six-month analytics, PDF statements — given away free | `Next.js` `MongoDB` `Recharts` |
| **[Legal Case Management](https://legal-case-sage.vercel.app)** | Three law firms, one deployment, zero shared rows. Hearings, deadlines, client matters and a per-case audit history | `Next.js` `MongoDB` `Prisma` |
| **[Next.js Learning Hub](https://nextjs-learning-hub.vercel.app)** | A full Next.js curriculum taught in Bengali — for developers who shouldn't have to learn the framework in a second language first | `Next.js` `MongoDB` `Prisma` |
| **[Jannati Traders](https://jannati-traders-billing.vercel.app)** | Replaced a trading business's carbon-copy invoice book with a catalogue, ledger, PDF invoicing and a sales dashboard that gets opened | `Next.js` `MongoDB` `Prisma` |
| **[Online Assessment Platform](https://online-assessment-platform-one.vercel.app)** | The digital counterpart to SmartOMR — timed MCQ exams with automatic scoring and a per-question breakdown on submit | `Next.js` `MongoDB` `Prisma` |

</div>

## Built for other developers

<div align="center">

| Tool | What it does |
|:---|:---|
| **[Schema Designer](https://schema-designer-eta.vercel.app)** | Draw an ER diagram on canvas, define columns and relations, export working PostgreSQL DDL or a Prisma schema |
| **[Prisma for Dummies](https://prisma-for-dummies.vercel.app)** | The Prisma reference I wanted when I started — models, relations, migrations and real query patterns, all copyable |
| **[GitHub Command Guide](https://github-command-guideline.vercel.app)** | Categorised Git & GitHub CLI reference — branching, rebasing, stashing, and the recovery commands you need at 2am |

</div>

---

## How I work

<div align="center">

| | |
|:---|:---|
| **Production-hardened** | Every project listed is deployed and in use by a real organisation — not a demo |
| **Multi-tenant by design** | Isolation lives in the schema, enforced through RBAC guards, with every access logged |
| **Hardware integration** | ZKTeco biometric terminals over ADMS; TWAIN scanners over a native binding |
| **Four databases in anger** | Prisma across MySQL, PostgreSQL, MongoDB and SQLite |
| **Offline-first** | Electron packaging, native module rebuilds, service workers, zero-backend PWAs |
| **I run the servers** | Ubuntu, Nginx, PM2, SSL, backups, and the 2am log reading |
| **Read the domain first** | A grace question, a shift crossing midnight, a hearing deadline — the domain has rules the brief never mentions |
| **Replies in under 2 hours** | Milestone updates you can see, documentation on handoff, support after it |

</div>

---

## Currently building

<div align="center">

| | | |
|:---|:---|:---:|
| **ICT Shikhi — chapter 6** | Remaining textbook figures, the last labs, then a board-paper generator per chapter | 🟢 Active |
| **HajiraPro v2** | Advanced leave workflows, a mobile PWA for punch-in, configurable payslip templates | 🟢 Active |
| **SmartOMR Desktop v5** | Multi-scanner batching, and a sync path reconciling an offline machine back into the cloud tenant | 🟡 In dev |

</div>

---

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sakibzaman255/sakibzaman255/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/sakibzaman255/sakibzaman255/output/github-contribution-grid-snake.svg" />
  <img alt="Contribution graph" src="https://raw.githubusercontent.com/sakibzaman255/sakibzaman255/output/github-contribution-grid-snake-dark.svg" width="98%" />
</picture>

</div>

---

## Tell me what's breaking, or what you want built

Open to freelance contracts, full-time roles and open-source collaboration.

<div align="center">

| | |
|:---|:---|
| **Email** | [sakibzaman255@gmail.com](mailto:sakibzaman255@gmail.com) |
| **LinkedIn** | [linkedin.com/in/sakibzaman255](https://www.linkedin.com/in/sakibzaman255/) |
| **Portfolio** | [rafiqulhasansakib.vercel.app](https://rafiqulhasansakib.vercel.app/) |
| **Where** | Dhaka, Bangladesh · GMT+6 · remote worldwide, on-site within Dhaka |
| **Hours** | Sun–Fri · 9 AM – 10 PM · replies within 2 hours |
| **Languages** | English (fluent) · Bengali (native) |
| **Education** | BSc Computer Science & Engineering — North South University |

</div>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:000000,45:1A0A00,75:8C3A08,100:D97757&height=170&section=footer&text=Let%27s%20build%20something%20that%20runs.&fontSize=26&fontColor=FFFFFF&fontAlignY=72&desc=Rafiqul%20Hasan%20Sakib%20%C2%B7%20Dhaka%2C%20Bangladesh&descAlignY=88&descSize=14&descColor=FFD4A8" width="100%" />

**⭐ [github.com/sakibzaman255](https://github.com/sakibzaman255)**

</div>
