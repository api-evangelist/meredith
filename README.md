# meredith

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

API Evangelist Network profile for **People Inc** (formerly **Dotdash Meredith**) — America's largest digital and print publisher and an IAC operating company.

- **Corporate site:** https://www.people.inc/
- **Parent:** IAC (NASDAQ: IAC) — https://www.iac.com/brands/peopleinc
- **Formed:** December 1, 2021 (Dotdash + Meredith Corporation, $2.7B transaction)
- **Rebranded:** July 31, 2025 (Dotdash Meredith → People Inc)
- **Scale (per IAC):** "More than 175 million people trust us each month to help them find inspiration, make decisions, and take action."
- **Brand count:** 40+ brands across Health, Finance, Food & Drink, Home, Beauty & Style, Travel, Tech & Sustainability, Entertainment, Premium Publishing.

## What this repo profiles

People Inc does not publish a public read/write developer API. The machine-readable surface that exists is:

| Surface | Endpoint pattern | Notes |
|---|---|---|
| RSS 2.0 feeds | `https://{brand}/feed` | Available on every consumer brand. The de-facto content API. |
| XML Sitemaps | `https://{brand}/sitemap.xml` | Sitemap index + per-section files; updated daily. |
| robots.txt policy | `https://{brand}/robots.txt` | Identical AI-bot policy template across brands. |
| D/Cipher (B2B) | https://www.people.inc/dcipher | Cookieless intent-based contextual ad platform; sold via direct sales, no public API. |

## Artifacts in this repo

- [`apis.yml`](apis.yml) — full inventory of brand RSS surfaces + corporate properties
- [`json-schema/`](json-schema/) — RSS feed, sitemap, and robots-policy schemas
- [`json-structure/`](json-structure/) — People Inc brand entity structure
- [`json-ld/`](json-ld/) — Linked-data context aligning People Inc concepts with schema.org
- [`examples/`](examples/) — Example payloads (RSS feed, sitemap index, robots policy)
- [`vocabulary/`](vocabulary/) — Domain vocabulary covering the publisher, brands, products
- [`capabilities/`](capabilities/) — Naftiko-style capability definitions (shared + workflows)
- [`rules/`](rules/) — Spectral rules for the RSS schema artifacts
- [`plans/`](plans/) — Commercial surfaces (advertising, licensing, subscriptions)
- [`rate-limits/`](rate-limits/) — Edge rate-shaping + the codified AI-bot policy
- [`finops/`](finops/) — FinOps view of People Inc as a vendor

## AI bot policy (important)

Every People Inc brand domain ships an identical `robots.txt` template that **fully disallows** `ClaudeBot`, `Claude-Web`, `anthropic-ai`, `CCBot`, `news-please`, `cohere-ai`, `ImagesiftBot`, `FriendlyCrawler`, `Quora-Bot`, `omgilibot`, `omgili`, and `PerplexityBot`, and **partially restricts** `ChatGPT-User`, `OAI-SearchBot`, and `GPTBot` (blocking the `/thmb/` image-transform subtree). `Pinterest` and `Pinterestbot` are explicitly allowed.

This is the canonical statement of how People Inc treats AI ingestion. Any agent reading People Inc content must honor it.

## Brand portfolio (sampled)

- **Entertainment:** PEOPLE, PEOPLE en Español, Entertainment Weekly
- **Home:** Better Homes & Gardens, Real Simple, Southern Living, The Spruce, Martha Stewart, Magnolia, Midwest Living
- **Food & Drink:** Allrecipes, Food & Wine, EatingWell, Serious Eats, Simply Recipes, The Spruce Eats, Liquor.com
- **Health:** Verywell Health, Verywell Mind, Verywell Fit, Health, Parents
- **Finance:** Investopedia, The Balance
- **Beauty & Style:** Byrdie, Brides, InStyle, Shape
- **Travel:** Travel + Leisure, TripSavvy
- **Tech & Sustainability:** Lifewire, Treehugger
- **Pets:** Daily Paws, The Spruce Pets
- **Premium Publishing:** Cooking Light, Coastal Living, Traditional Home, LIFE

## Offices

- New York — 225 Liberty St, 4th Fl, New York, NY 10281 (HQ; (212) 204-4000)
- Des Moines — 1716 Locust St, Des Moines, IA 50309 (legacy Meredith HQ)
- Birmingham — 4100 Old Montgomery Hwy, Birmingham, AL 35209 (Southern Progress legacy)

## Sources

- IAC brand page: https://www.iac.com/brands/peopleinc
- People Inc corporate site (via Wayback): https://web.archive.org/web/2026/https://www.people.inc/
- Wikipedia: https://en.wikipedia.org/wiki/People_Inc.
- Wikipedia: https://en.wikipedia.org/wiki/Meredith_Corporation
