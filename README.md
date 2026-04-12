# Awesome MCP 🚀

> A curated list of awesome Model Context Protocol (MCP) servers, tools, and resources

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Contents

- [What is MCP?](#what-is-mcp)
- [Legend](#legend)
- [Security Model](#security-model)
- [Official Resources](#official-resources)
- [MCP Servers](#mcp-servers)
  - [Free Servers](#free-servers)
  - [Paid/Freemium Servers](#paidfreemium-servers)
  - [Automation](#automation)
  - [OS Control](#os-control)
  - [RAG & Vector Databases](#rag--vector-databases)
  - [Observability & Monitoring](#observability--monitoring)
  - [Real-World Projects](#real-world-projects)
  - [Experimental & Research](#experimental--research)
- [Reference Architectures](#reference-architectures)
- [Templates & Starters](#templates--starters)
- [Clients](#clients)
- [Frameworks & SDKs](#frameworks--sdks)
- [Tutorials & Guides](#tutorials--guides)
- [Community](#community)
- [Contributing](#contributing)

## What is MCP?

The [Model Context Protocol](https://modelcontextprotocol.io) (MCP) is an open standard that enables AI models to securely interact with local and remote resources through standardized server implementations.

**Key Benefits:**
- 🔌 **Universal connector** - One protocol to connect AI to any data source
- 🟢 **Secure by design** - Controlled access to resources
- 🛠️ **Extensible** - Build custom integrations easily
- 🤝 **Interoperable** - Works across different AI platforms

## Quick Start

New to MCP? Start here:

1. **Install a client**: [Claude Desktop](https://claude.ai/download) or [Cursor](https://cursor.sh)
2. **Run a local server**: Try the [Filesystem](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) server
3. **Try a simple task**: Ask the AI to "Summarize files in this folder" or "Read this text file"

👉 **Pro Tip**: Use `npx` to run servers instantly without installation (e.g., `npx -y @modelcontextprotocol/server-filesystem`).

## Use Cases

Find the right tool for your goal:

| Goal | Recommended MCPs |
| :--- | :--- |
| **Coding Agent** | [Git](#developer-tools), [VS Code](#code-analysis--development), [RepoMapper](#code-analysis--development) |
| **Research** | [Fetch](#search--data), [Wikipedia](#knowledge--information), [Brave](#search--data) |
| **Automation** | [Puppeteer](#browser-automation), [n8n](#workflow-automation), [Cron](#task-automation) |
| **Personal AI OS** | [Filesystem](#system-operations), [Shell](#system-operations), [Memory](#knowledge-management) |
| **Data Analysis** | [PostgreSQL](#databases), [Excel](#data-processing), [Open-Meteo](#weather--environment) |

## Legend

Understanding server capabilities and risks:

**Hosting:**
- 🏠 **Local** - Runs on your local machine
- ☁️ **Cloud** - Remote service / API

**Risk Level:**
- 🟢 **Safe** - Read-only, no system modifications
- 🟡 **Moderate** - Write access, can modify data
- 🔴 **High Risk** - Can execute commands or critical OS operations

**Pricing:**
- 🆓 **Free** - No cost, no API key required
- 🔑 **Free (Key)** - Free but requires API key registration
- 💰 **Freemium** - Free tier available with paid upgrades
- 💲 **Paid** - Requires payment

## Security Model

<a id="security-model"></a>

MCP servers follow the **principle of least privilege** and user-controlled access:

**Security Principles:**
- ✅ Explicit capability exposure - Tools are declared upfront
- ✅ User-approved access - Manual approval for sensitive operations
- ✅ Sandboxed execution - Isolated from system when possible
- ✅ Auditable tool calls - All actions are logged and traceable

**🔴 Exercise Caution With:**

Servers that provide:
- **Shell execution** - Can run arbitrary commands
- **Filesystem write access** - Can modify/delete files  
- **Network access** - Can make external requests
- **System control** - Can change OS settings

Always review server code and permissions before use.

## Offline & Regional Usage

For air-gapped or offline environments:
- Prioritize **Local (🏠)** servers (e.g., Filesystem, SQLite).
- Avoid **Cloud (☁️)** servers that require internet access.
- Use local LLMs (e.g., via Ollama) combined with local MCP servers for a fully offline stack.

## Official Resources

- [MCP Documentation](https://modelcontextprotocol.io) - Official documentation
- [MCP Specification](https://spec.modelcontextprotocol.io) - Technical specification
- [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - Official TypeScript SDK
- [Python SDK](https://github.com/modelcontextprotocol/python-sdk) - Official Python SDK
- [Official Servers](https://github.com/modelcontextprotocol/servers) - Reference implementations

## MCP Servers

<a id="mcp-servers"></a>

### Free Servers

<a id="free-servers"></a>

Servers that are **free to use**, with no API keys or optional free registration.

#### 📚 Knowledge & Information

- [Wikipedia](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) 🆓 🏠 - Search and access Wikipedia articles
- [Context Awesome](https://github.com/bh-rat/context-awesome) 🆓 ☁️ - Query 8,500+ curated awesome lists  
- [REST Countries](https://restcountries.com) 🆓 ☁️ 🟢 - Comprehensive country data

#### ☁️ Weather & Environment

- [Open-Meteo Weather](https://open-meteo.com) 🆓 ☁️ 🟢 - Global weather data and forecasts
- Weather.gov 🆓 ☁️ 🟢 - US weather data

#### 🛠️ Tooling & Ecosystem

- [MCP Inspector](https://github.com/modelcontextprotocol/inspector) 🆓 🏠 - Official debugger for testing MCP servers
- [Smithery](https://smithery.ai) 🆓 ☁️ - Discovery and installation registry for MCP servers
- [Glama](https://glama.ai/mcp) 🆓 ☁️ - AI workspace with integrated MCP directory
- [toprank](https://github.com/nowork-studio/toprank) 🆓 🏠 🟡 - Open-source Claude Code plugin providing SEO & Google Ads skills. Connects Google Search Console, PageSpeed Insights, and Google Ads API.


####💻 Developer Tools

- [Git](https://github.com/modelcontextprotocol/servers/tree/main/src/git) 🆓 🏠 🟡 - Git repository operations
- [GitHub](https://github.com/github/github-mcp-server) 🔑 ☁️ - GitHub repository integration

#### 🔍 Search & Data

- [Fetch](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch) 🆓 ☁️ 🟢 - Web content fetching
- [Brave Search](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) 🔑 ☁️ 🟢 - Web search
- [Google Search](https://github.com/mixelpixx/Google-Search-MCP-Server) 🆓 ☁️ 🟢 - Google search results

#### 🧠 AI & Productivity

- [Sequential Thinking](https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking) 🆓 🏠 - Problem-solving through thought sequences

---

### Paid/Freemium Servers

<a id="paidfreemium-servers"></a>

Servers with free tiers or that require paid API access.

#### ☁️ Cloud Platforms

- **AWS**
  - [AWS Bedrock KB](https://github.com/awslabs/mcp/tree/main/src/bedrock-kb-retrieval-mcp-server) 💰 ☁️ - Amazon Bedrock Knowledge Bases
  - [AWS CDK](https://github.com/awslabs/mcp/tree/main/src/cdk-mcp-server) 💰 ☁️ - AWS Cloud Development Kit
  - [AWS Documentation](https://github.com/awslabs/mcp/tree/main/src/aws-documentation-mcp-server) 💰 ☁️ 🟢 - AWS docs access
  
- **Azure**
  - [Azure DevOps](https://github.com/microsoft/azure-devops-mcp) 💰 ☁️ - Azure DevOps integration
  
- **Google Cloud**
  - [Google Drive](https://github.com/modelcontextprotocol/servers/tree/main/src/gdrive) 💰 ☁️ 🟡 - Google Drive access
  - [Google Maps](https://github.com/anthropic/anthropic-quickstarts/tree/main/computer-use-demo/server) 💰 ☁️ 🟢 - Maps and location services

#### 🗄️ Databases

- [BigQuery](https://github.com/LucasHild/mcp-server-bigquery) 💰 ☁️ 🟢 - Google BigQuery access
- [MongoDB](https://github.com/mongodb/mcp-server-mongodb) 💰 ☁️ 🟡 - MongoDB database access
- [PostgreSQL](https://github.com/modelcontextprotocol/servers/tree/main/src/postgres) 🆓 🏠 🟡 - PostgreSQL database access
- [SQLite](https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite) 🆓 🏠 🟡 - SQLite database access  
- [Supabase](https://github.com/supabase/mcp-server-supabase) 💰 ☁️ 🟡 - Supabase platform integration

#### 💬 Communication & Collaboration

- [Basecamp](https://github.com/georgeantonopoulos/Basecamp-MCP-Server) 💰 ☁️ - Basecamp project management
- [Discord](https://github.com/discord/discord-mcp) 💰 ☁️ 🟡 - Discord server management
- [Gmail](https://github.com/google/gmail-mcp) 💰 ☁️ 🟡 - Gmail email access
- [Slack](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) 💰 ☁️ 🟡 - Slack workspace integration

#### 💰 Finance & Business

- [Stripe](https://stripe.com/mcp) 💲 ☁️ - Stripe payments API
- [Chargebee](https://github.com/chargebee/agentkit/tree/main/modelcontextprotocol) 💲 ☁️ - Subscription management
- [PayPal](https://github.com/paypal/paypal-mcp) 💲 ☁️ - PayPal integration
- [Alpha Vantage](https://mcp.alphavantage.co/) 💰 ☁️ 🟢 - Financial market data

#### 🔍 Search & Analytics

- [Exa](https://github.com/exa-labs/exa-mcp-server) 💰 ☁️ 🟢 - AI-powered search
- [Perplexity](https://www.perplexity.ai/mcp) 💰 ☁️ 🟢 - AI search and answers
- [Fathom Analytics](https://github.com/mackenly/mcp-fathom-analytics) 💰 ☁️ 🟢 - Privacy-focused analytics

#### 🎨 Creative & Media

- [Spotify](https://github.com/spotify/spotify-mcp) 💰 ☁️ - Spotify music streaming
- [YouTube](https://github.com/youtube/youtube-mcp) 💰 ☁️ - YouTube video platform
- [DALL-E](https://github.com/openai/dall-e-mcp) 💲 ☁️ - AI image generation
- [Midjourney](https://midjourney.com/mcp) 💲 ☁️ - AI image generation

#### 📊 Data & Analytics

- [Snowflake](https://github.com/snowflakedb/snowflake-mcp) 💲 ☁️ - Cloud data platform
- [dbt](https://github.com/dbt-labs/dbt-core/tree/main/mcp) 💰 🏠/☁️ - Data transformation
- [Tableau](https://github.com/tableau/tableau-mcp) 💲 ☁️ - Data visualization
- [Amplitude](https://amplitude.com/mcp) 💲 ☁️ - Product analytics

#### 🛠️ Development Tools

- [Linear](https://github.com/linear/linear-mcp) 💰 ☁️ - Issue tracking
- [Docker](https://github.com/docker/docker-mcp) 🆓 🏠 🔴 - Container management

#### 🌐 Web Services

- [Airtable](https://github.com/Airtable/airtable-mcp) 💰 ☁️ 🟡 - Cloud database platform

#### 🟢 Security

- [1Password](https://github.com/1Password/1password-mcp) 💲 🏠 🟢 - Password management
- [Okta](https://github.com/okta/okta-mcp) 💲 ☁️ - Identity management
- [Auth0](https://github.com/auth0/auth0-mcp) 💲 ☁️ - Authentication platform

---

## Automation

<a id="automation"></a>

Servers that enable workflow automation, browser automation, and task orchestration.

### Browser Automation

- [Playwright](https://github.com/microsoft/playwright-mcp) 🆓 🏠 🔴 - Official Microsoft Playwright MCP server for web automation
- [Browserbase](https://github.com/browserbase/mcp-server-browserbase) 💰 ☁️ 🔴 - Cloud browser automation with headless Chrome
- [Puppeteer](https://github.com/modelcontextprotocol/servers-archived/tree/main/src/puppeteer) 🆓 🏠 🔴 - Browser automation for web scraping
- [Browser-Use](https://github.com/co-browser/browser-use-mcp-server) 🆓 🏠 🔴 - Browser automation in Docker with VNC

### Workflow Automation

- [n8n](https://n8n.io/integrations/mcp/) 💰 🏠/☁️ - Workflow automation platform
- [Zapier](https://zapier.com/mcp) 💰 ☁️ - Connect 5000+ apps and automate workflows
- [Make.com](https://make.com) 💰 ☁️ - Visual automation platform
- [Apple Shortcuts](https://github.com/recursechat/mcp-server-apple-shortcuts) 🆓 🏠 - macOS automation integration

### Task Automation



- [Cron](https://github.com/cron-mcp/cron-server) 🆓 🏠 🔴 - Scheduled task execution
- [Home Assistant](https://github.com/allenporter/mcp-server-home-assistant) 🆓 🏠 🟡 - Control smart home devices
- [IFTTT](https://ifttt.com/mcp) 💰 ☁️ - If-This-Then-That automation

---

## OS Control

<a id="os-control"></a>

Servers that provide system-level control and OS integration capabilities.

### System Operations

- [Filesystem](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) 🆓 🏠 🟡 🔴 - Secure file operations with access controls
- [Shell](https://github.com/executeautomation/shell-mcp) 🆓 🏠 🔴 - Execute shell commands securely
- [Windows PowerShell](https://github.com/microsoft/powershell-mcp) 🆓 🏠 🔴 - Windows system control
- [macOS AppleScript](https://github.com/apple/applescript-mcp) 🆓 🏠 🔴 - macOS automation and control

### Desktop Integration

- [Apple Reminders](https://github.com/FradSer/mcp-server-apple-reminders) 🆓 🏠 🟡 - Interact with Apple Reminders on macOS
- [System Monitor](https://github.com/seekrays/mcp-monitor) 🆓 🏠 🟢 - CPU, memory, disk, network monitoring

---

## RAG & Vector Databases

<a id="rag--vector-databases"></a>

Servers for Retrieval-Augmented Generation and vector database integration.

### Vector Databases

- [Pinecone](https://github.com/pinecone-io/pinecone-mcp) 💰 ☁️ 🟡 - Managed vector database
- [Weaviate](https://github.com/weaviate/weaviate-mcp) 🆓 🏠/☁️ 🟡 - Open-source vector search engine
- [Qdrant](https://github.com/qdrant/qdrant-mcp) 🆓 🏠 🟡 - Vector similarity search engine
- [Milvus](https://github.com/milvus-io/milvus-mcp) 🆓 ☁️ 🟡 - Cloud-native vector database
- [Chroma](https://github.com/chroma-core/chroma-mcp) 🆓 🏠 🟡 - AI-native open-source embedding database

### RAG Platforms

- [LlamaIndex](https://github.com/run-llama/llamaindex-mcp) 🆓 🏠 - Data framework for LLM applications
- [LangChain](https://github.com/langchain-ai/langchain-mcp) 🆓 🏠 - Build LLM applications
- [Haystack](https://github.com/deepset-ai/haystack-mcp) 🆓 🏠 - End-to-end NLP framework

### Knowledge Management

- [Memory](https://github.com/modelcontextprotocol/servers/tree/main/src/memory) 🆓 🏠 🟡 - Knowledge graph-based persistent memory
- [Obsidian](https://github.com/obsidian/obsidian-mcp) 💰 🏠 🟡 - Personal knowledge base
- [Notion](https://github.com/notion/notion-mcp) 💰 ☁️ 🟡 - Connected workspace

### Embedding Services

- [OpenAI Embeddings](https://github.com/openai/embeddings-mcp) 💲 ☁️ - Text embedding API
- [Cohere Embeddings](https://github.com/cohere/embed-mcp) 💰 ☁️ - Multilingual embeddings

---

## Observability & Monitoring

<a id="observability--monitoring"></a>

Servers for application monitoring, logging, tracing, and performance analysis.

### Application Performance Monitoring (APM)

- [Datadog](https://github.com/datadog/datadog-mcp) 💰 ☁️ - Full-stack observability platform
- [New Relic](https://github.com/newrelic/newrelic-mcp) 💰 ☁️ - Performance monitoring
- [Dynatrace](https://github.com/dynatrace/dynatrace-mcp) 💲 ☁️ - Software intelligence platform

### Logging & Log Analytics

- [Grafana Loki](https://github.com/tumf/grafana-loki-mcp) 🆓 🏠/☁️ 🟢 - Log aggregation system
- [Elasticsearch](https://github.com/elastic/mcp-server-elasticsearch) 💰 ☁️ - Search and analytics engine
- [Logfire](https://github.com/pydantic/logfire-mcp) 💰 ☁️ - OpenTelemetry traces and metrics

### Metrics & Monitoring

- [Prometheus](https://github.com/yshngg/pmcp) 🆓 🏠 🟢 - Monitoring system and time series database
- [Grafana](https://github.com/grafana/mcp-grafana) 🆓 🏠/☁️ - Observability and data visualization
- [VictoriaMetrics](https://github.com/VictoriaMetrics-Community/mcp-victoriametrics) 🆓 🏠 - Time series database
- [Netdata](https://github.com/netdata/netdata) 🆓 🏠 🟢 - Real-time performance monitoring

### Error Tracking

- [Sentry](https://github.com/getsentry/sentry-mcp) 💰 ☁️ - Error tracking and performance monitoring
- [Rollbar](https://github.com/rollbar/rollbar-mcp) 💰 ☁️ - Error monitoring
- [Bugsnag](https://github.com/bugsnag/bugsnag-mcp) 💰 ☁️ - Error monitoring and reporting

### Distributed Tracing

- [Jaeger](https://github.com/jaegertracing/jaeger-mcp) 🆓 🏠/☁️ - End-to-end distributed tracing
- [Zipkin](https://github.com/zipkin/zipkin-mcp) 🆓 🏠/☁️ - Distributed tracing system
- [OpenTelemetry](https://github.com/open-telemetry/opentelemetry-mcp) 🆓 🏠 - Observability framework

### Infrastructure Monitoring

- [Zabbix](https://github.com/mpeirone/zabbix-mcp-server) 🆓 🏠/☁️ - Enterprise monitoring solution
- [Kubernetes](https://github.com/metoro-io/metoro-mcp-server) 💰 ☁️ - Container orchestration monitoring

---

## Real-World Projects

<a id="real-world-projects"></a>

Production-ready MCP servers and reference implementations from real-world use cases.

### Code Analysis & Development

- [CodeGraph Context](https://github.com/Shashankss1205/CodeGraphContext) 🆓 🏠 - Index code into graph database for AI context
- [VS Code MCP](https://github.com/juehang/vscode-mcp-server) 🆓 🏠 - Read directory structure, lint problems, edit files
- [RepoMapper](https://github.com/pdavis68/RepoMapper) 🆓 🏠 🟢 - Dynamic repository mapping for AI
- [Code Assistant](https://github.com/stippi/code-assistant) 🆓 🏠 🔴 - Multi-project coding agent

### Data Processing

- [Data Exploration](https://github.com/reading-plus-ai/mcp-server-data-exploration) 🆓 🏠 - Autonomous CSV data analysis
- [Excel MCP](https://github.com/haris-musa/excel-mcp-server) 🆓 🏠 🟡 - Excel manipulation and analysis
- [dbt Docs](https://github.com/mattijsdp/dbt-docs-mcp) 🆓 🏠 🟢 - dbt project metadata and lineage

### Content & Media

- [YouTube Transcript](https://github.com/kimtaeyoon83/mcp-server-youtube-transcript) 🆓 ☁️ 🟢 - Fetch YouTube subtitles for AI
- [Podcast Search](https://www.audioscrape.com/docs/mcp) 💰 ☁️ 🟢 - Search 1M+ hours of podcasts

### Security & DevOps

- [Inspektor Gadget](https://github.com/inspektor-gadget/ig-mcp-server) 🆓 🏠 🔴 - Container debugging with eBPF
- [BloodHound MCP](https://github.com/MorDavid/BloodHound-MCP-AI) 🆓 🏠 - Active Directory attack path analysis

### Multi-Agent Systems

- [Agent MCP](https://github.com/rinadelph/Agent-MCP) 🆓 🏠 - Framework for multi-agent coordination
- [Roundtable](https://github.com/askbudi/roundtable) 🆓 🏠 - Unify multiple AI coding assistants
- [Owlex](https://github.com/agentic-mcp-tools/owlex) 🆓 🏠 - Query multiple CLI agents in parallel

---

## Experimental & Research

<a id="experimental--research"></a>

Early-stage or experimental servers not yet production-ready.

**Note:** These servers are actively developed but may have incomplete features, breaking changes, or stability issues. Use with caution in production environments.

- Submit your experimental MCP server via PR!

---

## Agent Patterns

<a id="agent-patterns"></a>

Strategic patterns for building reliable agents:

- **Planner-Executor**: One agent creates a plan, another executes steps (uses [Sequential Thinking](#ai--productivity)).
- **Tool-Only**: Simple agent that just calls tools (e.g., "Get weather").
- **Memory-Backed**: Agent that persists state across sessions using [Memory](#knowledge-management) or [PostgreSQL](#databases).
- **Multi-Agent Swarm**: Specialized agents collaborating (e.g., Research Agent + Writer Agent + Editor Agent).

### Evaluation & Benchmarks

When choosing servers, consider:
- **Latency**: Local (🏠) is faster than Cloud (☁️).
- **Capability**: Does it support all operations you need?
- **Risk**: Check the risk level (🟢/🟡/🔴).
- **Cost**: 🆓 vs 💰.

## Reference Architectures

<a id="reference-architectures"></a>

Common patterns for combining MCP servers into powerful AI systems.

### 🖥️ Local AI OS
**Components:** Claude Desktop + Filesystem + Shell + Browser Automation  
**Use Case:** Complete local system control and automation

### 🧠 RAG System  
**Components:** Vector DB (Chroma/Qdrant) + Memory MCP + Document Loaders  
**Use Case:** Intelligent document Q&A and knowledge retrieval

### 👨‍💻 Coding Agent
**Components:** Git + RepoMapper + VS Code MCP + GitHub  
**Use Case:** Autonomous code analysis, refactoring, and PR management

### 🏠 Home Automation Agent
**Components:** Home Assistant + Cron + Slack + OpenAI  
**Use Case:** Smart home control, energy monitoring, and family notifications

### 🤖 Automation Agent
**Components:** Browser Automation + n8n + Cron + Slack  
**Use Case:** End-to-end workflow automation and notifications

### 🏢 Enterprise Agent
**Components:** Observability Stack + IAM + Cloud MCPs + Databases  
**Use Case:** Production monitoring, access control, and data integration

### 🔬 Research Agent
**Components:** ArXiv + Semantic Scholar + RAG + Memory  
**Use Case:** Academic research, literature review, and citation management

---

## Templates & Starters

<a id="templates--starters"></a>

Reusable templates and starter projects for building MCP servers.

- [TypeScript MCP Template](https://github.com/modelcontextprotocol/typescript-sdk/tree/main/examples) - Official TypeScript starter
- [Python MCP Template](https://github.com/modelcontextprotocol/python-sdk/tree/main/examples) - Official Python starter
- [Dockerized MCP Example](https://github.com/docker/mcp-example) - Container-based MCP deployment

**Contributing:** Have a useful template? Submit a PR!

---

## Clients

Applications and tools that support MCP:

- [Claude Desktop](https://claude.ai/download) - Anthropic's desktop AI assistant
- [Cline](https://github.com/cline/cline) - VS Code AI coding assistant  
- [Zed](https://zed.dev) - Collaborative code editor with AI
- [Cursor](https://cursor.sh) - AI-powered code editor
- [Continue](https://continue.dev) - Open-source AI code assistant

## Frameworks & SDKs

Build your own MCP servers:

- [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk) - Official TypeScript implementation
- [Python SDK](https://github.com/modelcontextprotocol/python-sdk) - Official Python implementation
- [FastMCP](https://github.com/jlowin/fastmcp) - Fast MCP server framework (Python)
- [.NET SDK](https://github.com/microsoft/mcp-dotnet) - .NET implementation

## Tutorials & Guides

- [Building Your First MCP Server](https://modelcontextprotocol.io/quickstart) - Official quickstart guide
- [MCP Server Examples](https://github.com/modelcontextprotocol/servers) - Reference implementations
- [MCP Best Practices](https://modelcontextprotocol.io/docs/best-practices) - Development guidelines
- [MCP Security Guide](https://modelcontextprotocol.io/docs/security) - Security considerations

## Community

- [Discord](https://discord.gg/mcp) - Official MCP Discord community
- [GitHub Discussions](https://github.com/modelcontextprotocol/discussions) - Technical discussions
- [Reddit](https://reddit.com/r/modelcontextprotocol) - Community discussions
- [Twitter](https://twitter.com/mcprotocol) - Updates and announcements

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

Looking for where to start? Check issues labeled "good first issue" in the server repositories!

### How to Submit

1. Fork this repository
2. Add your MCP server to the appropriate category
3. Follow the format: `- [Name](link) 🆓/💰 🏠/☁️ - Brief description`
4. Ensure it's alphabetically ordered within the category
5. Include appropriate legend icons
6. Submit a Pull Request

### Submission Criteria

- ✅ Must be a working MCP server
- ✅ Must have clear documentation
- ✅ Must be actively maintained (🟢 or 🟡)
- ✅ Must specify pricing model
- ✅ Must follow MCP specification
- ✅ Must include legend tags

### Maintenance Status

When submitting, please indicate:
- 🟢 **Active** - Updated in last 3 months
- 🟡 **Maintained** - Updated in last year  
- 🔴 **Archived** - No longer maintained

We periodically review and may move stale servers to an archived section.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related rights to this work.

---

**Made with ❤️ for the MCP community**

Find more awesome lists at [awesome.re](https://awesome.re)
