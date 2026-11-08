# Awesome API Discovery & Cataloging [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of awesome tools, platforms, specifications, and frameworks for automated API discovery, shadow/zombie API detection, software cataloging, and API attack surface management.

---

## Sector Overview & Market Dynamics

The global API Security and Discovery market is estimated between **$1.2B and $10B** (projected to reach over $14B by 2032 with a robust ~25–30% CAGR). The sector is currently **moderately fragmented** among specialized runtime pure-plays, application security vendors, and developer tooling providers, but is experiencing rapid **consolidation and concentration pressures** as cloud infrastructure giants (such as Akamai acquiring Noname Security, Cloudflare bundling API Shield, and Postman absorbing Akita) build unified, end-to-end API lifecycle and protection platforms.

---

## SaaS Platforms

Commercial and hosted SaaS solutions providing automated continuous API discovery, eBPF/proxy-based shadow API inventorying, security posture management, and centralized catalogs. Sorted in descending order by company scale (market cap / valuation / revenue).

| Vendor / Product | Company Scale (Valuation / Revenue) | Starting Tier Pricing | Free Tier / Trial Limits | Key Discovery & Catalog Capabilities |
| :--- | :--- | :--- | :--- | :--- |
| **[Cloudflare API Shield](https://www.cloudflare.com/application-services/products/api-shield/)** | **$33.15B Market Cap** ($1.67B FY2024 Revenue) | **$25/month** (Pro plan base; automated ML discovery requires Enterprise custom quote) | **Free Plan**: Free forever with up to 10 mTLS client certs & basic rate limiting (Automated ML discovery requires Enterprise evaluation sandbox upon request) | Machine-learning-driven endpoint discovery from Cloudflare edge traffic, schema validation, and sequence mitigation. |
| **[Postman API Catalog & Insights](https://www.postman.com/api-catalog/)** | **$5.6B Valuation** (~$313M ARR) | **$19/user/month** (Team, billed annually; Enterprise at $49/user/month for Insights Agent) | **Free Forever**: 1 user, up to 3 public API definitions, and 50 AI credits; 14-day Enterprise trial available upon request | Deploys eBPF-based Insights Agent into Kubernetes/cloud environments to automatically discover live endpoints and populate Postman API Catalog. |
| **[Salt Security](https://salt.security/)** | **$1.4B Valuation** (~$75M ARR) | **$20,000/year** (Starting baseline AWS Marketplace 12-month tier; enterprise packages scale to $100k/yr) | **No self-serve free plan**; 14-day guided proof-of-concept (PoC) / sandbox evaluation available via sales | Patented big data architecture analyzes continuous API traffic across gateways and cloud providers to automatically inventory all internal and shadow endpoints. |
| **[Traceable AI](https://www.traceable.ai/)** | **$450M+ Valuation** (~$25M–$31M ARR) | **$20,000/year** (AWS Marketplace Discovery tier covering up to 250 API endpoints) | **No self-serve free plan**; 30-day technical proof-of-concept (PoC) and evaluation sandbox available upon sales request | Continuous automated API discovery, sensitive data flow tracking, and behavioral risk profiling using distributed tracing and eBPF sensors. |
| **[Akamai API Security (formerly Noname)](https://www.akamai.com/products/api-security)** | **$450M Acquisition Price** ($452.3M cash deal by Akamai in 2024) | **Custom Enterprise contract** (Annual contract starting at ~$30,000 via AWS Marketplace private offers) | **No self-serve free plan**; 14-to-30-day enterprise evaluation and dark-traffic assessment available via sales request | Integrates agentless network sniffers, cloud mirrors, and API gateways to catalog shadow APIs, legacy endpoints, and anomalous data access. |
| **[Cequence Security](https://www.cequence.ai/)** | **$250M–$500M Est. Valuation** (~$30M–$40M ARR) | **$52,500/year** (AWS Marketplace entry baseline unified security platform annual tier) | **No self-serve free plan**; 14-to-30-day custom Proof-of-Value (PoV) sandbox coordinated via sales engineering | API Spartan & API Sentinel for automated discovery of all managed and unmanaged external APIs, sensitive payload tracking, and bot mitigation. |
| **[42Crunch](https://42crunch.com/)** | **~$25M Funding** (~$5M+ ARR) | **$9/month** (Developer Individual plan; Pro at $20/month) | **Free Forever**: 100 API security audit scans per month via IDE plugins (VS Code, JetBrains) and up to 25 CI/CD scans/month across 3 repositories | Shift-left API discovery and security audit platform that parses OpenAPI definitions in IDEs and CI/CD pipelines to build a unified posture catalog. |
| **[FireTail](https://www.firetail.ai/)** | **~$5M Funding** (~$2M ARR) | **$0/month** (Free Developer tier; Enterprise starting at $6,000/year) | **Free Forever**: Covers up to 5 APIs, 1,000,000 API call logs per month, and 7-day data retention | Hybrid runtime and code-level API security providing inline inspection, continuous automated discovery, and central logging. |
| **[Levo.ai](https://www.levo.ai/)** | **~$4M Funding** (~$3M ARR) | **Custom Per-Endpoint tier** (Custom pricing structured per endpoint rather than request volume) | **14-day Free Trial**: Full access to eBPF auto-discovery sensor and OpenAPI specification generator upon registration | Auto-discovers internal and external APIs via passive eBPF sensors, auto-generating real-time OpenAPI schemas without requiring code changes. |

---

## Open-Source Tools & Frameworks

Open-source frameworks, software catalogs, traffic analyzers, and registries for discovering, introspecting, and inventorying APIs. Sorted in descending order by GitHub stargazers count.

| Project & Stars Badge | Description | Primary Discovery / Catalog Mechanism |
| :--- | :--- | :--- |
| **[mitmproxy](https://github.com/mitmproxy/mitmproxy)** [![GitHub stars](https://img.shields.io/github/stars/mitmproxy/mitmproxy?style=social&color=white)](https://github.com/mitmproxy/mitmproxy/stargazers) | Interactive, SSL/TLS-capable intercepting HTTP proxy for penetration testers and developers. | Intercepts live network traffic to inspect payloads, reverse-engineer undocumented endpoints, and export HTTP flows into OpenAPI definitions. |
| **[Backstage](https://github.com/backstage/backstage)** [![GitHub stars](https://img.shields.io/github/stars/backstage/backstage?style=social&color=white)](https://github.com/backstage/backstage/stargazers) | Spotify's open-source framework for building internal developer portals (IDPs). | Software Catalog core that tracks `kind: API` entities, OpenAPI/AsyncAPI/GraphQL specifications, ownership, and service dependency graphs. |
| **[Swagger UI](https://github.com/swagger-api/swagger-ui)** [![GitHub stars](https://img.shields.io/github/stars/swagger-api/swagger-ui?style=social&color=white)](https://github.com/swagger-api/swagger-ui/stargazers) | Visual documentation and exploration collection for OpenAPI specifications. | Serves as an interactive catalog viewer and discovery UI for exposed OpenAPI 2.0/3.x specifications across distributed microservices. |
| **[Katana](https://github.com/projectdiscovery/katana)** [![GitHub stars](https://img.shields.io/github/stars/projectdiscovery/katana?style=social&color=white)](https://github.com/projectdiscovery/katana/stargazers) | Next-generation crawling and spidering framework by ProjectDiscovery. | Discovers unmapped and hidden API endpoints, query routes, and endpoints through automated headless crawling and JavaScript parsing. |
| **[Prism](https://github.com/stoplightio/prism)** [![GitHub stars](https://img.shields.io/github/stars/stoplightio/prism?style=social&color=white)](https://github.com/stoplightio/prism/stargazers) | Open-source HTTP mock and proxy server powered by OpenAPI v2/v3 documents. | Validates live traffic against API schemas, logging contract drifts, missing endpoints, and shadow parameters. |
| **[APIs-guru OpenAPI Directory](https://github.com/APIs-guru/openapi-directory)** [![GitHub stars](https://img.shields.io/github/stars/APIs-guru/openapi-directory)](https://github.com/APIs-guru/openapi-directory/stargazers) | The "Wikipedia for Web APIs" containing machine-readable specifications. | Massive catalog of thousands of public REST API definitions formatted in OpenAPI 2.0/3.x, serving as a global benchmark and discovery directory. |
| **[kin-openapi](https://github.com/getkin/kin-openapi)** [![GitHub stars](https://img.shields.io/github/stars/getkin/kin-openapi?style=social&color=white)](https://github.com/getkin/kin-openapi/stargazers) | OpenAPI 3.0 (and 3.1) implementation for Go (router, validator, parser). | Programmatically inspects, merges, and validates OpenAPI specs from Go services to power custom cataloging systems and discovery pipelines. |
| **[Akto](https://github.com/akto-api-security/akto)** [![GitHub stars](https://img.shields.io/github/stars/akto-api-security/akto?style=social&color=white)](https://github.com/akto-api-security/akto/stargazers) | Open-source API security platform that discovers APIs and tests for business logic vulnerabilities. | Integrates with AWS, GCP, Cloudflare, Kubernetes DaemonSets, and traffic mirrors to continuously discover and catalog shadow endpoints and sensitive data. |
| **[Optic](https://github.com/opticdev/optic)** [![GitHub stars](https://img.shields.io/github/stars/opticdev/optic?style=social&color=white)](https://github.com/opticdev/optic/stargazers) | Git-native API documentation, automated changelog generation, and schema diffing tool. | Observes API traffic in test/dev environments to generate OpenAPI schemas automatically, catch breaking changes, and track version history. |

---

## Contributing

Contributions are welcome! Please check out [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on suggesting new tools, repositories, or commercial platforms.
