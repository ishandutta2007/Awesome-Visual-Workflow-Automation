# Awesome-Visual-Workflow-Automation

# Awesome Visual Workflow Automation

> A curated list of top Visual Workflow Automation platforms — both SaaS/Hosted commercial solutions and open-source alternatives for building no-code and low-code automations with a visual canvas.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Zoho Flow](#zoho-flow)
  - [Zapier](#zapier)
  - [Make](#make)
  - [Microsoft Power Automate](#microsoft-power-automate)
  - [Tray.io](#trayio)
  - [Workato](#workato)
  - [Bardeen](#bardeen)
  - [Relay.app](#relayapp)
- [Open-Source Software](#-open-source-software)
  - [n8n](#n8n)
  - [Activepieces](#activepieces)
  - [Apache NiFi](#apache-nifi)
  - [Node-RED](#node-red)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Visual Workflow Automation platforms. These are not open-source but are included as reference points for feature comparison.

### Zoho Flow
**Type:** AI-powered hybrid iPaaS with visual builder  
Zoho Flow connects 1,000+ cloud and on-premises apps with a drag-and-drop workflow builder. The 2026 release introduced **Zia**, an AI assistant that generates workflows from natural language descriptions — you describe what you want, and Zia builds the initial flow for you to refine . It supports polling APIs, webhooks, templated emails, and RSS feeds as triggers, plus an on-premises agent for secure access to local systems. Troubleshooting allows restarting entire workflows or rerunning specific parts. As part of the Zoho ecosystem, it integrates deeply with Zoho One apps alongside third-party services like Google and WordPress .  
**Best for:** Teams in or near the Zoho ecosystem wanting AI-assisted workflow generation with hybrid cloud/on-prem connectivity.

### Zapier
**Type:** The incumbent no-code automation platform  
Zapier connects 7,000+ apps with trigger-action workflows. It is the most widely adopted platform for non-technical users, with a massive integration library and a gentle learning curve. Multi-step Zaps support filters, formatters, and paths. **Limitation:** Pricing scales per task, which can become expensive at volume; complex data manipulation is limited compared to more developer-oriented platforms.

### Make
**Type:** Visual automation with granular data control  
Make provides a visual scenario builder with powerful data shaping, iteration, and error handling. Its canvas shows the flow of data between modules, and it supports complex branching, aggregators, and iterators. **Trade-off:** The scenario model takes longer to learn than simple trigger-action chains, but it offers more control for users who need to transform data between steps [citation:9].

### Microsoft Power Automate
**Type:** Business-user automation within Microsoft ecosystem  
Power Automate empowers business users and citizen developers to build workflows without IT involvement, with a visual designer and hundreds of connectors to Microsoft and third-party services [citation:2]. It integrates with Azure Logic Apps for more advanced scenarios. **Best fit:** Organizations already standardized on Microsoft 365, Dynamics, and Azure, where Power Automate flows can be embedded into SharePoint, Teams, and other Microsoft surfaces.

### Tray.io
**Type:** Enterprise iPaaS with embedded automation  
Tray.io provides a visual workflow canvas with 650+ pre-built connectors, JSONata data mapping, and a Connector SDK for custom integrations [citation:13]. Its **Embedded** offering lets SaaS vendors embed automation capabilities directly into their own products. Features include workspaces for dev/prod separation, callable workflows for reusable functions, and Insights for graphical health monitoring [citation:3]. Pricing is custom per workspace + task.

### Workato
**Type:** Enterprise automation for citizen integrators  
Workato is built from the ground up to serve both IT and business users through a single design interface. It combines enterprise-grade security and governance with consumer-grade ease of use [citation:6]. Features include a conversational bot-building platform for Slack and Teams, cross-enterprise visibility for IT governance, and a Connector SDK for custom applications. Recipes can be complex, supporting multi-step business processes across cloud and on-premises systems.

### Bardeen
**Type:** Browser-based AI automation agent  
Bardeen lives in the browser as an extension, automating web apps and websites without requiring separate sign-ups for tools you do not use. Its **AI agent** approach presents a plan for your approval before executing multi-step tasks, and it can learn from recorded actions [citation:14]. Features include web scraping, data extraction, and integrations with ChatGPT, Google Sheets, and CRM tools. SOC 2 Type 2 compliant with 300,000+ users [citation:4][citation:14].  
**Best for:** Sales, recruiting, and operations teams automating browser-based repetitive tasks (LinkedIn scraping, data transfer between web apps) without building full backend workflows.

### Relay.app
**Type:** Human-in-the-loop workflow automation  
Relay.app differentiates with **Human-In-The-Loop** functionality: workflows can pause at defined steps for a person to make a judgment call, provide input, or approve an action before continuing [citation:5]. This makes it suited to operationalized SOPs where not everything can or should be automated. It integrates with Asana, Linear, and other tools, and users frequently cite its clean UI and responsive support as advantages over Zapier [citation:5].  
**Best for:** Teams automating processes that require occasional human judgment, approvals, or context-dependent decisions.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Visual Workflow Automation platforms. All listed projects offer source code you can deploy on your own infrastructure.

### n8n
**Stack:** TypeScript / Node.js | **License:** Sustainable Use License (source-available, not OSI)  
n8n is the most widely adopted open-source (source-available) workflow automation platform, with 208.9k GitHub stars and 250k+ community members [citation:8]. It provides a visual canvas with **500+ native integrations**, plus any API via HTTP and any agent via MCP. Workflows can mix visual building with custom code (JavaScript/Python) where needed. Key differentiators include **full visibility into agent decisions**, human-in-the-loop approval steps, replay of past runs for debugging, and enterprise features like SSO, RBAC, and on-premises deployment [citation:8]. Trusted by Vodafone, Huel, and other enterprises for security operations and AI-first workflows.  
**Important:** The license is the **Sustainable Use License**, which is source-available but restricts certain commercial resale. It is not OSI-approved open source, though self-hosting for internal use is permitted [citation:9].  
**Best for:** Technical teams wanting a powerful, extensible automation platform with AI agent capabilities and the option to self-host without per-task pricing.

### Activepieces
**Stack:** TypeScript | **License:** MIT (Community Edition)  
Activepieces is a **MIT-licensed** open-source automation platform positioned as a more permissively licensed alternative to n8n. The Community Edition is free to self-host with no license fees [citation:9]. It includes a visual builder, a built-in AI chat that can describe a process and publish a live flow, and RBAC/audit logs on paid tiers. MoneyGram, Moneypenny, and Alan run Activepieces in production [citation:9]. **Trade-off:** Some enterprise controls require a paid plan, and the integration library, while growing, is smaller than n8n's.  
**Best for:** Teams wanting a genuinely MIT-licensed, self-hostable automation platform without the source-available restrictions of n8n.

### Apache NiFi
**Stack:** Java | **License:** Apache 2.0  
Apache NiFi is an Apache-governed dataflow automation platform focused on **data processing and distribution** rather than SaaS app-to-app integration. It provides a browser-based UI for designing, controlling, and monitoring flows, with features including guaranteed delivery with retry and backoff, provenance tracking with graph data lineage, horizontal scaling via clustering, and secure configuration with TLS and SSO [citation:10]. It supports native Python processors and a REST API for orchestration.  
**Best for:** Organizations needing robust, auditable data pipelines between systems — especially in cybersecurity, observability, and event stream processing — rather than marketing or business-user automation.

### Node-RED
**Stack:** Node.js | **License:** Apache 2.0  
Node-RED is a low-code programming tool for event-driven applications, built on Node.js's event-driven model. Its visual flow editor lets users wire together nodes to collect, transform, and visualize real-time data [citation:11]. The community has contributed over **5,000 nodes and flows**, making it highly extensible. It runs on low-cost hardware like Raspberry Pi as well as in the cloud.  
**Best for:** IoT, home automation, industrial control, and edge computing scenarios where event-driven data flows need to be built visually without full application development.

---

## 📊 Comparison at a Glance

| Software | License | Type | Self-Hosted | Free Tier | AI Features | Best For |
|----------|---------|------|-------------|-----------|-------------|----------|
| **Zoho Flow** | Proprietary | Hybrid iPaaS | ❌ | (Zoho plans) | ✅ Zia generation | Zoho ecosystem + on-prem |
| **Zapier** | Proprietary | No-code automation | ❌ | ✅ (limited) | Limited | Broadest app coverage |
| **Make** | Proprietary | Visual automation | ❌ | ✅ (limited) | Limited | Granular data shaping |
| **Power Automate** | Proprietary | Business automation | ❌ | ✅ (M365) | Copilot | Microsoft 365 estates |
| **Tray.io** | Proprietary | Enterprise iPaaS | ❌ | ❌ | Merlin AI | Embedded automation |
| **Workato** | Proprietary | Enterprise automation | ❌ | ❌ | Limited | Citizen integrators + governance |
| **Bardeen** | Proprietary | Browser AI agent | ❌ | ✅ (limited) | ✅ AI agent plans | Browser task automation |
| **Relay.app** | Proprietary | HITL automation | ❌ | ✅ (limited) | ✅ | Human-in-the-loop workflows |
| **n8n** | Sustainable Use | Source-available | ✅ | ✅ (self-host) | ✅ AI agents | Powerful self-hosted + AI |
| **Activepieces** | MIT | Open-source automation | ✅ | ✅ (self-host) | ✅ chat builder | MIT-licensed self-hosted |
| **Apache NiFi** | Apache 2.0 | Dataflow automation | ✅ | ✅ | ❌ | Data pipelines + provenance |
| **Node-RED** | Apache 2.0 | Event-driven flows | ✅ | ✅ | ❌ | IoT + edge automation |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Visual Workflow Automation platform that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source (or clearly note the license if source-available but not OSI-approved, as with n8n's Sustainable Use License).

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
