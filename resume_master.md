<!--
═══════════════════════════════════════════════════════════════════════════
  resume_master.md — MASTER SOURCE OF TRUTH (content only; not for submission)
═══════════════════════════════════════════════════════════════════════════

  This file holds every defensible bullet in its fullest honest form. Generate
  a role-targeted resume by filtering bullets, then EXPORT TO PDF/DOCX — raw
  Markdown is never submitted to a job portal, and all HTML comments below must
  be stripped on export.

  ── PER-BULLET METADATA ───────────────────────────────────────────────────
  Each bullet carries a trailing HTML comment (invisible when rendered):

      <!-- roles:eng,data | since:2022 | verify:doc-volume | conf:unaided -->

  roles:   which role-types the bullet suits. Vocabulary (fixed):
             eng  = software / engineering
             data = data engineering / analysis / DS
             ai   = AI / ML / LLM-focused roles
             pm   = product / program management
             ops  = operations / manufacturing
             all  = include in every version
  since:   OPTIONAL approximate time anchor (YYYY or YYYY-MM) for traceability.
           Present only where it aids verification; never a forced prefix.
  verify:  Present on ANY bullet with a hard metric (counts, volumes, $, %).
           The slug names the claim you must be able to defend in an interview.
  conf:    OPTIONAL honesty flag for skills/tech:
             unaided  = can use without assistance (→ belongs in Skills)
             assisted = used but AI-implemented or pair-built (→ frame in bullet)
             rusty    = real but not current; verify before claiming
  REVIEW:  A bare REVIEW token marks something Harry must confirm/correct.

  ── GENERATING A ROLE-TARGETED VERSION ────────────────────────────────────
  1. Pick a target role-type (e.g. `eng`).
  2. Keep every bullet whose roles: list contains that type OR `all`.
  3. Drop the rest. Reorder/trim to one page as needed.
  4. Strip ALL <!-- ... --> comments.
  5. Export to formatted PDF/DOCX for submission.

  ── SCOPE ──────────────────────────────────────────────────────────────────
  Content is scoped to the April 2026 master (resume_harry_sood_master_20260409).
  College/early-career material not in that resume — the Projects section
  (ESPAStar, Mcity/Innoviz, M-Fly), the older CAD/analysis tools, and Hobbies —
  was intentionally excluded. It still lives in resume_harry_sood_master_20220530.docx
  if ever needed again.

  ── OPEN REVIEW ITEMS / DECISIONS ────────────────────────────────────────────
  • chipsID mobile-app subsection added (iOS / React Native, Android planned).
  • Test counts deliberately omitted everywhere — the test suite was authored by
    Claude Code, not Harry; app bullets stay at "an automated test suite" (no numbers).
  • JavaScript still excluded from Skills (not claimed unaided).
  • conf:assisted marks work Harry designed/directed but Claude Code implemented.
═══════════════════════════════════════════════════════════════════════════
-->

# HARRY SOOD

San Diego, CA | (901) 921-1040 | harry.hs.sood@gmail.com | US Citizen | Active DoD Secret Clearance

---

## SKILLS

<!-- Skills = "can use unaided." Items needing a confidence call are flagged conf:REVIEW. -->

- **Programming:** Python (Pandas, NumPy, Matplotlib, SciPy, OpenPyXL) | SQL | MATLAB | C++ <!-- roles:eng,data -->
- **Cloud & Infrastructure:** Azure (Functions, Durable Functions, ADLS, Blob Storage) | GCP (Cloud Storage, Google Sheets API) <!-- roles:eng,data,ai -->
- **Data & Analytics:** Excel | Jupyter Notebooks | Power BI | ETL Pipeline Development | Statistical Analysis | Signal Processing <!-- roles:data,eng -->
- **Tools & Software:** Visual Studio Code | Git | Windows, macOS, Linux | Microsoft Office Suite | Agile Workflow <!-- roles:all | note: "Microsoft Office Suite" is roles:pm,ops only — drop it from eng/ai exports -->
- **AI-Assisted Development:** Claude Code | coding agents (agent-integrated workflow) <!-- roles:eng,ai | conf:unaided (tool use only) -->

---

## EXPERIENCE

### Senior Data Engineer — General Atomics Aeronautical Systems
San Diego, CA | July 2022 – Present

**Generative AI Data Pipeline Development**

- Architected and implemented a scalable Azure data pipeline to ingest, classify, and route proprietary company documents from OnBase into Azure ADLS blobs, enabling production-ready AI-driven indexing <!-- roles:eng,data,ai | since:2022 -->
- Deployed durable Azure Functions with eternal orchestration to automatically process 50,000+ documents on initial load and an average of 50 additional documents per week; eliminated IT-dependent manual processes <!-- roles:eng,data,ai | verify:doc-volume (50,000+ initial / ~50 per week) -->
- Engineered fault tolerance via file-by-file orchestration, Azure Table state tracking, batch finalization to resolve race conditions, and scheduled data validation; achieved zero data loss across all environments <!-- roles:eng,data | verify:zero-data-loss -->
- Hardened pipeline with environment-driven configurability, Git-based version control, and local Linux testing to accommodate shifting upstream conventions and evolving requirements without service interruption <!-- roles:eng,data -->
- Use AI-assisted development tools (Claude Code, coding agents) daily within an agent-integrated workflow to investigate issues, refactor at scale, and extend platform capability as a small team <!-- roles:ai,eng | conf:unaided (tool use; honest attribution) — AI-targeted versions only -->

**Flight Data Analysis**

- Conducted 100+ flight log analyses — parsing telemetry data from a repository of 150,000+ logs across 14 UAV variants, each with 1,300+ signals — to support investigations, establish performance baselines, and train junior engineers <!-- roles:eng,data | verify:log-repo (100+ analyses / 150,000+ logs / 14 variants / 1,300+ signals) -->
- Develop custom event detection scripts and synthetic signals to identify behavioral patterns and anomalies across datasets spanning as many as 200,000 events per analysis <!-- roles:eng,data | verify:event-count (up to 200,000 events) -->
- Deliver tailored visualizations and Power BI dashboards scaled to dataset size and stakeholder needs, enabling engineering and program teams to interpret complex flight data and inform decisions <!-- roles:data,pm -->
- Ensure signal integrity across a diverse fleet by processing and filtering downlinked telemetry data using statistical outlier analysis, threshold-based detection, and aeronautical domain expertise <!-- roles:eng,data -->

**Root Cause Analysis (RCA) & Cross-Functional Consulting**

- Operate as an internal consultant on two to three multi-month RCA investigations per year, jumping into unfamiliar subsystems, rapidly becoming a domain expert, and delivering unbiased findings on failures that eluded other teams <!-- roles:eng,data,pm | verify:rca-frequency (2–3 per year) -->
- Interface directly with internal engineering teams, program management, and external customers to define analysis requirements, present conclusions, and translate complex data insights into actionable decisions <!-- roles:pm,ops,data -->
- Designed a preliminary data pipeline bridging engineering and manufacturing operations for a new aircraft program, enabling the machine shop to track part schedules; helped accelerate first flight to meet a year-long program timeline <!-- roles:pm,ops,data | verify:program-timeline (year-long; first-flight contribution) -->
- Supplement data analysis with hands-on participation in operations including engine tests, starter generator inspections, and datalink troubleshooting to validate and contextualize results <!-- roles:data,ops -->

### Co-Founder, Data & Infrastructure — chipsID LLC (IC Counterfeit Mitigation Services)
San Diego, CA | July 2022 – Present

**Mobile Application Development**

- Designed and own chipsID's iOS app — built in React Native/TypeScript (Android planned) on a Python/FastAPI backend — with a thin-client REST architecture where the app holds no credentials and per-request access gating prevents leaking non-public part data <!-- roles:eng,ai | since:2025 | conf:assisted (design+architecture mine; implementation via Claude Code) -->
- Built with AI-assisted development (Claude Code) — directed implementation and an automated test suite across frontend and backend, deployed via Google Cloud Run and EAS Build (TestFlight) <!-- roles:eng,ai | conf:assisted (all code/tests authored by Claude Code; my role was design + prompt direction) -->

**Database & Cloud Infrastructure Development**

- Established GCP Cloud Storage infrastructure with automated Python backend to manage part image repositories, generate links, and orchestrate file uploads across buckets; enabled platform-agnostic image sourcing and fast retrieval <!-- roles:eng,data -->
- Implemented a MySQL database on GCP for component tracking, then migrated to a Google Sheets-based data layer after evaluating cost, team accessibility, and efficiency; leveraged built-in revision control for metadata collaboration <!-- roles:eng,data -->
- Built backend features including advanced filtering, search persistence, and API integration to connect GCP Cloud Storage and metadata to the web platform for seamless part discovery <!-- roles:eng -->

### Project Engineer — General Atomics Aeronautical Systems
San Diego, CA | July 2021 – June 2022

**Software Tools & Data Systems**

- Expanded software tools suite from 4 to 9 custom applications, maintaining full ownership across backend logic, CLI and Excel-based interfaces, and comprehensive documentation; ensured team-wide usability through training and support <!-- roles:eng,pm | verify:tool-count (4 → 9 apps) -->
- Integrated tools across multiple data sources including GOLD depot, SharePoint, Power BI, and legacy systems to track component obsolescence, LRU replacements, and program supply chain risk; delivered insights to external stakeholders <!-- roles:eng,data,pm -->
- Structured tools with upstream change resilience; achieved zero runtime logic issues after team deployment; upon request, returned post-departure to enhance and add features based on evolving program needs <!-- roles:eng -->

**Modernization & Obsolescence Mitigation**

- Spearheaded a successful $3M tech refresh of the Certifiable Ground Control Station's (CGCS) computer systems <!-- roles:eng,pm,ops | verify:refresh-cost ($3M) -->
- Redesigned the CGCS's C-Band video architecture to minimize failure points and non-recurring engineering costs <!-- roles:eng -->
- Executed mitigation strategies to defend against supply chain shortages and obsolescence of critical components <!-- roles:pm,ops -->

### Engineering Intern — General Atomics Aeronautical Systems
San Diego, CA | June 2020 – August 2020

**Software Tools Development**

- Created a custom suite of interlinked tools to increase team efficiency, resulting in estimated annual savings of 780 engineer labor hours ($195,000/year at $250/hour) <!-- roles:eng,pm | verify:labor-savings (780 hrs / $195,000 / $250 per hr) -->
- Programmed data integration software pulling from Windchill, SAP, and team-managed spreadsheets to track the impact of obsolete parts on associated end products <!-- roles:eng,data -->

### Researcher — University of Michigan, College of Engineering
Ann Arbor, MI | May 2018 – April 2020

**Formally Verified Autonomous Systems**

- Validated and verified autonomous vehicle systems through formal proofs for Toyota-sponsored research program <!-- roles:eng | since:2019 -->
- Modeled autonomous vehicle collision avoidance through robust simulations under various dynamic parameters <!-- roles:eng | since:2018 -->

---

## EDUCATION

### University of Michigan, College of Engineering — Ann Arbor, MI

- **M.Eng. Space Engineering** | GPA: 4.0/4.0 | Focus: Systems Design — Class of 2021 <!-- roles:all | verify:gpa (4.0) -->
- **B.S.E. Aerospace Engineering** | GPA: 3.4/4.0 | Minor: Computer Science — Class of 2020 <!-- roles:all | verify:gpa (3.4) -->

---

## PUBLICATIONS

- Aakash Abhishek, Harry Sood, Jean-Baptiste Jeannin. 2020. *Formal verification of swerving maneuvers for car collision avoidance.* ACC 2020. IEEE. https://doi.org/10.23919/ACC45564.2020.9147679 <!-- roles:eng,data -->
- Aakash Abhishek, Harry Sood, Jean-Baptiste Jeannin. 2020. *Formal verification of braking while swerving in automobiles.* HSCC 2020. ACM. https://doi.org/10.1145/3365365.3382217 <!-- roles:eng,data -->

---

## CERTIFICATIONS

- FAA Private Pilot Certificate | Aircraft Single Engine Land (ASEL) <!-- roles:all -->
