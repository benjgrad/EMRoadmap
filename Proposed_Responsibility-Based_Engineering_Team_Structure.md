# Proposed Responsibility-Based Engineering Team Structure (Method 2026 Strategy)

## Document Brief

This document outlines a comprehensive strategy for reorganizing Method's engineering teams around customer-facing responsibilities to achieve our 2026 strategic vision of delivering tailored experiences for SMB users.

### Key Sections

**Strategic Overview:**
- [Motivations](#1-motivations) - Why transformation is essential for Method's future:
  - [The Cost of Organizational Misalignment](#the-cost-of-organizational-misalignment) - How current structure creates delivery bottlenecks
  - [The SMB Market Opportunity](#the-smb-market-opportunity) - Untapped potential in small business software
  - [The AI-Powered Software Revolution](#the-ai-powered-software-revolution) - Industry disruption and competitive positioning
  - [Strategic Vision: Method as the SMB Operating System](#strategic-vision-method-as-the-smb-operating-system) - Our ambitious 2026 goal
  - [The Transformation Imperative](#the-transformation-imperative) - Why the cost of inaction exceeds the effort to change
- [Problem Statements](#2-problem-statements) - Detailed analysis of current challenges:
  - [Internal Team Friction](#internal-team-friction) - Dependency entanglement and low team autonomy
  - [Product Gaps for SMB Customers](#product-gaps-for-smb-customers) - User engagement and customization challenges

**Proposed Solution:**
- [Team Structure Overview](#3-proposed-responsibility-based-team-structure) - High-level approach and principles
- [Proposed Teams](#teams-and-responsibilities):
  - [Insights Team](#insights-team) - Data synthesis and intelligence for company and customers
  - [Action Automation Team](#action-automation-team) - Workflow automation and no-code platform reliability
  - [User Experience Team](#user-experience-team) - In-platform navigation and customer education
  - [Internal Tools Team](#internal-tools-team) - Reducing internal bottlenecks for faster delivery
  - [Visualization Team](#visualization-team) - Customer data manipulation and front-end components
  - [Integrations Team](#integrations-team) - External platform automation and connectivity
  - [Auth Team](#auth-team) - Authentication and authorization for multi-tenant businesses
  - [AI Solutions Team](#ai-solutions-team) - AI-powered custom app generation and validation
- [Coordination and Role Relationships](#coordination-and-role-relationships) - How teams collaborate effectively

**Technical Implementation:**
- [System Architecture Diagrams](#4-system-architecture-diagrams) - Visual mapping of team ownership to platform components

**User-Centered Design:**
- [Customer Personas](#5-customer-personas) - Six key SMB user roles guiding feature development:
  - [Owner / General Manager](#persona-owner--general-manager) - High-level business oversight and strategic decisions
  - [Office Administrator](#persona-office-administrator) - Day-to-day operations and administrative tasks
  - [Sales Lead (Sales Manager)](#persona-sales-lead-sales-manager) - Revenue generation and team management
  - [Finance Manager (Bookkeeper/Accountant)](#persona-finance-manager-bookkeeperaccountant) - Financial records and compliance
  - [Customer Support Representative](#persona-customer-support-representative) - Customer service and issue resolution
  - [Inventory/Operations Manager](#persona-inventoryoperations-manager) - Supply chain and operational efficiency

**Implementation Strategy:**
- [Migration Path](#6-migration-path-to-the-new-structure) - Four-phase transition plan from current to target state
- [Industry Best Practices & References](#7-industry-best-practices--references) - Supporting research and proven methodologies

### Expected Outcomes

This transformation aims to deliver:
- **Increased Team Autonomy** - Reduced dependencies and faster decision-making
- **Improved User Experience** - Role-tailored interfaces and workflows for each SMB persona
- **Enhanced Delivery Speed** - Independent deployments and parallel development streams
- **Better System Reliability** - Modular architecture with clear ownership boundaries

---

## 1. Motivations

The need for organizational transformation at Method stems from both immediate operational challenges and long-term strategic imperatives. Our current structure is fundamentally misaligned with our goals of delivering exceptional value to SMB customers while scaling our internal capabilities.

### The Cost of Organizational Misalignment

*Current structure creates a "coordination tax" that severely limits delivery velocity and innovation.*

Method's engineering teams are trapped in a web of dependencies that dramatically reduces effectiveness:

- **87.5% delivery failure rate** when three teams must collaborate on features¹
- **Innovation paralysis** as teams fear breaking shared platform components
- **Accountability vacuum** where no single team owns end-to-end outcomes
- **Technical debt accumulation** from risk-averse, patch-based solutions

### The SMB Market Opportunity

*SMBs need role-specific software experiences but current solutions force them into one-size-fits-all approaches.*

Small businesses represent massive untapped potential with unique requirements:

- **Low adoption rates**: Only 1-2 power users typically engage while 3-15 stakeholders remain underserved
- **Immediate value expectation**: SMBs abandon software that doesn't provide obvious benefit within days
- **Customization paradox**: Need tailored workflows but lack resources for complex implementations
- **Multi-tenant complexity**: Franchises and PE portfolios require sophisticated access control we don't provide

### The AI-Powered Software Revolution

*AI is democratizing software creation, creating both opportunity and existential threat for traditional platforms.*

The software industry is undergoing fundamental disruption:

- **Natural language programming**: Non-technical users can now create sophisticated applications through conversation
- **Quality trust gap**: AI generates code quickly but businesses need confidence in reliability and maintainability
- **Platform advantage**: Our no-code infrastructure uniquely positions us to combine AI generation with governance
- **Competitive moat opportunity**: Robust QA and validation can differentiate us from pure AI code generators

### Strategic Vision: Method as the SMB Operating System

*Transform from CRM platform to the central nervous system for all SMB operations by 2026.*

Our ambitious but achievable vision encompasses four pillars:

- **Role-Aware Intelligence**: Every stakeholder sees exactly what they need, when they need it
- **Seamless Integration**: All external SMB tools connect automatically, eliminating data silos
- **AI-Powered Adaptability**: Custom solutions generated through conversation, validated through rigorous testing
- **Multi-Tenant Sophistication**: Enterprise-grade access control for franchises and PE portfolios

### The Transformation Imperative

*The cost of maintaining the status quo far exceeds the effort required for organizational change.*

Aligning teams around customer outcomes rather than technical domains will deliver four critical advantages:

1. **Accelerated Innovation**: Customer-problem-focused teams outperform technical-layer-organized teams
2. **Scaled Quality**: Clear ownership eliminates the diffusion of responsibility that creates platform fragility
3. **Market Leadership**: Solving real SMB problems positions Method as the default choice for growing businesses
4. **Future-Proofing**: This structure leverages emerging technologies while maintaining platform strengths

**The question isn't whether we should reorganize, but whether we can afford not to.**

## 2. Problem Statements

Method faces critical challenges that prevent us from delivering value effectively to both our internal teams and SMB customers. These issues fall into two main categories:

### Internal Team Friction

Our current organizational and technical structure creates significant barriers to efficient product development:

#### [Dependency Entanglement Between Teams](#dependency-entanglement-between-teams)

- Most stock apps depend heavily on a shared no-code platform (including runtime, schema, action sets, screen designer)
- This leads to coordination bottlenecks—teams can't confidently ship features without affecting or waiting on others
- Research shows that each additional inter-team dependency dramatically increases delays; having just three teams dependent on each other can reduce the chance of on-time delivery to 1 in 8¹

#### [Low Autonomy for App Teams](#low-autonomy-for-app-teams)

- App teams can't move independently because they're blocked by changes or limitations in platform infrastructure
- This reduces velocity and limits innovation at the edge of the platform
- Teams cannot make decisions unilaterally; any significant change requires approval or coordination with other teams
- This not only slows delivery but also stifles innovation – developers are less likely to experiment or propose bold improvements

#### [Update Fragility](#update-fragility)

- Customizations made by customer-facing teams create tension with automated app update processes
- Rollouts are fragile and can unintentionally break user-configured experiences
- Because the no-code platform is tightly coupled, even minor updates can require full platform regression testing
- Teams often queue changes into infrequent big releases, resulting in fewer, larger releases that carry more risk

#### [Lack of Clear Ownership Across Platform Components](#lack-of-clear-ownership-across-platform-components)

- It's unclear who owns what—teams overlap in responsibility for runtime behaviors, visual components, and automation logic
- This causes confusion, duplicated work, and missed opportunities for platform-wide improvements
- When "everyone" owns a part of a feature, no single team feels fully accountable for the outcome

As Conway's Law predicts, a product's design reflects the organization's communication structure⁵⁶ – currently, that structure is convoluted, so the software has become convoluted as well.

### Product Gaps for SMB Customers

Our current approach creates significant barriers to customer success and growth:

#### [Stock Apps Don't Engage Individual Users Within Customer Organizations](#stock-apps-dont-engage-individual-users-within-customer-organizations)

- **Underlying Problem**: The current stock apps are generalized and not tailored to the responsibilities of distinct roles (e.g. Office Manager, Sales Lead, Finance Coordinator)
- **Impact**: Only one or two "power users" tend to adopt the product fully, while other users disengage or rely on external tools
- **Result**: Lower stickiness, lower expansion, and fewer advocates within each customer organization

For instance, an Owner or General Manager wants a quick snapshot of the business (sales trends, cash flow, staff performance) but instead sees generic CRM screens not tailored to their high-level overview needs. A Sales Lead cares about pipelines, lead follow-ups, and team performance metrics – yet the out-of-the-box design may not highlight these effectively, forcing them to manually pull data or use workarounds.

#### [Customer-Specific Customizations Are Difficult to Support Across Updates](#customer-specific-customizations-are-difficult-to-support-across-updates)

- **Underlying Problem**: SMBs frequently need workflows that diverge from stock templates, and these are delivered via Professional Services or customer self-configuration
- **Impact**: These customizations aren't always visible to product/platform teams, and often lack automated test coverage or safe update mechanisms
- **Result**: Updates risk breaking functionality, slowing down release cadence and damaging customer trust

This creates a vicious cycle where the fear of breaking customizations further slows our ability to innovate and improve the platform.

#### [Lack of Insight Into Real-World Usage and Friction Points](#lack-of-insight-into-real-world-usage-and-friction-points)

- **Underlying Problem**: The platform doesn't systematically capture feedback, feature usage, or pain points across personas or customer segments
- **Impact**: Teams miss opportunities to learn from real behavior, limiting their ability to improve workflows or prioritize the right enhancements
- **Result**: Product evolution is driven more by anecdote or high-touch feedback than representative data

Ultimately, **limited persona relevance is hampering Method's growth**. SMBs have very limited time and seek tools that immediately fit their workflow⁷. If Method's platform requires significant tweaking or doesn't speak each role's language, busy users either disengage or seek alternate solutions. Method must evolve from a generic CRM to a **role-aware business platform**, where each type of SMB user finds direct, tailored value.

## 3. Proposed Responsibility-Based Team Structure

### Overview of the Team Model

We propose reorganizing our development organization into **8 cross-functional teams oriented around key strategic capabilities**, rather than around technical layers or broad product domains. Each team – roughly 6 to 8 people ("two-pizza team" size) – will own an **end-to-end slice of functionality** that delivers on specific business objectives. In practice, this means a team has all the skills needed (frontend, backend, QA, and ideally a product manager and designer) to **build, test, and deploy features** in their responsibility area with minimal hand-offs.

This structure addresses both **customer-facing capabilities** (insights, visualization, integrations) and **internal enablement** (internal tools, auth, AI solutions) while maintaining platform reliability (automation, user experience). Each team's mission is defined in terms of **strategic value delivery** to ensure alignment with Method's goals of serving SMB users more effectively while scaling our internal capabilities.

The guiding principle is that teams act as **mini start-ups** within their domain: they have the freedom to decide how to achieve their objectives (tools, approach) while being accountable for results. This approach draws inspiration from the Spotify model's emphasis on autonomy, communication, and quality⁹, while incorporating modern concepts of **stream-aligned teams** from Team Topologies¹⁰¹¹. Below, we outline the specific teams, each with its name, mission, scope of ownership, and example responsibilities.

## Teams and Responsibilities

### Insights Team

**Mission:** Gather and synthesize data into actionable insights for both Method as a company and our customers. This team transforms raw information from diverse sources into intelligence that drives strategic decisions and enhances product value.

**Scope & Ownership:** The Insights Team owns the end-to-end data intelligence pipeline, from collection through analysis to presentation. This includes processing PS team transcripts, customer databases, emails, support tickets, user behavior analytics, and external market data. They develop both internal business intelligence capabilities and customer-facing analytics features.

**Key Responsibilities:**
• **Internal Intelligence:** Mining PS team transcripts and customer communications to identify product gaps, feature requests, and market trends that inform strategic planning
• **Customer Analytics:** Building dashboards and reports tailored to SMB personas (Owner dashboards, Sales performance metrics, Financial reporting, etc.)
• **Predictive Intelligence:** Developing models to forecast customer churn, identify upsell opportunities, and predict feature adoption
• **Data Pipeline Management:** Ensuring clean, reliable data flows from all internal and customer sources into our analytics infrastructure
• **Cross-functional Intelligence:** Providing data-driven insights to other teams about user behavior, feature usage patterns, and market opportunities

### Action Automation Team

**Mission:** Deliver workflow automation and ensure execution reliability of our no-code platform. This team focuses on making automation powerful, reliable, and accessible to SMB users while maintaining platform stability.

**Scope & Ownership:** The Action Automation Team owns the entire automation engine, from workflow design tools to execution infrastructure. They ensure automations run reliably at scale and provide users with intuitive tools to automate their business processes without coding knowledge.

**Key Responsibilities:**
• **Workflow Engine Reliability:** Hardening the automation execution engine with proper error handling, retries, rollback mechanisms, and monitoring
• **No-Code Workflow Designer:** Building intuitive interfaces for users to create complex business automations without technical expertise
• **Action Library Expansion:** Developing and maintaining a comprehensive library of pre-built actions (email, SMS, integrations, data operations, etc.)
• **Performance Optimization:** Ensuring automations execute efficiently even at high volume and complex workflows don't degrade platform performance
• **Quality Assurance:** Building testing frameworks to validate automation logic before deployment and monitor execution reliability

### User Experience Team

**Mission:** Optimize in-platform navigation and customer education to ensure users can effectively utilize Method's capabilities. This team focuses on user onboarding, discoverability, and guided experiences.

**Scope & Ownership:** The User Experience Team owns the overall user journey within Method, including navigation patterns, onboarding flows, help systems, and educational content. They ensure users can discover and effectively use platform features.

**Key Responsibilities:**
• **Navigation & Information Architecture:** Designing intuitive navigation patterns that help users efficiently move between features and find what they need
• **Onboarding & Education:** Creating guided tours, tutorials, and contextual help that educate users on platform capabilities
• **User Research & Testing:** Conducting user research to identify pain points and validate design decisions across different SMB personas
• **Accessibility & Usability:** Ensuring the platform is accessible and usable across different devices, abilities, and technical skill levels
• **Feature Discoverability:** Helping users discover and adopt new features through thoughtful UI/UX design and progressive disclosure

### Internal Tools Team

**Mission:** Reduce internal bottlenecks that prevent us from delivering quickly by building tools and processes that accelerate development, support, and operations.

**Scope & Ownership:** The Internal Tools Team owns development tools, internal dashboards, support tools, and operational efficiency systems that enable other teams to work more effectively.

**Key Responsibilities:**
• **Developer Experience Tools:** Building CI/CD improvements, testing frameworks, deployment tools, and development environment optimizations
• **Support Tools:** Creating customer support dashboards, debugging tools, and automated issue resolution systems
• **Operational Dashboards:** Developing real-time monitoring, alerting, and business intelligence tools for internal operations
• **Process Automation:** Automating manual internal processes like customer onboarding, billing operations, and support ticket routing
• **Knowledge Management:** Building internal wikis, documentation systems, and knowledge sharing tools

### Visualization Team

**Mission:** Provide customers with the ability to intuitively manipulate and understand their own data through sophisticated front-end components and visualization tools.

**Scope & Ownership:** The Visualization Team owns all customer-facing data visualization components, chart libraries, interactive dashboards, and data exploration tools that help SMB users understand their business data.

**Key Responsibilities:**
• **Interactive Chart Library:** Building and maintaining a comprehensive library of interactive charts, graphs, and data visualizations
• **Dashboard Builder:** Creating drag-and-drop dashboard building tools that allow customers to create custom views of their data
• **Data Exploration Tools:** Developing intuitive interfaces for customers to filter, sort, and drill down into their business data
• **Mobile-Optimized Visualizations:** Ensuring data visualizations work effectively on mobile devices for on-the-go business monitoring
• **Performance Optimization:** Optimizing visualization rendering for large datasets and ensuring smooth interactions

### Integrations Team

**Mission:** Drive automation of external platforms that our customers use by building seamless, reliable connections between Method and third-party systems.

**Scope & Ownership:** The Integrations Team owns all external platform connections, API integrations, data synchronization, and third-party automation capabilities.

**Key Responsibilities:**
• **Platform Connectors:** Building and maintaining integrations with QuickBooks, Xero, email marketing tools, e-commerce platforms, and other business software
• **API Management:** Developing robust API authentication, rate limiting, error handling, and data transformation capabilities
• **Real-time Synchronization:** Ensuring data stays synchronized between Method and external systems with minimal latency
• **Integration Marketplace:** Building a marketplace or library of pre-built integrations that customers can easily enable
• **Custom Integration Tools:** Providing tools for power users or consultants to build custom integrations without deep technical knowledge

### Auth Team

**Mission:** Handle authentication and authorization within our platform, specifically supporting multi-tenant businesses like franchises and private equity portfolios.

**Scope & Ownership:** The Auth Team owns user identity management, permission systems, multi-tenant architecture, and access control across the entire platform.

**Key Responsibilities:**
• **Multi-Tenant Architecture:** Building robust tenant isolation and management systems for franchise and portfolio business models
• **Role-Based Access Control:** Developing granular permission systems that support complex organizational hierarchies
• **Single Sign-On (SSO):** Implementing enterprise SSO capabilities for larger customers with existing identity systems
• **Audit & Compliance:** Building audit trails and compliance reporting for businesses with regulatory requirements
• **Security Infrastructure:** Implementing security best practices, threat detection, and incident response capabilities

### AI Solutions Team

**Mission:** Leverage AI to provide customers with custom applications without requiring software or no-code knowledge, using chat interfaces and robust QA workflows to deliver validated solutions.

**Scope & Ownership:** The AI Solutions Team owns AI-powered app generation, natural language interfaces for software creation, and quality assurance frameworks for AI-generated solutions.

**Key Responsibilities:**
• **Conversational App Builder:** Developing AI agents that can understand customer requirements through natural language and generate appropriate no-code solutions
• **Requirements Translation:** Building systems that translate business requirements into technical specifications and app configurations
• **AI-Powered QA Framework:** Creating comprehensive testing and validation systems that ensure AI-generated apps meet quality standards and business requirements
• **Solution Templates:** Developing a library of proven app patterns and business logic that the AI can leverage to build reliable solutions
• **Confidence & Validation Systems:** Building mechanisms to assess the quality and appropriateness of AI-generated solutions before deployment
• **Human-AI Collaboration Tools:** Creating interfaces where Method consultants and customers can collaborate with AI to refine and perfect generated solutions

**Strategic Vision for AI Solutions:** This team positions Method at the forefront of the AI-powered software generation revolution. By combining AI's ability to understand and generate solutions with robust QA workflows, Method can offer the confidence and reliability that businesses need when adopting AI-generated software. The focus on validation and human oversight differentiates Method from pure AI code generation tools by ensuring business-grade quality and reliability.

## Coordination and Role Relationships

While each team has a clear mission and greater autonomy, coordination mechanisms are critical to keep everyone aligned towards Method's product vision (especially tailoring to SMB roles). We propose adopting elements of the Spotify model for cross-team collaboration and knowledge sharing:

**Tribe Structure:** All the teams above together form a "Product Tribe" focused on Method's platform. The Director of Product (the audience of this report) could act as the Tribe Lead, ensuring that the work of each squad (team) ties back to the overall strategy. We anticipate ~5 teams (squads) in this tribe, which is well within the size a tribe can manage (Spotify tribes often comprise up to ~100 people)¹⁶. Regular tribe meetings (e.g., monthly) will showcase each team's progress on role-specific enhancements and foster alignment.

**Chapters (Discipline Alignment):** Developers, QA, designers, etc., across different teams will belong to chapters led by a senior specialist. For example, all front-end engineers across Data, Insights, Automation, etc., would form a Front-End Chapter. This ensures consistency in tech stack and best practices. The chapter lead (possibly a UI Architect) will help disseminate standards (like using the same UI library conventions set by the UX team). Chapters ensure that while squads are autonomous, the technical excellence and coherence are maintained across the organization¹⁷.

**Guilds (Communities of Interest):** We will establish guilds for broader topics that anyone passionate can join¹⁸. For instance, a "Persona Experience Guild" might bring together members from each team to discuss how features for a given SMB role are coming along, ensuring a holistic experience. Another guild could be "Quality and Performance" focusing on non-functional aspects across teams. Guilds are voluntary and span all teams; they're a key tool for cross-pollination of ideas without formal hierarchy.

**Shared Planning Rituals:** To manage cross-team dependencies and strategy alignment, we'll implement regular joint planning sessions. A quarterly planning meeting (akin to PI Planning in some agile frameworks) can be held where each team presents their upcoming quarter goals, key features, and any help needed from others. In these sessions, teams will identify any dependencies early and agree on sequencing – reducing surprises later. Additionally, we can run a bi-weekly Scrum-of-Scrums: a short sync where each team's representative shares progress and blockers, focusing on anything affecting other teams. This keeps inter-team coordination issues visible and resolved in real time.

**Team APIs & Interface Agreements:** As mentioned, each team will publish and socialize a "team API" – essentially a living document outlining what services/artifacts they own, how other teams can use them, and who to contact for what¹⁹²⁰. For example, the Automation Team might document how to request a new type of action to be added, or how the Data team can use their workflow triggers. By treating these interfaces seriously (similar to how microservices define APIs), we minimize friction: teams collaborate through well-defined touchpoints rather than ad-hoc requests. This approach draws from Team Topologies and has been shown to improve inter-team communication in remote and scaled setups²¹²².

**Product and Design Alignment:** We will also institutionalize a trio model (as per Spotify's Trio of Tribe Lead, Product Lead, Design Lead²³) at the tribe level. The Director of Product, along with a UX lead and an engineering lead, will regularly ensure that what each team is building fits the overall product narrative and design language for each persona. They meet perhaps bi-weekly to discuss cross-team product issues (e.g., "Are Owners getting a coherent experience across the features from Team A and Team B?"). This leadership trio then communicates adjustments to teams while still allowing teams autonomy in execution.

In summary, the new structure emphasizes **autonomy with alignment**. Teams have more control within their domains (as evidenced by the success of empowered squads in other companies²⁴), but we mitigate silo effects through deliberate coordination practices – guilds for knowledge sharing, shared planning for syncing roadmaps, and a strong product/design overview to keep the user experience seamless. The culture we aim for is one of "loosely coupled, tightly aligned" teams, where control is decentralized but everyone moves in the same strategic direction¹⁷¹².

## 4. System Architecture Diagrams

To better understand how this new team structure maps to Method's technology, it's important to visualize the platform architecture and then overlay team ownership. Below are two diagrams: (1) a high-level architecture of Method's no-code platform, and (2) the proposed team ownership of those components.

### Figure 1: High-level architecture of Method's no-code platform

Major services include the Screen Designer (UI Builder) for creating app interfaces, the Runtime Engine for executing app logic and serving the UI to users, the Schema Service which manages the data model and database, and the Action Engine for running automated workflows ("action sets"). External systems like QuickBooks integrate via an External Integrations service that syncs data into the platform. Arrows indicate key data or action flows (e.g., user actions go from the UI to the runtime; the runtime reads/writes data via the schema service; the action engine triggers on events and may update data or call external APIs). This architecture underpins Method's stock apps and customizations.

In this architecture, end-users interact through the UI (stock or customized screens) which are rendered by the Runtime. The Screen Designer is the tool that admins or Method consultants use to configure those UI screens (defining which fields, layouts, etc., are shown). When a user performs an action (like clicking "Save" on a form), the Runtime handles that event – it might update data through the Schema Service (e.g., saving a record in the database) and also trigger any relevant Action Sets in the Action Engine (for example, "after saving an invoice, trigger an email send"). The Schema Service represents the no-code data layer: it manages the structure of data (like which tables/fields exist, their relationships) and serves as an abstraction over the actual database/storage. The Action Engine executes automation scripts defined in a no-code manner (if X happens, do Y and Z). These automation rules are often set up in the Screen Designer (for instance, configuring that pressing a button runs a certain action set).

External Integrations (such as a QuickBooks sync service) run in the background or on-demand to keep Method's data in sync with other systems. For example, a scheduled job might pull new invoices from QuickBooks via their API and then use the Schema Service to insert them into Method's database. Likewise, when Method needs to push data out (say, a payment recorded in Method should update QuickBooks), the runtime or action engine will call the External Integration service to perform that API communication. The figure also implicitly includes authentication/authorization as part of runtime (ensuring users only see screens/data they are permitted to).

Overall, this high-level view shows a modular platform: UI/Screen config, data management, workflow engine, and integration connectors, all orchestrated by a runtime. The current challenge, as noted, is that these pieces are tightly coupled and largely managed as one unit (making changes risky). The next diagram illustrates how we'll assign clear ownership of these components to different teams, which is a step toward more modularity and resilience.

### Figure 2: Proposed team ownership overlay on platform architecture

Each colored cluster (dashed box) represents an engineering team and the components they primarily own. For example, the Data Ingestion Team (brown outline) owns the External Integrations service (handling data sync with external systems). The Automation Team (green) owns the Action Engine (workflows). The UX Team (blue) owns the Screen Designer and, in collaboration with Platform, the UI components at runtime. The Insights Team (orange) is responsible for Reporting & Analytics (not a single component in the base architecture, but a layer utilizing the data in the Schema Service to produce dashboards/reports). The Platform Core Team (purple) owns the foundational Runtime and Schema Service, as well as the overall database and system infrastructure. Arrows between components (unchanged from Figure 1) show how teams will need to interact via defined interfaces (e.g., Automation Team's engine writes data via Platform's schema service, Data Team's integrations pull data into the schema, etc.). This mapping ensures each team has clear responsibility areas and collaborates at well-defined integration points.

As illustrated, each major platform element falls under a team's ownership, aligning with the responsibility-based structure:

• **The Platform Core Team (purple)** owns the core Runtime and Schema Service. They provide the backbone on which all other functionality runs. In practice, this means Platform team members will work on core code that affects everyone (for example, how the system processes a screen's logic, or how data is queried and saved). By centralizing this in one team, we avoid situations where multiple teams make conflicting changes to critical infrastructure. Other teams will interface with these core services via stable APIs or extension points set by the Platform team.

• **The UX Team (blue)** owns the Screen Designer (UI Builder) and front-end component library. In the diagram, the Screen Designer is the tool that defines screens which the Runtime then renders. While the Platform team runs the engine, the UX team ensures the engine has what it needs to display beautiful, role-tailored UIs (e.g., UI metadata, templates). The UX team likely also influences the client-side portion of the Runtime (like a Javascript app or similar) to ensure screens behave as intended. The overlap between UX and Platform here will be managed by clear contracts – e.g., a defined interface for how screens are described (JSON, XML, etc.) that the runtime consumes. The division of responsibilities is such that UX focuses on what the user sees and how screens are built, while Platform ensures those definitions execute correctly and efficiently.

• **The Action Automation Team (green)** owns the Action Engine (Workflows). They have full responsibility for that component – its logic, its performance, and its integration with the rest. In operation, when a user action triggers a workflow, the Runtime notifies the Action Engine. The Automation team will ensure that interface is robust (e.g., the Action Engine exposes a function like `runWorkflow(workflowID, context)` that the runtime calls). The Action Engine in turn may call back to the Schema Service (to read/write data as part of a workflow) – again an integration point between Automation and Platform teams. By defining this usage as an internal API (with perhaps agreed data contract, transaction handling), we keep the teams decoupled yet cooperative.

• **The Data Ingestion Team (brown)** owns External Integrations. In the figure, you see this component connecting external systems to Method's Schema Service. The Data team's code will feed data into the Schema (and conversely extract data out) through well-defined endpoints – likely the Schema Service has API methods or is accessed via an ORM. The Data team, thus, works closely with Platform on any changes needed to support new data types or bulk operations. But importantly, they can add a new integration (say to Shopify or a new payroll system) without touching the core runtime or action engine – they just use the Schema Service API. This encapsulation lowers risk when extending integrations.

• **The Insight Generation Team (orange)** is mapped to a Reporting & Analytics layer (as added in the diagram). This isn't a single existing module but represents their responsibility to create new components or services for analytics. For instance, they might develop a reporting service that queries the main database (or a data warehouse). That service would interface with the Schema Service for data, or possibly read the database directly in a read-replica scenario (depending on implementation). In either case, their work is distinct: they focus on data retrieval and aggregation logic for insights, and the UI team helps display it. The interface here could be a reporting API or even materialized views in the database that the Platform team allows them to create. By delineating this, the Insights team can iterate on analytical queries and caching strategies independently.

This team-component mapping implements Conway's Law in a deliberate way: we structure our teams so that the software architecture will naturally evolve towards modular services with clear interactions²⁵²⁶. Each team's codebase can be somewhat isolated (maybe separate repositories or at least separate modules in a mono-repo with ownership rules). Interactions between modules (and thus teams) are the arrows – these should be turned into well-documented interfaces. For example, if the Automation team needs something from the Data team (like "please import these records as part of a workflow"), rather than reaching into each other's code, they use an API (maybe the Data team offers an API endpoint or library for importing, or the Automation engine raises an event that the Data integration service listens to). We expect that over time, the platform could be broken into microservices aligning to these components – e.g., a standalone integration service, a separate workflow service – enabling independent deployments by each team. Even if initially they remain in one codebase, this clear responsibility split is the first step to untangling the monolith.

In summary, these diagrams illustrate both the technical blueprint of Method's system and the mapping of that blueprint to team ownership. This alignment will help us achieve faster flow (teams work in parallel on different parts) and safer changes (a change in one module/team shouldn't break others if interfaces are respected). It's a move from a "big ball of code" to a platform of services coordinated by teams – a proven approach in modern software orgs (many companies have made similar journeys, guided by principles like domain-driven design and team alignment to architecture).

## 5. Customer Personas

A key part of tailoring the product experience is deeply understanding our **SMB user personas**. Below we define six common roles that Method serves. For each persona, we detail their goals, pain points, typical workflows, and key product needs. These personas will guide how each team prioritizes features and designs solutions (for instance, the Insights team will think about what reports a Finance Manager needs, while the UX team ensures an Inventory Manager's screens are efficient for their tasks).

### Persona: Owner / General Manager

**Role & Background:** The Owner (or GM) is the primary decision-maker in a small business. Often the founder or an executive, they wear many hats – overseeing operations, finance, and strategy. They might not use Method every day for data entry but log in frequently to check on the business or when critical issues arise.

**Goals:** Ensure the overall health and growth of the business. They focus on high-level KPIs: sales revenue, cash flow, customer satisfaction, project delivery status, etc. They want to identify trends (good or bad) early and make strategic decisions. Also, to enforce accountability – seeing which departments or individuals need attention.

**Pain Points:** Lack of visibility is a common pain. They often complain, "I can't easily see what's going on in each part of my business." Without tailored dashboards, they might resort to manually consolidating reports. They also face time constraints – they can't spend hours digging into data or navigating complex software. If the tool is too granular or not focused on their needs, it gets ignored. Additionally, Owners often feel that software doesn't "speak their language," bombarding them with details when they just want summaries and red flags. On the strategic side, they worry about adoption – if their team isn't using Method effectively, the investment is wasted. (Indeed, research finds SMB decisions are usually driven by owners, who need to see clear value²⁷.)

**Typical Workflows:** The Owner might log in weekly to review a dashboard of key metrics (sales this month vs. last, top overdue invoices, pipeline status, support ticket counts). They may use Method to approve exceptions – e.g., approving a big discount on a quote, or stepping in on a VIP customer issue. They could also use it for high-level planning, like reviewing forecasts or setting targets (if Method provides such tools). Owners often need to switch contexts quickly – a morning might start with reviewing sales, then an HR issue, then financials. So their ideal workflow in Method is jump in, get insights, and jump out (with actions delegated to their team).

**Key Product Needs:**
• **Executive Dashboard:** A one-page overview of the business, possibly configurable but with great defaults. It should highlight what needs the owner's attention (e.g., "7 invoices overdue >30 days" or "New large deal won today").
• **Alerts/Notifications:** Owners want notifications for exceptions or important events (e.g., a deal above $X closed, or inventory below threshold, etc.). This ties into automation – they'd configure triggers for what they care about.
• **Easy Drill-down:** While they don't want clutter, when something catches their eye (say a spike in expenses), they need to drill in or run a quick report. The product should allow an owner to click through a dashboard chart to see underlying data without needing to ask an analyst.
• **Mobile Access:** Owners are often on the go. A mobile-friendly view of key info (or mobile app) is crucial so they can check in from anywhere.
• **Team Usage Reports:** To manage adoption, an owner might want to see who on their team is (or isn't) using Method (login frequency, records updated, etc.). This helps them intervene if the tool isn't being utilized, thereby aligning with their goal of ROI on software.

**Design implication:** The Owner persona benefits most from work by the Insight Generation Team (for dashboards), the Automation Team (for alerts), and the UX Team (for ensuring information density is optimized on their screens). Our new structure ensures these needs don't fall through the cracks – they are explicitly someone's responsibility to deliver.

### Persona: Office Administrator

**Role & Background:** The Office Admin is the operational backbone of many SMBs. They handle a variety of administrative tasks: managing appointments, entering invoices/bills, onboarding new customers, running payroll or basic accounting tasks, etc. They are usually very hands-on with Method and likely one of the most frequent users of the system.

**Goals:** Keep the business running smoothly day-to-day. This includes making sure information is up-to-date (customer records, orders, schedules), ensuring bills and invoices are processed, and coordinating across departments. They often aim to reduce errors (no double-bookings, no missed emails to clients) and save time by streamlining recurring tasks.

**Pain Points:** Double data entry and manual work are huge pain points. If Method isn't integrated well, the Office Admin might have to enter data in multiple places (e.g., update QuickBooks and Method separately – something we aim to fix via integration). They also deal with information silos – e.g., sales has some data, support has other data; they often end up being the person to gather it all. Any lack of automation hits them hardest: they spend time on repetitive tasks (sending out reminders, updating spreadsheets) that they wish the system could automate. Another pain point is **complexity** – if the CRM screens are cluttered or not tailored, the Admin has to memorize workarounds ("When creating a new job, ignore Field X unless it's a consulting client" – these sorts of things cause friction). They benefit from clear, simplified processes. Lastly, Admins can be interrupted a lot; they need to pick up where they left off, so software should be forgiving and help them track what's done vs pending.

**Typical Workflows:** An Office Admin starts the day by checking for any new incoming information – e.g., new leads from the website (which they then assign to sales via Method), emails from customers (which they log or respond to), or bills to enter. They might use Method to generate invoices or receipts for customers, and then ensure those sync to QuickBooks. Throughout the day, they update records (address changes, new notes from calls, scheduling follow-ups). They also often pull basic reports – like an aged receivables report to call customers who owe money, or a daily shipments list for the warehouse. If something is wrong (e.g., an automation didn't send an email), people come to them first, so they also play the role of first-line support for Method internally, checking if data is entered correctly. Multitasking is constant – they jump between Method, email, phone, and Excel. Thus, having Method integrated and efficient is key to not dropping balls.

**Key Product Needs:**
• **Integrated Workflows:** The Admin benefits from tight integration between CRM and accounting, email, calendar, etc. For example, if Method can show QuickBooks info (like if a customer is overdue on payments) right on the customer screen, the Admin doesn't have to cross-check systems.
• **Automation of Routine Tasks:** They would love to automate things like payment reminders, appointment follow-up emails, task assignments. The easier we make it for them to set these up (via templates or one-click activation of common automations), the better.
• **Clear, Simplified UI for Data Entry:** Perhaps a special "Admin Console" that aggregates the tasks they need to do. Or simply well-designed screens (through our Screen Designer) that only show what's necessary for the Admin's workflows. For instance, when entering a new customer, maybe have a guided form with tooltips, rather than a generic form with dozens of fields.
• **Search and Cross-reference:** A powerful search in Method is a must-have for Admins. They often need to find a record quickly based on partial info (a phone number, or a first name, etc.). Also the ability to link items (attach a file to a customer, relate a contact to an account, etc.) from one place saves them time.
• **Error Prevention & Notifications:** If they forgot to fill something important or an automation failed, the system should notify them promptly (e.g., "This invoice didn't sync – click to retry"). This ties into both UX design and Automation reliability.

In our new structure, the Office Admin's needs intersect with almost every team's domain: Data Ingestion (for integration to avoid double entry), Automation (for routine task automation), UX (for good UI/UX on forms), and Platform (for search performance, etc.). Having well-defined personas ensures each team considers impacts on the Admin. For example, the Data team integrating Outlook calendar could drastically reduce an Admin's scheduling burden, or the UX team simplifying forms directly improves Admin productivity.

### Persona: Sales Lead (Sales Manager)

**Role & Background:** The Sales Lead is responsible for driving revenue. In an SMB, this could be the head of sales or just the most senior sales rep who also manages others. They spend a lot of time in CRM systems to track leads, opportunities, and team performance.

**Goals:** Close more deals and grow customer relationships. The Sales Lead wants to ensure that the sales pipeline is healthy – enough leads, progressing deals, and hitting monthly/quarterly targets. They aim to coach their sales team, so they need visibility into each rep's pipeline and activities. They also focus on improving conversion rates (turning leads into customers efficiently) and ensuring follow-ups happen on time so no opportunity slips through. Customer satisfaction can also be a goal – making sure promises made during sales are fulfilled, requiring coordination with other teams.

**Pain Points:** A major pain is lack of pipeline visibility or manual reporting. If the CRM doesn't give easy pipeline status, the Sales Lead ends up building spreadsheets or constantly asking reps for updates. Inefficient follow-up is another – e.g., leads not being contacted promptly or tasks falling through cracks because the system doesn't prompt reps effectively. They also struggle with data quality issues – duplicate leads, missing information, which can make forecasting inaccurate. In SMBs, Sales Leads often multitask with selling themselves, so time is limited for administrative tasks; a CRM that's cumbersome (or not tailored to their sales process) feels like a burden rather than a help. Another pain can be integration with marketing or support – for example, not knowing that a lead had a recent support issue or is on a marketing email list. If stock apps aren't integrated, the Sales Lead might lack context when pursuing a deal.

**Typical Workflows:** Daily, a Sales Lead will review the status of deals: checking Method's Opportunities or similar app to see new leads, deals in negotiation, deals closing soon. They might reassign or distribute leads that came in (if an Office Admin didn't already do so), ensuring each rep has a fair load. They often update forecasts – e.g., adjusting probabilities or values of deals, which ideally Method should roll up into a forecast report. The Sales Lead will also have 1-on-1s with reps, for which they use CRM data: looking at each rep's activities logged (calls made, emails sent) and pipeline progression. Weekly, they might run a pipeline review meeting, projecting Method's reports on a screen to discuss each deal's status. They also likely use Method to store key account info and may occasionally step in to help close a big deal (so they'll add notes or tasks on high-value opportunities). At month-end or quarter-end, they spend time generating sales performance reports for the Owner, which, if Method can do out-of-the-box, saves them huge effort.

**Key Product Needs:**
• **Pipeline Dashboard & Kanban:** A visual pipeline board (e.g., leads -> qualified -> proposal -> won) that's always up to date. The Sales Lead should be able to drag and drop deals or quickly see where bottlenecks are (e.g., many deals stuck in proposal stage).
• **Team Performance Metrics:** They need reports like "Calls/Emails per rep (activity report)", "Deals won vs target per rep", "Funnel conversion rates". These should be easily accessible, not require manual compilation. The Insights team would likely create a Sales Leaderboard or report suite for this persona.
• **Follow-up Automation:** The Sales Lead benefits from automations that ensure leads are contacted. For example, if a new lead is added without any follow-up logged in 2 days, alert the Sales Lead or automatically ping the assigned rep. Or sequence automations (cadence emails) that reps can use – the Automation team could build those templates.
• **Contact Management & Context:** When looking at an opportunity or account in Method, the Sales Lead wants a 360° view – recent support tickets (so they know if the client is happy or upset), any outstanding invoices (in case that affects negotiation), related contacts, etc. Integration and good UI design can bring this context to one place. This avoids them being blindsided in conversations.
• **Mobile/On-the-road access:** Sales Leads often travel or meet clients. They need to quickly pull up info on their phone – e.g., "What was our last quote to this client?" Method should support that either via a mobile app or responsive design.

The Sales Lead persona aligns closely with enhancements from the Insights Team (sales analytics), Automation Team (sales cadence automation), and UX/Experience (ensuring the CRM is optimized for sales workflows). By focusing on this persona, Method can differentiate itself as not just a generic CRM but one that truly understands a small sales team's needs. Our restructured teams would, for example, collaborate via a "Sales Persona Guild" to ensure features from different teams result in a cohesive solution for the Sales Lead.

### Persona: Finance Manager (Bookkeeper/Accountant)

**Role & Background:** The Finance Manager in an SMB could be an in-house bookkeeper, an external accountant, or simply the Office Admin doubling as one. They oversee financial records, ensure bills and invoices are processed, handle payroll or coordinate with external accountants, and care a lot about accuracy and compliance.

**Goals:** Maintain accurate financial records and ensure the business's financial stability. This includes timely invoicing, collections, bill payments, and financial reporting (P&L, cash flow). They also aim to ensure compliance (tax filings correct, audit trails in place). In context of Method, their goal is often to minimize duplicate data entry between CRM and accounting software, and to leverage CRM data for any financial insights (like sales pipeline translating into revenue forecasts).

**Pain Points:** Redundant work is a big one – if Method (CRM) and QuickBooks (accounting) aren't well integrated, the Finance person ends up re-entering data or constantly cross-referencing systems. This is not only tedious but prone to errors. Data mismatches (like an invoice amount in Method not matching QuickBooks) are their nightmare, as they have to reconcile and explain discrepancies. They also worry about security and proper access – not everyone should see financial data, so if the platform isn't granular in permissions, they get anxious (e.g., they may not want a sales rep to edit an invoice). Reporting limitations can frustrate them; if the CRM can't produce a needed report (like sales by product/service type, or monthly recurring revenue), they have to export to Excel and do it manually. Time spent on manual reconciliation or report prep is time away from more strategic finance tasks. Additionally, finance folks often operate on strict schedules (month-end close, etc.), so any system downtime or slow performance at critical times is a big pain.

**Typical Workflows:** Daily, a Finance Manager will check for any new sales (deals closed) that need invoicing. If Method is integrated to QuickBooks, a perfect workflow is: as soon as a deal is marked "Won" in Method, the Finance Manager either approves or automatically generates an invoice in QuickBooks. They then use Method to perhaps send that invoice to the customer or follow up on payments. They will also manage accounts receivable – e.g., using Method to track which customers owe money and sending reminders (or asking Sales to follow up). If they manage inventory or purchase orders, they'll track orders in Method and ensure bills from vendors are recorded. Monthly, they might run financial reports – if Method handles some sales reporting, they combine it with accounting data for a full picture. They might also maintain the product/service catalog and pricing in the system (ensuring Method's items match accounting items). During tax time or audits, they may extract a lot of data (customer lists, invoice logs) from Method as backup documentation. In essence, they straddle CRM and Accounting, trying to make them act as one.

**Key Product Needs:**
• **Seamless QuickBooks/Xero Integration:** This is paramount. Every invoice, payment, customer info, etc., should sync between Method and the accounting system with minimal clicks. And with proper controls (e.g., maybe only Finance Manager or Owner can approve syncing an invoice to QuickBooks to avoid junk data). Real-time sync or close to it is ideal.
• **Financial Reporting Dashboards:** While detailed accounting reports may live in QuickBooks, Method can provide at-a-glance financial metrics: sales vs. targets, receivables aging, expense tracking if relevant. Especially metrics crossing CRM and finance – e.g., "Sales pipeline vs. actual invoiced revenue" or "Outstanding quotes that might turn into invoices this month".
• **Robust Permissions/Roles:** The Finance Manager needs to ensure that sensitive data (like revenue figures, salary info if tracked, etc.) is only accessible to authorized roles. Method should allow setting those permissions easily, e.g., only Finance role and Owner see certain financial screens. Also, an audit log of changes to financial records would be comforting for them (to trace any errors).
• **Automated Reminders & Workflows for Financial Tasks:** For example, an automation that sends payment reminder emails to customers 5 days before due date, cc'ing the Finance Manager. Or a workflow that alerts Finance Manager if a high-value deal was closed without generating an invoice after 2 days. These help enforce financial discipline without manual tracking.
• **Data Export & Backup:** Finance folks often like to export data to Excel for analysis or backup. Method should make it easy to export lists of transactions, customers, etc. in a structured way. Also, integration to Excel or BI tools for custom reports could be beneficial.

By addressing the Finance Manager's needs, Method strengthens one of its selling points: being "the #1 CRM for QuickBooks users." The Data Ingestion Team is key here (ensuring flawless sync). The Platform/Core Team also plays a role in permissioning and data integrity. The Insights Team can deliver valuable combined reports. Our persona-centric approach means these requirements won't be afterthoughts – they are part of the planned scope for the respective teams. A Finance Manager who finds Method reduces their bookkeeping time and errors will be a strong advocate for the product.

### Persona: Customer Support Representative

**Role & Background:** The Support Rep (or Customer Service Rep) handles customer inquiries and issues. In SMBs, this could be a dedicated support agent or someone who splits time (e.g., an Office Admin who also answers phones). They use Method to track customer tickets, log calls/emails, and ensure issues are resolved.

**Goals:** Resolve customer issues efficiently and keep customers happy. They aim for quick response times, accurate answers, and ensuring no issue falls through the cracks. They also try to upsell or educate customers occasionally (turning a support call into an opportunity). If there's a support team, they want good collaboration and knowledge sharing.

**Pain Points:** Fragmented customer info is a big challenge – if the support rep has to go to multiple places to get a full picture (e.g., invoices in QuickBooks, previous communications in an email system, contract details in a file cabinet), it slows them down. They need a 360° view of the customer situation immediately. Lack of ticket tracking is another; some SMBs don't have a formal ticket system, so reps use spreadsheets or inboxes. If Method's stock app for support is not robust, they feel the pain of missing features like ticket prioritization or status tracking. Repetitive questions/answers – without a knowledge base or canned responses, reps waste time rewriting answers. And if the CRM isn't helping them, response times increase and customers get frustrated. They also deal with stress of unhappy customers, so any software friction (slowness, confusing UI) exacerbates their stress. Finally, communication gaps with other teams (sales promising something support can't deliver, or support not informing sales of an issue) can cause internal friction – they need the CRM to facilitate cross-team awareness.

**Typical Workflows:** A Support Rep's day starts by checking open tickets or issues. If Method has a Cases or Support App, they'll filter by new or high-priority cases. They respond to customers – maybe via email or phone – and log the interaction in Method (notes, status updates). They might escalate some issues to others (tag the Finance Manager if it's a billing issue, or the Sales Lead if it's an upsell opportunity). They frequently use customer data during the interaction: checking order history, last contact, any notes from sales. If Method integrates with an email system, they might reply directly from the CRM. They also set follow-up tasks if an issue can't be resolved immediately (e.g., "check back with customer in 3 days"). Throughout the day, as new inquiries come (calls or emails), they create new case records in Method and start the process. Weekly, if they have time, they might review common issues and draft template responses or solutions. If there's a small team, they might have a team meeting to discuss tough cases, where they could use Method's data to see trends (like "We got 5 complaints about feature X this week."). They could also be involved in customer onboarding or training – ensuring new customers are set up, which might involve checking if Method has all their data and if any welcome tasks are pending.

**Key Product Needs:**
• **Unified Customer View:** When a support rep opens a customer's record, they should see recent tickets/cases, recent purchases or interactions, and any notes from sales or finance that could be relevant. This prevents the rep from asking the customer redundant questions and gives context (e.g., "I see you just bought our product last month; sorry you're having an issue with it…").
• **Ticket Management Tools:** A way to log issues (cases) with statuses (New, In Progress, Resolved, etc.), priority, and assignment. Even if it's a simple app, it should support sorting and filtering so reps can manage their workload. Notifications when a ticket is assigned or updated would help keep everyone aligned.
• **Templates / Knowledge Base:** The ability to insert canned responses or have a repository of common solutions (could be as simple as text snippets or a linked wiki). If Method doesn't natively support a KB, maybe integration to an external one, but at least the rep should be able to quickly pull up FAQ answers.
• **Automation for Follow-ups:** If a case is in "Waiting on customer" status for 3 days, auto-send a reminder to the customer; or if a case is unresolved for too long, alert a manager. The Automation Team can implement these kind of support workflow automations to ensure nothing gets stuck.
• **Customer Self-Service Portal (Future):** Some CRMs allow customers to log in and view status or submit tickets. If Method has (or could have) a portal, support reps would benefit as it deflects simple queries. Even if not, at least an email acknowledgment to customers when they create a ticket would set expectations.
• **Integration with Communication Channels:** If possible, link Method with whatever channels customers come from – e.g., if a customer emails support@company.com, it auto-creates a case in Method. Or if they call, the rep can quickly create a case while on the phone. Reducing the data entry during a live call is important so they can focus on the conversation.

The Support Rep's needs will be addressed primarily by the UX Team (ensuring the support screens are user-friendly and show all needed info), the Data/Integration Team (for pulling in data like order history from external sources if needed), and the Automation Team (for triggers and alerts in support workflows). Although we haven't explicitly formed a separate "Support Team" in engineering (given limited dev capacity), these concerns are folded into our responsibility teams. For instance, if support cases are part of the stock app, maybe the UX or Platform team will own that baseline feature. By highlighting this persona, we ensure that improving the support experience isn't neglected – since a smooth support process can be a differentiator for Method in retention and upsells.

### Persona: Inventory/Operations Manager

**Role & Background:** This persona could vary: in a product-based business, it's an Inventory Manager focusing on stock levels, ordering, and fulfillment. In a service or project-based business, it might be an Operations Manager focusing on service delivery or project completion. We combine them here as someone who deals with the "back-end" of the business operations.

**Goals:** Efficiently manage the supply chain and service delivery. For an Inventory Manager, the goal is to have the right products in stock, avoid stock-outs or overstocks, and fulfill orders on time. For an Ops Manager, it's to ensure projects/tasks are completed on schedule and resources are utilized well. They want smooth coordination between sales (what's sold) and fulfillment (delivering it).

**Pain Points:** A classic pain is lack of real-time information on inventory or project status. If sales sells something that's out of stock and the inventory info in Method wasn't updated, it causes failure to deliver. If Method's stock app isn't robust, managers resort to spreadsheets for inventory tracking. Manual processes like updating stock after each sale by hand or not having automated re-order reminders lead to errors. If there is an e-commerce or POS system not integrated, that's double work or inconsistent data. For Ops, lacking a clear view of all ongoing projects or tasks can cause missed deadlines. Another pain is communication gaps: e.g., sales sells a custom item but doesn't communicate the specifics to operations, resulting in delays – the system should aid in bridging those gaps (through data or alerts). Forecasting demand is also tough if not supported: inventory needs to predict what to stock based on historical sales (something CRM data can help with if analyzed). In short, without a tailored system, the Inventory/Ops manager spends a lot of time firefighting – finding where things are stuck, chasing people for updates, and updating multiple systems.

**Typical Workflows:** For an Inventory Manager: daily they check stock levels of key items, likely via a report or the inventory app in Method. If something is low, they might create a purchase order (if Method supports it) to reorder. They also process fulfillment – when an order or invoice is created by sales, they pick/pack/ship goods and then update Method (or QuickBooks) to mark it shipped. They might also handle receiving shipments from suppliers and adding that to inventory. Weekly or monthly, they do stock reconciliations – comparing what Method says vs actual count (this could be an exported list from Method that they check). They coordinate closely with sales on any backorders or lead time issues. For an Operations Manager in services: they would use Method to track project tasks or work orders. Each day, they see what tasks are due, assign team members, and update statuses. They'll communicate with sales if a project is delayed or completed early. They might also use Method for resource scheduling (who is working on which project, do we have availability for a new job sold).

**Key Product Needs:**
• **Inventory Management Features:** This includes being able to log stock levels, set reorder points, generate POs, and track fulfillment status (order picked, shipped, delivered). Method might integrate with shipping carriers or at least allow input of tracking numbers. If these are not currently strong in Method, expanding them would help this persona. There's note that Method can track stock levels for manufacturing²⁸, indicating this is within scope.
• **Alerts for Low Stock:** An automation should alert the Inventory Manager (and maybe Purchaser) when inventory drops below threshold or when a big order comes in that exceeds stock. Also, if an order is open for too long unfulfilled, notify Ops Manager.
• **Integration with eCommerce/POS:** If the business sells online or in-store, Method should integrate those sales into the system so inventory is updated universally. The Data team might create connectors for Shopify, etc. to centralize order info.
• **Job/Project Tracking:** If Method has an app for jobs or work orders, ensure it's customizable for different industries. The Ops Manager needs to see all active jobs, their status, who's responsible, and any blockers. Possibly a calendar or Gantt view for scheduling would be useful. They should be able to attach files or notes (e.g., spec sheets, delivery instructions) to jobs.
• **Cross-module visibility:** For example, when looking at an inventory item, see open orders for it (so they know demand). Or when looking at a project, see the originating sale or contract. This prevents things falling through cracks between departments.
• **Reporting on Operations:** Inventory valuation reports, fulfillment rate (orders shipped on time %), for a manufacturing context maybe assembly/BOM tracking. For service ops, maybe utilization reports or project profitability if possible (tying hours or costs to projects). These help the Ops persona optimize and also report to the Owner.

The Inventory/Ops Manager persona will benefit from the Data Ingestion Team's work on integrations (bringing sales and inventory data together), the Automation Team's triggers (low stock, overdue tasks alerts), and the Insights Team's ops-focused reports. By clearly identifying their needs, we ensure our stock apps (or platform capabilities) cover not just CRM in the narrow sense, but the operational follow-through, which is key for SMBs. Method's promise is end-to-end workflow automation; addressing this persona is fulfilling that promise from sales through delivery.

**Note:** Each persona above has distinct needs, but there's overlap. For example, both the Owner and Finance Manager care about financial figures but in different granularity; both Sales Lead and Support Rep care about customer history but use it differently. By defining these personas, product development can identify where a feature for one persona might also help another (or how to tweak it). Our new responsibility-aligned teams will use these personas as a checklist to ensure coverage. We may even assign a persona champion within each team – someone who deeply thinks from, say, the Sales Lead's perspective, during design discussions. This user-centric approach, supported by the new team structure, will drive Method's 2026 goal of tailored experiences.

## 6. Migration Path to the New Structure

Transitioning from the current organization (and architecture) to this new responsibility-based model is a significant change. It must be handled incrementally and thoughtfully to mitigate risks. Here we outline a migration path covering team reorganization, technical refactoring, and risk mitigation:

### Phase 1: Preparation and Team Formation

- **Leadership Alignment & Vision Communication:** First, ensure all current team leads and stakeholders understand the why and what of this change. Present the new structure (perhaps using sections of this report) to get buy-in. Emphasize how this setup addresses current pain points (autonomy, faster delivery, quality for customers).

- **Define Clear Boundaries (Fracture Planes):** Analyze the existing codebase and application scope to outline bounded contexts or modules corresponding to the proposed teams. For example, identify all parts of the code related to "workflow actions," all parts related to "reports," etc. We may leverage fracture planes suggested by Team Topologies, such as business subdomains or even user personas¹⁰, to decide how to split the monolith. The target is that each new team can mostly work on one set of components with minimal overlap initially.

- **Reorganize Personnel into New Teams:** With ~50 developers, we might form about 5 main teams (as described). This could mean splitting existing larger teams or combining people from different current teams. For instance, if currently there's a "Backend team" and "Frontend team," we would peel off some backend and frontend devs into a cross-functional Data Ingestion Team, others into Automation Team, etc. We will assign interim tech leads for each new team, ideally those who have expertise in that area of the code. In parallel, assign product managers and UX designers to teams (even if shared across two teams initially due to headcount). We should also identify any gaps (maybe we need to hire or train someone for a specialized skill like data analytics for the Insights team).

- **Establish Team Charters:** Each new team should craft a one-page team charter (or Team API as earlier noted) detailing their mission, ownership scope, and initial backlog of responsibilities¹⁵²³. This helps clarify boundaries. For example, the Automation Team's charter might state "owns workflow engine, automation rules UI; other teams can request new automation features through us." These charters can be shared org-wide to set expectations on who does what.

### Phase 2: Module Carve-Out and Dual Operating Mode

- **Architectural Modularization:** Begin refactoring the codebase to separate along the lines of team responsibilities. We don't aim for a full microservices split immediately, but perhaps create modular libraries or packages for each area. For example, isolate the action engine code into its own directory/repository that the main app calls via an interface. Similarly, segregate reporting logic. Use techniques like the "strangler pattern" to peel functionality without breaking everything – i.e., develop new services or modules alongside the old until fully ready. During this, set up clear API interfaces between modules (even if just function calls or internal HTTP APIs) to mirror how teams communicate. This code separation enforces the team boundaries technically.

- **Domain Leads and Guild Support:** During this carving out, allow a temporary Architecture Guild (senior devs/architects from each team) to guide the module boundaries and avoid breaking contracts. They'll ensure that, for instance, the Data team's changes to how QuickBooks sync works doesn't break something the Automation team expects, by aligning on interfaces. Essentially, we apply the idea of "if you built it, you run it" gradually: as soon as a module is decoupled enough, the respective team fully takes over running it in production.

- **Operate in Parallel (Old vs New Structure):** Recognize that we can't flip a switch; likely there will be a period where the legacy setup and new setup coexist. We might still have some old "functional teams" or legacy product owners keeping the lights on in existing system, while new teams start delivering improvements in their domain. For example, the Insights Team might start building a new dashboard module even as the old reporting mechanisms remain for a while. It's important to manage this dual mode: have clear decision-making so new teams can push forward without waiting on old processes. We may sunset legacy committees or reassign those roles to empower the new team leads.

- **Deliver Early Wins in New Model:** To build confidence, identify one or two pilot projects that the new teams can tackle relatively independently. For instance, let the Automation Team build a small new feature (like a "workflow template gallery") from start to finish. Or the Data Team could implement a new integration that was backlogged. Delivering it faster than before, and with quality, will showcase the benefit of the new structure and rally support.

### Phase 3: Gradual Transition of Ownership and Shutdown of Old Structures

- **Shift Ownership of Existing Features:** Start formally transferring ownership of parts of the existing product to the new teams. For example, assign all bug tickets related to the screen designer to the UX Team. Have the Platform Core Team take over all platform performance and security issues. This might require some knowledge transfer sessions from those who built those features originally (if they are now in a different team or left). Use documentation and hands-on shadowing to bring new team members up to speed. As ownership solidifies, update internal documentation: code repositories should list the owning team, and support tickets should be routed to the right team's queue.

- **Refactor Teams' Backlogs and Processes:** Each team should establish its own agile rituals (planning, stand-ups, retros) if not already. They should maintain a backlog focused on their responsibilities. It's likely initially their backlogs contain a mix of new initiatives (for personas) and legacy bugfix/tech debt tasks. Balance these to ensure stability while moving forward. Introduce a lightweight coordination process for cross-team work – e.g., if the Insights Team needs a change in the schema from Platform Team, how to request and track that. Possibly implement a "request ticket" system or just use the shared planning meetings to line these up.

- **Role-Based Access & Data Migration:** On the technical side, as we tailor experiences to roles, we should enhance the role-based access control (RBAC) in the platform. The Platform Core Team might introduce new user role definitions (Owner, Admin, Sales, etc. as first-class roles in Method if not already) and permissions structures so that new persona-specific features can be properly restricted or shown. During migration, careful attention is needed that existing customers' permissions don't change unexpectedly. Possibly run the new RBAC in parallel (audit mode) to see if any differences before enforcing. Also, if splitting databases or services, plan data migration scripts and tests. For example, if we move the "cases" data to a new support module or service, ensure all data is carried over. We might do phased migration: copy data to new module, run both for a bit to verify, then cut over writes to new module. The Platform Team will orchestrate these efforts, with each team testing their domain's data integrity.

- **Gradual Service Extraction & Releasing Independence:** Over time, as modules firm up, consider extracting them into independent deployables (if beneficial). E.g., the Action Engine could become a microservice. The aim is each team can deploy their part without deploying the whole system – achieving continuous delivery for each stream. Initially, even within a monolith, we can simulate this by feature flags (teams release features dark and toggle on when ready for all users). Eventually, break down the CI/CD pipeline per team. This reduces the "monolithic release" pain and allows more agility. Conway's Law will start to work for us here: the software structure aligns with the team structure, making each decoupled and faster²⁹.

### Phase 4: Full Adoption and Optimization

- **Retire Old Team Habits:** Once the new teams are fully owning their domains, we can dissolve any residual old teams or roles. For example, if there was a "database admin team" separate before, their functions might now live in Platform Team – formally move those people or responsibilities over. Make sure performance review, hiring, etc., are all realigned to the new teams (people should have managers in their new team's chain). This cements the org change.

- **Monitor & Adjust Team Boundaries:** We should be open to adjusting the team scope if needed. Perhaps we discover the Insights Team has too broad a scope (if, say, they own both complex data warehousing and UI). We might split one team into two in the future (e.g., separate "Analytics Backend" vs "Reporting UI"). Or if two teams have a persistent heavy dependency, maybe their scopes need tweaking or they should merge. Use metrics like team delivery speed and dependency tracking to inform this. The goal is to have stream-aligned teams with minimal cognitive load per Team Topologies guidelines¹¹. Over time, create additional enabling teams if necessary (for example, a short-term Performance Task Force could be spun up from Platform team to solve a specific scaling issue, then retire).

- **Cultural Embedding:** Continue reinforcing the new culture – celebrate wins of teams acting autonomously, encourage innovation (hackathons within teams to address persona needs creatively), and use retrospectives at multi-team level to learn and improve coordination. Train everyone on writing and using the Team APIs and on the principle that "teams are products" with other teams as customers¹²¹³. This mindset will help sustain the benefits.

### Risk Mitigation Considerations:

- **Knowledge Silos:** One risk is losing knowledge when reforming teams. Mitigate by having transitional pair programming or documentation from old domain experts. Possibly keep an "Architect Advisory" (could be existing senior devs) who float to guide teams on old system quirks initially.

- **Customer Impact:** We must avoid disrupting current users during migration. Use feature flags and beta releases for new components. For example, when rolling out the new dashboard by Insights Team, offer it as "Beta Dashboard" alongside the old one until fully vetted. Similarly, data migrations should be invisible to users or at least scheduled in maintenance windows.

- **Performance/Fragility During Transition:** Splitting services could have performance impacts (e.g., API call overhead). Counteract with thorough testing and perhaps temporarily running some things in parallel to compare. Platform Core Team should do load tests as modules extract. Keep a rollback plan for each major technical change.

- **Alignment Risk:** With autonomy can come divergence. Mitigate by the coordination practices discussed (guilds, shared planning). Also possibly define some guardrails – e.g., all teams must use common logging, common UX style guide, etc., to keep the product unified.

- **Employee Morale:** Change can be hard. Some may resist new roles or fear job security (especially if their current specialty is de-emphasized). Proactively address this with HR support, clarity that no one is losing jobs – instead, jobs are becoming more impactful. Provide training where needed (e.g., if a QA engineer now works embedded in a dev team, train the team on how to do integrated QA). Emphasize career growth: they'll get to broaden skills and see more direct impact on customers.

This migration path is a gradual evolution, not a sudden revolution. By incrementally carving out modules, aligning them to newly formed teams, and using both organizational and technical strategies to reduce risk, Method can transition to the 2026 target state with minimal disruption. We acknowledge it's a journey – possibly 6-12 months to fully transition – but each step will yield improvements (e.g., even in month 3 we might see faster delivery in one area). Throughout, we measure success in things like deployment frequency, cycle time for features, and customer satisfaction per persona (did support tickets drop after we gave Support Reps better tools? etc.). If something's not working, we adapt – the structure is not dogma, but a means to achieve our strategic goals.

## 7. Industry Best Practices & References

The proposed structure and process draw on several industry-proven principles in modern tech organizations:

• **Conway's Law & Architecture Alignment:** As mentioned, Conway's Law states that system design mirrors org communication structure⁵. Rather than fight this, we use it: by structuring teams around key product areas, the software will evolve into well-defined components for those areas⁶. Our approach is consistent with stories from companies who reorganized to align with their desired architecture, breaking monoliths into services owned by small teams. This reduces the "tensions" and communication overhead that arise when architecture and org chart diverge²⁵. In practice, it means if we want a decoupled platform (which we do for faster deployment), we need decoupled teams first.

• **Team Topologies & Stream-Aligned Teams:** The structure essentially creates stream-aligned teams (focused on continuous flow of value in a particular domain) as described by Skelton and Pais (Team Topologies)¹⁰¹¹. Each of our teams (Data, Insights, etc.) is aligned to a flow of work that directly matters to customers. We also introduce a Platform team which is a core concept in Team Topologies – a team dedicated to providing a stable internal platform that stream-aligned teams can use, thereby reducing their cognitive load. This separation of platform vs product teams helps balance innovation and standardization. Our enabling constructs like guilds and chapters echo Team Topologies' ideas for enabling and complicated subsystem teams as well – if a particular aspect gets too complex, we might spin up a specialist team temporarily. We've also adopted the Team API concept from Team Topologies¹⁵, encouraging teams to define how others interact with them – this formalizes inter-team communication and sets expectations (such as service level agreements for support requests, as exemplified in that literature³⁰).

• **Spotify Model (Squads, Tribes, Guilds):** We have heavily leveraged the Spotify Engineering Culture model for our coordination strategy⁷⁸. Our teams are essentially squads – autonomous, cross-functional units with a mission. We anticipate increased autonomy and innovation because, as Spotify's model showed, giving teams control and trusting them leads to more engagement and faster decision-making⁹. We are implementing guilds and chapters to maintain alignment without heavy bureaucracy¹⁹²⁰. It's worth noting that many organizations have tried variants of the Spotify model; key lessons are to adapt it rather than adopt blindly. We'll watch out for guilds becoming too talk-heavy and ensure they produce tangible standards or solutions. But overall, the ethos of "loosely coupled, tightly aligned" from Spotify is what we're after.

• **Amazon's "Two-Pizza Teams" & API-First Approach:** Amazon famously organized into small teams that own services and communicate via APIs. We're mirroring that by making teams small and ownership clear. Jeff Bezos' mandate of "you build it, you run it" and every team exposing service interfaces (even to internal teams) is akin to our Team API approach²²²³. This reduces dependency bottlenecks and fosters a culture of accountability. We cited how platform teams can be run like product teams – that insight from HashiCorp's blog aligns with Amazon's internal platform mindset. Treating internal developers as customers of the platform team ensures the platform evolves in a way that serves engineering needs, which in turn leads to better product development. We'll encourage each team to think of their work as a service – e.g., the Data Team provides "data-as-a-service" to other teams, with defined expectations.

• **DevOps & Autonomy for Speed:** Our plan is also influenced by DevOps research (e.g., the Accelerate book's findings) which shows small batches, high deploy frequency, and team autonomy correlate with high performance. We specifically aim to break the monolithic release cycle into on-demand deployments by each team. One reference point: a case study where a company moved to independent services noted improved deployment frequency and stability. We foresee similar benefits – each team can deploy more often since they don't have to coordinate a global release, and issues will be localized (thus easier to fix and less likely to cascade). We've built in DevOps practices by having Platform Core ensure CI/CD and monitoring from the get-go in the new model.

• **Product Mindset and Customer-Centricity:** A subtle but important shift is running engineering with a product mindset. Not just the platform team as a product team¹²¹³, but each team thinking of the personas they serve as their "product market". For example, the Automation Team's "customers" are users who want to automate tasks; they should seek feedback from those users, iterate on features, and even measure adoption of their features. This aligns with agile and lean principles – build, measure, learn – now applied at a team feature level. It breaks the old model where engineering just implemented requirements from product; instead, each team is partly a mini product team that can drive solutions for their domain. This is very much in line with modern agile organizations where even engineering teams talk to end-users and understand the problem, not just the requirements.

• **Engineering Org Design Examples:** Companies like Spotify, Amazon, Netflix, and HubSpot have all shared their approaches to scaling teams. A common theme is autonomy with alignment (as we've stressed). Another theme is focus on reducing cognitive load per team. By limiting each team's scope, we let them become experts rather than spread thin. HubSpot, for instance, organized teams by persona at one point (small business marketer vs sales rep personas) – a similar philosophy to ensure each team deeply empathizes with a user segment. We opted to organize by responsibilities (like features) rather than strictly by persona, because our analysis (and the Medium blog on fracture planes²²) suggests that aligning by business capability (which multiple personas use) can achieve autonomy while still allowing focus on personas via cross-cutting concerns.

• **Continuous Improvement & Retrospectives:** Borrowing from agile, we will set up periodic retrospectives not just within teams but across the engineering org to reflect on the new structure. This echoes the Lean principle of continuous improvement (Kaizen). Many companies after reorgs do a 6-month check – we should do the same: measure key metrics (deployment frequency, lead time for changes, number of support escalations, etc.) and see if they've improved. If not, we tweak the structure or processes. The goal is not just to implement these best practices, but to create a learning organization that adapts them as we grow (the model that works at 50 devs might need tweaks at 70 devs, and that's okay).

### References

Throughout this report, we've cited sources that back up our approach:
- Skelton & Pais's Team Topologies concepts on team dependencies and APIs¹⁵²².
- Atlassian's summary of the Spotify model highlighting team autonomy and squad structure⁷⁹.
- Agile Alliance insights on how dependencies impact delivery (each dependency halving on-time probability)¹, reinforcing why reducing inter-team dependencies is crucial.
- Medium articles on splitting monoliths with a team-first approach²¹¹ that justify choosing organizational boundaries (fracture planes) that match natural business domains or user roles for easier decoupling.
- A Medium piece contrasting SMB and Enterprise sales cycles and decision-making²⁷, which we used to underline the importance of impressing the SMB owner (the key decision-maker).
- HashiCorp's recommendation to treat platform engineering with a product mindset¹⁶¹⁷, guiding how our Platform Core Team should operate.

By aligning our transformation with these well-regarded practices and learnings from industry, we increase the likelihood of success. Method's leadership can be confident that this proposal isn't unproven theory – it's built on the shoulders of successful transformations at other companies, tailored to Method's unique context. In implementing it, we should remain flexible, keep listening to team feedback, and be ready to adjust while holding true to the core principles of autonomy, responsibility, and customer-focus. This structured yet adaptive approach will drive Method toward its 2026 goals and beyond, yielding an engineering organization that is scalable, innovative, and relentlessly focused on our SMB users.

---

## References

1. Entangled: Solving the Hairy Problem of Team Dependencies | Agile Alliance
   https://agilealliance.org/resources/sessions/entangled-solving-the-hairy-problem-of-team-dependencies/

2. ⁴ ¹⁰ ¹¹ ²⁹ Splitting up a monolith using a teams-first approach | by Zeger Hendrikse | NS-Techblog | Medium
   https://medium.com/ns-techblog/splitting-up-a-monolith-using-a-team-first-approach-5387b51efda0

3. ²⁷ Enterprise Sales vs SMB Sales: A Side-by-Side Comparison | by Rebecca Matias | Medium
   https://medium.com/@callboxrebecca/enterprise-sales-vs-smb-sales-a-side-by-side-comparison-2eab1e383364

5. ⁶ ²⁵ ²⁶ Conway's Law
   https://martinfowler.com/bliki/ConwaysLaw.html

7. ⁸ ⁹ ¹⁸ ¹⁹ ²⁰ ²⁴ | Atlassian
   https://www.atlassian.com/agile/agile-at-scale/spotify

12. ¹³ ¹⁶ ¹⁷ Why you should run your platform team like a product team
   https://www.hashicorp.com/en/blog/why-you-should-run-your-platform-team-like-a-product-team

14. ¹⁵ ²¹ ²² ²³ ³⁰ Visualizing Team Dependencies with a Team API - IT Revolution
   https://itrevolution.com/articles/visualize-team-dependencies-with-a-team-api/

28. Best Manufacturing CRM for QuickBooks — Method
   https://www.method.me/industries/manufacturing-crm-software/