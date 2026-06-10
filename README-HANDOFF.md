# README-HANDOFF — Hestia Foundation

## What This Is

Hestia Foundation is a **non-profit housing advocacy organization** based in Lagos, Algarve, Portugal. Its purpose is to design, document, and distribute open-source construction systems that enable families to build durable, energy-independent homes using locally available materials.

The starting prototype is **Shell A**: a 7×12 meter modular house built primarily from EPAL pallets and modern low-cost framing, with a hard ceiling of **€20,000 for the shell** and **€50,000 finished** (materials only — labor is deliberately excluded because the model is DIY/self-build, like Amish or Jehovah's Witness construction).

## Why This Exists (The Human Behind It)

The founder (Sebastian) sees housing as a **human right parallel to clean water**. He is furious that housing became a financialized investment vehicle instead of family shelter. The economic argument is the beating heart:

- In 1970s Sweden, 2 years of average salary bought a home. Now it takes 8 years.
- In Portugal, the average property requires 19 years of gross income.
- EU house prices up 60% since 2013. Rents up 20%. Only 6–7% social housing stock. 20% of housing unoccupied.

This is not a startup. It is not a charity. It is a **systemic intervention** that treats shelter as infrastructure, not commodity. The aesthetic is "pallet logic × modern low-cost construction × open-source framing × elegant minimal aesthetics." Think Japanese joinery applied to pallets. Not ugly. Not temporary. Not tents.

## The Website

- **Production:** https://hestiafoundation.org (Cloudflare Pages)
- **Design language:** Clean, data-driven, minimal, no blue-purple gradients, no AI-slop. Visual references are uploaded as book page images — the human prefers screenshots over verbal descriptions.
- **SEO strategy:** Hundreds of blog posts drawing traffic from multiple angles. Ragebait titles are deliberate and grounded in real claims (e.g., framing a €20k pallet house as "luxury" to challenge assumptions).
- **No pedestal language.** The human rejects phrasing that puts the project on a pedestal. Community-praising, problem-focused, humble positioning. If you write like a pretentious 20-year-old, he will correct you harshly.

## Key Constraints (Do Not Violate)

| Constraint | Value |
|------------|-------|
| Shell cost ceiling | €20,000 |
| Finished house cost ceiling | €50,000 (materials only, labor excluded) |
| Build time | 2 weeks |
| Default footprint | 7m × 12m |
| Labor model | DIY/self-build (Amish/JW efficiency, not professional contractors) |
| Data sources | Official statistical governing bodies, 2025–26 research, averaged across Germany/Sweden/UK |

Every cost claim must be **verifiable with citations**. The human will check.

## Repo Structure

```
hestia-foundation/
├── website/              # Cloudflare Pages site (hestiafoundation.org)
│   ├── index.html        # Homepage — OMNIBUS DOMUS DIGNA motto
│   ├── manifesto.html    # Standalone manifesto (v1.1)
│   ├── the-system.html   # Build system explanation
│   ├── lineage.html      # Historical/cultural lineage
│   ├── costs.html        # Cost breakdowns
│   ├── build.html        # Build protocol overview
│   ├── faq.html          # FAQ
│   ├── get-involved.html # Volunteer/partner page
│   ├── grants.html       # Grant strategy
│   ├── partners.html     # Partner organizations
│   ├── pitch.html        # One-pager pitch
│   ├── prototype.html    # Prototype status
│   ├── research.html     # Research hub
│   ├── resources.html    # Downloadable resources
│   ├── timeline.html     # Project timeline
│   ├── blog/             # Blog posts (SEO traffic engine)
│   ├── images/           # All visual assets
│   ├── style.css         # Global styles
│   └── favicon.svg       # Brand icon
│
├── docs/                 # Strategic documents (NOT the website)
│   ├── HESTIA_SETUP.md           # Complete setup checklist
│   ├── HESTIA_PITCH.md           # One-page pitch
│   ├── HESTIA_ACTION_LIST.md     # Immediate 10-step action list
│   ├── STATUS_REPORT.md          # Comprehensive dashboard
│   ├── PORTUGAL_GRANT_STRATEGY.md # Portugal-specific advantages (39.3% success rate)
│   ├── contact_database.md       # 15+ verified contacts (UAlg, LNEC, ANI, FCT)
│   ├── FINANCIAL_MODEL.md        # 3-scenario projection
│   ├── VOLUNTEER_RECRUITMENT.md  # How to join
│   ├── SOCIAL_MEDIA_STARTER_PACK.md # Content strategy
│   ├── build/                    # Construction docs
│   ├── grants/                   # Grant applications
│   ├── legal/                    # Portuguese non-profit bylaws
│   ├── outreach/                 # Partnership emails
│   ├── press/                    # Press kit
│   └── risk/                     # Risk assessment
│
└── .github/              # GitHub Actions for CI/CD
```

## Active Work Streams

1. **Blog content factory** — Hundreds of posts planned. Every post must be grounded in real data, cite sources, and draw traffic from a specific angle.
2. **Grant applications** — HORIZON-NEB-2026-01-REGEN-01 (€4M, deadline 01/12/2026), NEB Boost (€30K), NEB Facility (€50K–€5M), Horizon Europe Clusters 4/5/6, LIFE Programme.
3. **Legal entity** — Need 3 founding members with Portuguese NIFs to register as Associação.
4. **Prototype site** — Need 200m²+ flat land in Lagos area.
5. **University partnerships** — UAlg (University of Algarve), LNEC (structural testing).

## Deployment

- **Platform:** Cloudflare Pages
- **Build:** Static HTML/CSS/JS — no build step required
- **Domain:** hestiafoundation.org
- **DNS:** Cloudflare
- **Updates:** Push to GitHub → auto-deploy via Cloudflare Pages integration

## How to Not Fuck This Up

1. **Do not use blue-purple gradients.** Do not use AI-slop aesthetic. Reference specific designers/painters/writers if you need visual direction. The human uploads book pages as design spec — use them.
2. **Do not write pedestal language.** "We are changing the world" gets corrected. "This is a serious problem and here is a practical solution" is the tone.
3. **Do not make up statistics.** Every cost, ratio, and timeline must be traceable to a real source. Cite on the website.
4. **Do not remove images.** The human treats visual assets as primary specification material. If you change the site, images stay.
5. **Do not add em-dashes.** The human banned them as an AI-tell.
6. **Keep it plainspoken.** Overwrought prose gets cut. Short sentences. Concrete nouns. No inflated symbolism.

## Current Status (as of handoff)

- Website: Live, 20+ pages
- Blog: 4+ posts published, more in pipeline
- Legal entity: In progress (needs 3 founding members)
- Prototype: Pending site acquisition
- Grants: Framework ready, applications not yet submitted

## Contact & Ownership

- **Human:** Sebastian (sebastianbrosche on GitHub)
- **Location:** Lagos, Algarve, Portugal
- **Email:** Via hestiafoundation.org contact form
- **This repo:** github.com/sebastianbrosche/hestiafoundation

---

*"Day one. Begin recording everything about this one."*
