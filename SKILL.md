---
name: running-marketing-campaigns
description: >
  Plans, creates, and optimizes digital marketing campaigns including content
  strategy, social media, email marketing, SEO, and AI visibility (GEO). Generates UTM
  parameters and tracking URLs. Helps develop go-to-market strategies,
  campaign messaging, content calendars, performance measurement frameworks,
  search engine optimization, and generative engine optimization for AI chatbots.
  Use when creating marketing campaigns, planning content strategy, building email
  sequences, setting up campaign tracking, analyzing marketing metrics, launching
  products, optimizing for search engines, or improving visibility in AI-generated
  responses. Supports both marketing beginners learning fundamentals and experienced
  marketers needing execution templates and benchmarks.
license: MIT
metadata:
  version: 1.2.0
  domains: [content, social, email, analytics, gtm, brand, seo, geo]
  author: Claude Skills
---

# Marketing Campaign Execution

Plan, execute, and measure digital marketing campaigns across content, social, email, and analytics.

## Quick Start

### Generate UTM Parameters
```
Source: where traffic originates (google, facebook, newsletter)
Medium: how it arrives (cpc, email, social, organic)
Campaign: initiative name (spring-sale-2025, product-launch)

Format: lowercase, hyphens, no spaces
Example: ?utm_source=linkedin&utm_medium=social&utm_campaign=q1-launch
```

### Create Email Sequence
1. Welcome (immediate): Set expectations, deliver promised value
2. Value (day 2-3): Best content or quick win
3. Engagement (day 5-7): Encourage reply or action
4. Offer (day 10): Clear CTA with incentive

### Plan Content Calendar
Essential fields: Title, Target keyword, Funnel stage (TOFU/MOFU/BOFU), Format, Owner, Publish date, Distribution channels.

### Check Campaign Performance
Primary metrics by channel:
- Email: Open rate (43% avg), CTR (2% avg), Conversion rate
- Social: Engagement rate, Reach, Click-through
- Paid: ROAS, CPA, CTR
- Content: Traffic, Time on page, Conversions

## Domain Reference Guide

| Need | Reference | When to Load |
|------|-----------|--------------|
| Plan content strategy | [content-strategy.md](references/content-strategy.md) | Topic clusters, calendars, funnel mapping, repurposing |
| Execute social media | [social-media.md](references/social-media.md) | Platform tactics, posting times, engagement benchmarks |
| Build email campaigns | [email-marketing.md](references/email-marketing.md) | Sequences, subject lines, segmentation, deliverability |
| Track campaigns | [utm-tracking.md](references/utm-tracking.md) | UTM formatting, naming conventions, GA4 alignment |
| Measure performance | [analytics-measurement.md](references/analytics-measurement.md) | KPIs, GA4 setup, attribution, ROI calculations |
| Launch products | [gtm-tools.md](references/gtm-tools.md) | GTM frameworks, positioning, tool selection |
| Define brand voice | [brand-guidelines.md](references/brand-guidelines.md) | Voice dimensions, tone, messaging framework, terminology |
| Optimize for search | [seo-optimization.md](references/seo-optimization.md) | Technical SEO, on-page, content SEO, link building, E-E-A-T |
| Optimize for AI | [geo-optimization.md](references/geo-optimization.md) | GEO, LLMO, AEO, AI Overviews, chatbot visibility |

## Scripts

Python utilities for campaign automation:

| Script | Purpose | Usage |
|--------|---------|-------|
| [utm_tools.py](scripts/utm_tools.py) | UTM generation, validation, batch processing, QR codes | `python utm_tools.py generate --source facebook --medium paid-social --campaign q1-launch` |
| [brand_checker.py](scripts/brand_checker.py) | Brand voice compliance, readability scoring, banned words | `python brand_checker.py check --file copy.txt` |

### Script Quick Reference

**Generate and validate UTMs:**
```bash
# Generate UTM parameters
python scripts/utm_tools.py generate -s facebook -m paid-social -c spring-2025

# Build complete tracking URL
python scripts/utm_tools.py build -u https://example.com -s email -m newsletter -c q1-launch

# Validate existing URL
python scripts/utm_tools.py validate -u "https://example.com?utm_source=email&utm_medium=cpc"

# Batch process from CSV
python scripts/utm_tools.py batch -f campaigns.csv -u https://example.com -o tracking.csv

# Check GA4 channel mapping
python scripts/utm_tools.py ga4-check -s facebook -m paid-social
```

**Check brand compliance:**
```bash
# Full compliance check
python scripts/brand_checker.py check --file marketing_copy.txt

# Check readability score
python scripts/brand_checker.py readability --text "Your marketing copy here"

# Find banned words
python scripts/brand_checker.py banned --file email_draft.txt

# Full audit with JSON output
python scripts/brand_checker.py full-audit --file campaign.txt --output report.json
```

## Workflow Decision Tree

**What does the user need?**

```
Creating or planning content?
├─ Yes → content-strategy.md
│        • Topic clusters, pillar pages
│        • Content calendars (annual/quarterly/weekly)
│        • TOFU/MOFU/BOFU mapping
│        • Repurposing workflows
└─ No ↓

Platform-specific social guidance?
├─ Yes → social-media.md
│        • Instagram, LinkedIn, TikTok, X, Facebook
│        • Posting cadence and timing
│        • Algorithm priorities
│        • Engagement benchmarks
└─ No ↓

Email campaigns or sequences?
├─ Yes → email-marketing.md
│        • Welcome, drip, re-engagement sequences
│        • Subject line optimization
│        • Segmentation strategies
│        • Deliverability requirements
└─ No ↓

UTM parameters or tracking URLs?
├─ Yes → utm-tracking.md + scripts/utm_tools.py
│        • Parameter formatting rules
│        • Naming conventions
│        • GA4 channel alignment
│        • Dynamic parameters for ads
│        • Batch URL generation
└─ No ↓

Analytics, metrics, or reporting?
├─ Yes → analytics-measurement.md
│        • KPIs by channel
│        • GA4 configuration checklist
│        • Attribution models
│        • ROI formulas
└─ No ↓

Product launch or go-to-market?
├─ Yes → gtm-tools.md
│        • SOSTAC, RACE, AARRR frameworks
│        • Launch campaign structure
│        • Positioning methodology
│        • Marketing tool selection
└─ No ↓

Brand voice, tone, or messaging?
├─ Yes → brand-guidelines.md + scripts/brand_checker.py
│        • Voice dimension matrix
│        • This-but-not-that chart
│        • Messaging framework
│        • Terminology standards
│        • Compliance checking
└─ No ↓

SEO or search engine optimization?
├─ Yes → seo-optimization.md
│        • Technical SEO (crawling, indexing, speed)
│        • On-page SEO (titles, headers, content)
│        • Content SEO (E-E-A-T, topic clusters)
│        • Link building strategies
│        • Core Web Vitals
└─ No ↓

AI visibility, GEO, or chatbot optimization?
├─ Yes → geo-optimization.md
│        • Generative Engine Optimization (GEO)
│        • LLMO (Large Language Model Optimization)
│        • AEO (Answer Engine Optimization)
│        • ChatGPT, Perplexity, AI Overviews visibility
│        • Content structure for AI citation
└─ No → Clarify the specific marketing need
```

## Multi-Domain Queries

Some requests span multiple domains. Load references in this order:

**"Plan a product launch"**
1. gtm-tools.md — Launch structure, positioning
2. brand-guidelines.md — Messaging framework, voice alignment
3. content-strategy.md — Content calendar for launch
4. email-marketing.md — Announcement sequences
5. social-media.md — Platform-specific launch tactics

**"Set up campaign tracking and reporting"**
1. utm-tracking.md — Parameter setup
2. analytics-measurement.md — GA4 configuration, dashboards

**"Create a quarterly marketing plan"**
1. content-strategy.md — Content pillars and calendar
2. social-media.md — Platform strategy
3. email-marketing.md — Email calendar
4. analytics-measurement.md — KPIs and reporting cadence

**"Optimize campaign performance"**
1. analytics-measurement.md — Identify metrics gaps
2. Then domain-specific reference based on underperforming channel

**"Define our brand voice"**
1. brand-guidelines.md — Voice dimensions, this-but-not-that chart
2. Use brand_checker.py to validate existing copy

**"Improve search rankings"**
1. seo-optimization.md — Technical audit, on-page optimization
2. content-strategy.md — Topic clusters, content gaps
3. analytics-measurement.md — Track ranking improvements

**"Get content cited by AI (ChatGPT, Perplexity)"**
1. geo-optimization.md — GEO strategies, content structure for AI
2. seo-optimization.md — Foundation for discoverability
3. content-strategy.md — Authority-building content

**"Full digital marketing strategy"**
1. seo-optimization.md — Search foundation
2. geo-optimization.md — AI visibility
3. content-strategy.md — Content planning
4. social-media.md — Distribution channels
5. email-marketing.md — Nurture sequences
6. analytics-measurement.md — Measurement framework

## Campaign Validation Checklist

Before launching any campaign, verify:

### Strategy
- [ ] Target audience clearly defined
- [ ] Campaign goals documented with baseline metrics
- [ ] Success criteria established (KPIs + targets)
- [ ] Timeline and milestones set

### Tracking
- [ ] UTM parameters validated (lowercase, hyphens, no spaces)
- [ ] GA4 channel alignment confirmed
- [ ] Conversion tracking tested
- [ ] Attribution model selected

### Content
- [ ] Brand voice checklist completed
- [ ] No banned words or unsubstantiated claims
- [ ] Readability score acceptable (60+ Flesch)
- [ ] CTA clear and actionable

### Technical
- [ ] Email sequences tested in preview
- [ ] Links verified working
- [ ] Mobile responsiveness checked
- [ ] Analytics tracking confirmed

## Persona Adaptation

**Beginner signals:** Asks "what is," "how do I," "why should I," unfamiliar terminology, requests explanations.
→ Provide concept context before tactics. Explain frameworks. Offer templates to follow.

**Experienced signals:** Uses correct terminology, asks for benchmarks, requests templates, mentions specific tools.
→ Skip fundamentals. Provide benchmarks, templates, advanced tactics directly.

## Boundaries

**In scope:**
- Campaign strategy and planning
- Content calendars and topic clusters
- Social media tactics and scheduling guidance
- Email sequences and copy frameworks
- UTM parameter generation and governance
- Marketing analytics and KPI frameworks
- Go-to-market planning and positioning
- Marketing tool recommendations
- Brand voice and messaging frameworks
- Copy compliance checking

**Out of scope (suggest alternatives):**
- Paid ad campaign management (bid strategies, audience targeting)
- CRM workflow implementation
- Website design/development
- Technical SEO (crawling, indexing, schema markup)
- Brand identity design (logos, colors, visual design)
- PR and media relations
- General copywriting (not campaign-specific)

**Clarify before proceeding:**
- "Help with marketing" → Which domain?
- "Improve my ads" → Creative/copy (in scope) or campaign management (out of scope)?
- "Analytics setup" → Marketing analytics or general web analytics?
- "Brand guidelines" → Voice/messaging (in scope) or visual identity (out of scope)?
