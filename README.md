# Awesome-Resource-Allocation-Capacity-Planning

# Awesome Resource Allocation & Capacity Planning

> A curated list of top Resource Allocation and Capacity Planning platforms — both SaaS/Hosted commercial solutions and open-source alternatives for visualizing team workloads, forecasting availability, and balancing utilization across projects.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Resource Guru](#resource-guru)
  - [Runn](#runn)
  - [Float](#float)
  - [Forecast](#forecast)
  - [Teamdeck](#teamdeck)
  - [Saviom](#saviom)
  - [Smartsheet Resource Management](#smartsheet-resource-management)
- [Open-Source Software](#-open-source-software)
  - [LibrePlan](#libreplan)
  - [Capacinator](#capacinator)
  - [CapacityTwin AI](#capacitytwin-ai)
  - [OpenProject Resource Management](#openproject-resource-management)
  - [TaskJuggler](#taskjuggler)
  - [d3-scheduler](#d3-scheduler)
  - [Jira Capacity Tracker](#jira-capacity-tracker)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Resource Allocation and Capacity Planning platforms. These are not open-source but are included as reference points for feature comparison.

### Resource Guru
**Type:** Visual resource scheduling with availability tracking
Resource Guru provides a clean, calendar-based interface for scheduling people and equipment, with real-time availability visibility, utilization reports, and leave management. It is known for its simplicity and fast setup, making it a common choice for agencies and professional services teams wanting visual resource planning without complex configuration.

### Runn
**Type:** Resource and capacity planning with project forecasting
Runn combines resource scheduling with project forecasting, offering a timeline view of allocations, capacity vs. demand charts, and budget tracking. It is positioned for organizations needing both forward-looking capacity planning and actual time tracking, with integrations into project management and time-tracking tools.

### Float
**Type:** Visual resource scheduling with task-level allocation
Float provides a visual timeline for scheduling team members across projects, with drag-and-drop allocation, utilization reports, and budget tracking. It is widely adopted by agencies and consultancies for its clean interface and focus on day-to-day scheduling rather than complex project management.

### Forecast
**Type:** AI-powered project and resource management
Forecast (by ProSymmetry) combines project management with resource allocation, using AI to suggest optimal assignments based on skills, availability, and project requirements. It is positioned for organizations wanting intelligent automation alongside traditional resource planning.

### Teamdeck
**Type:** Resource scheduling with time tracking and leave management
Teamdeck provides resource scheduling, time tracking, and leave management in a single platform, with a focus on utilization visibility and project profitability. It is suited for teams wanting an integrated view of who is working on what and how much capacity remains.

### Saviom
**Type:** Enterprise resource management with forecasting
Saviom provides enterprise-grade resource management with capacity planning, utilization tracking, and project forecasting. It is positioned for large professional services organizations needing sophisticated resource optimization and reporting.

### Smartsheet Resource Management
**Type:** Work management with resource views
Smartsheet's Resource Management add-on provides resource allocation views, workload tracking, and capacity planning within the broader Smartsheet work management platform. It is the natural choice for organizations already using Smartsheet for project tracking.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Resource Allocation and Capacity Planning tools. The open-source ecosystem spans **full project management suites with resource modules**, **standalone capacity planners**, **simulation tools**, and **embeddable scheduling components**.

### LibrePlan
**Stack:** Java / PostgreSQL | **License:** AGPL-3.0
LibrePlan is a long-standing open-source web-based project management platform designed for project planning, **resource allocation, governance, and collaboration** [citation:2]. Since 2009, it has been used internationally and is available under AGPL, making it suitable for public administrations, municipalities, educational institutions, and NGOs seeking self-hosted project governance without proprietary SaaS dependency [citation:2]. Key resource features include assigning resources to tasks manually or automatically based on criteria, calendar-based holiday management, **resource utilization and workload visibility**, detailed resource allocation planning, and time-sheet entry for actuals [citation:8]. Version 1.6.0 added issue/risk logs, document repositories, and expanded email notifications [citation:2]. Deploys via Docker Compose [citation:8]. **Trade-off:** It is a full project management platform rather than a dedicated capacity planning tool, with a correspondingly broader learning curve.
**Best for:** Public sector organizations and project-driven teams wanting a proven, self-hosted platform with resource allocation integrated into full project governance.

### Capacinator
**Stack:** Node.js / React / SQLite / Electron | **License:** MIT
Capacinator is a **resource capacity planning and allocation management system** built specifically for project teams [citation:1]. It provides project management, team member management, and resource assignments with **conflict detection** for identifying overallocations. The dashboard shows analytics across projects and people, and Excel files can be imported for bulk setup. Data is stored locally (with platform-specific app data paths), and it is packaged as a standalone Electron executable [citation:1]. **Trade-off:** It is a standalone desktop application rather than a web-hosted platform, limiting real-time collaboration across distributed teams.
**Best for:** Project managers wanting a focused, local-first capacity planning tool with conflict detection and no server infrastructure.

### CapacityTwin AI
**Stack:** Python / Streamlit / Docker | **License:** Open Source
CapacityTwin AI is a lightweight **"what-if" simulator** that shows whether a team can deliver its workload on time, who is overloaded, and what changes when plans change [citation:15]. Given people (working hours, skills, days off) and tasks (effort, priority, deadline, dependencies), it builds a day-by-day schedule and reports available capacity, utilization, projected completion dates, missed deadlines, and bottlenecks. The key differentiator is **scenario comparison**: it shows plain before/after differences when someone is away, hours change, or priorities shift — for example, demonstrating that adding developer hours changes nothing while adding designer hours fixes every deadline [citation:15]. The engine is deterministic (same input, same output) with no AI dependency; explanations are template-based. Deploys via Docker Compose with Streamlit [citation:15]. **Limitation:** Deliberately simple model (fixed effort estimates, one task per person, greedy scheduler, no uncertainty) intended for planning conversations, not performance decisions [citation:15].
**Best for:** Team leads and freelancers wanting a decision-support simulator to test capacity scenarios before committing to deadlines, particularly where bottlenecks are not obvious from total hours.

### OpenProject Resource Management
**Stack:** Ruby on Rails / PostgreSQL | **License:** GPL-3.0 (Community) / Enterprise
OpenProject 17.7.0 introduced a dedicated **Resource Management module** (Enterprise feature) that models hierarchical departments, role-based user attributes, and individual working time models [citation:5][citation:11]. Managers get a central view for searching, filtering, and comparing employees by department, qualification, availability, and current utilization. A **timeline view** highlights overallocations and planning conflicts, allowing resources to be assigned directly from the timeline. The **Staffing view** shows suitable employees for a need, including their suitability and current workload [citation:11]. The module can inherit organizational structure from LDAP. **Important:** Resource management is gated to Enterprise plans; the Community edition includes project management but not this specific module [citation:5].
**Best for:** Existing OpenProject users or organizations wanting enterprise-grade resource management integrated with a mature open-source project management platform, accepting the Enterprise licensing for the resource module.

### TaskJuggler
**Stack:** Ruby | **License:** GPL-2.0
TaskJuggler is a free and open-source project management tool with a **text-based planning approach** rather than Gantt chart editing [citation:14]. It covers the complete spectrum from project scoping through resource assignment, cost and revenue planning, and risk management. It is positioned for "serious project managers" who want flexible, scriptable planning with precise control over resource constraints. **Trade-off:** The text-based interface is a significant departure from visual scheduling tools, with a steep learning curve for teams accustomed to drag-and-drop planning.
**Best for:** Technical project managers wanting scriptable, precise resource and capacity planning without a GUI dependency.

### d3-scheduler
**Stack:** TypeScript / D3.js | **License:** Open Source (npm)
d3-scheduler is an open-source **D3.js resource scheduler and timeline** with interactive calendar views, drag-and-drop events, resizing, resource allocation, and Gantt-style planning [citation:7]. It displays **scheduled hours, task count, and capacity percentage** in the sidebar, supports hierarchical department groupings, and includes Critical Path Method (CPM) calculation with zero-float highlighting [citation:7]. It is distributed as a React component (`<Scheduler />`) or vanilla JavaScript class, with full TypeScript declarations. Performance is stress-tested at 10,000 events across 100 rows [citation:7]. **Trade-off:** It is a **UI component/library** rather than a complete application — you build the data layer, persistence, and user management around it.
**Best for:** Developers wanting to embed a capable resource scheduling timeline into their own application, accepting responsibility for the surrounding application infrastructure.

### Jira Capacity Tracker
**Stack:** Java / Spring Boot / Jira API / Google Sheets | **License:** Open Source (per repository)
Jira Capacity Tracker is a Spring Boot application that integrates with Jira to provide **team capacity overview, resource availability forecasting (30-day view), overload detection, and utilization tracking** [citation:3][citation:9]. It fetches Jira issues in real time, tracks story points and velocity, and can generate Google Sheets with color-coded capacity data. Automated sync runs every 5 minutes, with email notifications for daily summaries [citation:9]. **Trade-off:** It is tightly coupled to Jira (requiring Jira API access and project keys), and the Google Sheets integration adds an external dependency. It is a companion tool rather than a standalone planning platform.
**Best for:** Jira-centric teams wanting capacity visibility derived directly from their existing issue data, particularly those already using Google Sheets for planning.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Capacity Forecasting | Conflict Detection | Self-Hosted | Best For |
|----------|---------|-------|----------------------|---------------------|-------------|----------|
| **Resource Guru** | Proprietary | Cloud | ✅ Utilization | (Visual) | ❌ | Simple visual scheduling |
| **Runn** | Proprietary | Cloud | ✅ Demand vs capacity | ✅ | ❌ | Project + resource forecasting |
| **Float** | Proprietary | Cloud | ✅ Utilization | (Visual) | ❌ | Agency day-to-day scheduling |
| **LibrePlan** | AGPL-3.0 | Java/PostgreSQL | ✅ Workload | ✅ | ✅ | Full PM + resource governance |
| **Capacinator** | MIT | Node.js/Electron | ✅ Analytics | ✅ | ✅ (Desktop) | Local capacity planning |
| **CapacityTwin** | Open Source | Python/Streamlit | ✅ What-if scenarios | ✅ Bottleneck | ✅ | Scenario simulation |
| **OpenProject RM** | GPL/Enterprise | Ruby/PostgreSQL | ✅ Timeline | ✅ Overallocation | ✅ | Enterprise PM + resources |
| **TaskJuggler** | GPL-2.0 | Ruby | ✅ Scriptable | ✅ Constraints | ✅ | Precise scriptable planning |
| **d3-scheduler** | Open Source | TypeScript/D3 | ✅ Capacity % | (CPM) | ✅ (Library) | Embeddable scheduler UI |
| **Jira Capacity** | Open Source | Spring Boot | ✅ 30-day forecast | ✅ Overload | ✅ | Jira-derived capacity |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Resource Allocation or Capacity Planning tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem **splits** between **full project management platforms with resource modules** (LibrePlan, OpenProject), **focused capacity planners** (Capacinator, Jira Capacity Tracker), **simulation and scenario tools** (CapacityTwin AI), and **embeddable UI components** (d3-scheduler). **LibrePlan** is the most established self-hosted option with over 15 years of history and AGPL licensing suitable for public sector sovereignty [citation:2]. **CapacityTwin AI** uniquely addresses the scenario-testing gap — showing that adding developer hours may change nothing while adding designer hours fixes every deadline [citation:15]. **OpenProject** offers the most polished enterprise resource management, though the resource module requires an Enterprise subscription [citation:5].

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
