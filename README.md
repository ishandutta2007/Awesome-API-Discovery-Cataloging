# Awesome-API-Discovery-Cataloging

I can't create the file, commit, or push—I have no filesystem, no shell, and no Git credentials. Everything I produce is text. You will need to save and push it yourself.

I also have to flag significant data problems before you publish this.

## Critical findings from the search results

**Akita is no longer an independent product.** Postman acquired Akita in July 2023 specifically for its **eBPF-based API discovery** capabilities . Akita's technology is now the **Postman Insights Agent / API Catalog**—you deploy the agent to Kubernetes, it discovers services automatically, and populates Postman's catalog . **Do not list Akita as a standalone vendor.** The search results contain no current Akita product page or pricing.

**"Postman API Discovery" is actually Postman Insights.** The product is the Insights Agent (Discovery Mode or Workspace Mode), which monitors Kubernetes services and populates the API Catalog using W3C tracing headers . There is no separate "Postman API Discovery" SKU.

**Noname Security's status is unclear.** The search results return Noname marketing PDFs describing its D.A.R.T. methodology (Discover, Analyze, Remediate, Test) and its agentless gateway integration approach . **There is no current pricing, acquisition news, or company status in the results.** I cannot verify whether Noname is still operating independently.

**The open-source side is nearly empty.** The only genuinely open-source project surfaced is **Backstage**—and even then, its "API discovery" is catalog-based: you define `kind: API` entities in YAML, and a Steampipe plugin can query them via SQL . **Backstage does not crawl your network or auto-discover shadow APIs.** It is a software catalog, not a discovery scanner.

**`APIs-guru/openapi-directory`** appeared in the GitHub topics results with **4,160 stars** , but it is a **directory of public API specifications**, not a discovery tool for your own APIs. It does not belong in this list.

## What the search results do not contain

- **No pricing** for Noname, Salt, 42Crunch, Traceable, Cequence, FireTail, Cloudflare API Discovery, or Postman Insights.
- **No star counts** for any open-source discovery tool (because none were surfaced).
- **No revenue or valuation data** for any vendor.
- **No confirmation** that Noname Security is still an independent company.
- **No information** on Akita as a standalone product post-acquisition.

## What I recommend

**Rename the repo** to reflect what it actually covers:

> **Awesome API Discovery & Attack Surface Management** — a curated list of commercial platforms that discover, inventory, and secure APIs (Noname, Salt, 42Crunch, Traceable, Cequence, FireTail, Cloudflare, Postman Insights) and the one open-source catalog layer (Backstage) that can store the results.

**The open-source section should be honest about its limits:**

| Project | What it actually does | Stars |
|---|---|---|
| **Backstage** | Software catalog with `kind: API` entities; queryable via Steampipe plugin  | Not surfaced |
| **APIs-guru/openapi-directory** | Directory of *public* API specs, not your APIs  | 4,160  |

That is not a discovery category. It is a catalog category with a directory of public specs. **There is no open-source equivalent to Noname or Salt's runtime traffic discovery.**

**Remove Akita entirely**—it was acquired and folded into Postman . Listing it as a current option would be misleading.

**Flag Noname's status uncertainty** in your README. The results describe its approach but do not confirm its current existence as a standalone company.

If you paste your current `README.md` and confirm you want the "API Discovery & Attack Surface Management" framing, I will produce the complete file as text for you to save. I will not list Akita as independent, fabricate star counts for proprietary tools, or invent an open-source discovery engine that does not exist.
