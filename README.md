# Running Marketing Campaigns - Claude Agent Skill

A comprehensive Claude Code skill for planning, executing, and measuring digital marketing campaigns across content, social media, email, and analytics channels.

## Features

- **UTM Campaign Tracking** - Generate, validate, and batch-process UTM parameters with GA4 channel alignment
- **Content Strategy** - Topic clusters, content calendars, funnel mapping, and repurposing workflows
- **Email Marketing** - Sequence templates, subject line optimization, segmentation strategies
- **Social Media** - Platform-specific tactics, posting schedules, engagement benchmarks
- **Analytics & Measurement** - KPI frameworks, attribution models, ROI calculations
- **Go-to-Market** - Launch frameworks (SOSTAC, RACE, AARRR), positioning methodology
- **Brand Voice** - Voice dimension matrix, tone guidelines, messaging frameworks, terminology standards
- **SEO Optimization** - Technical SEO, on-page optimization, content SEO, link building, E-E-A-T guidelines
- **GEO (Generative Engine Optimization)** - AI SEO, LLMO, AEO for ChatGPT, Perplexity, Google AI Overviews visibility

## Installing with Skilz (Universal Installer)

The recommended way to install this skill across different AI coding agents is using the **skilz** universal installer.

### Install Skilz

```bash
pip install skilz
```

This skill supports [Agent Skill Standard](https://agentskills.io/) which means it supports 14 plus coding agents including Claude Code, OpenAI Codex, Cursor and Gemini.

### Git URL Options

You can use either `-g` or `--git` with HTTPS or SSH URLs:

```bash
# HTTPS URL
skilz install -g https://github.com/SpillwaveSolutions/running-marketing-campaigns-agent-skill

# SSH URL
skilz install --git git@github.com:SpillwaveSolutions/running-marketing-campaigns-agent-skill.git
```

### Claude Code

Install to user home (available in all projects):
```bash
skilz install -g https://github.com/SpillwaveSolutions/running-marketing-campaigns-agent-skill
```

Install to current project only:
```bash
skilz install -g https://github.com/SpillwaveSolutions/running-marketing-campaigns-agent-skill --project
```

### OpenCode

Install for [OpenCode](https://opencode.ai):
```bash
skilz install -g https://github.com/SpillwaveSolutions/running-marketing-campaigns-agent-skill --agent opencode
```

Project-level install:
```bash
skilz install -g https://github.com/SpillwaveSolutions/running-marketing-campaigns-agent-skill --project --agent opencode
```

### Gemini

Project-level install for Gemini:
```bash
skilz install -g https://github.com/SpillwaveSolutions/running-marketing-campaigns-agent-skill --agent gemini
```

### OpenAI Codex

Install for OpenAI Codex:
```bash
skilz install -g https://github.com/SpillwaveSolutions/running-marketing-campaigns-agent-skill --agent codex
```

Project-level install:
```bash
skilz install -g https://github.com/SpillwaveSolutions/running-marketing-campaigns-agent-skill --project --agent codex
```

### Install from Skillzwave Marketplace

```bash
# Claude to user home dir ~/.claude/skills
skilz install SpillwaveSolutions_running-marketing-campaigns-agent-skill/running-marketing-campaigns

# Claude skill in project folder ./claude/skills
skilz install SpillwaveSolutions_running-marketing-campaigns-agent-skill/running-marketing-campaigns --project

# OpenCode install to user home dir ~/.config/opencode/skills
skilz install SpillwaveSolutions_running-marketing-campaigns-agent-skill/running-marketing-campaigns --agent opencode

# OpenCode project level
skilz install SpillwaveSolutions_running-marketing-campaigns-agent-skill/running-marketing-campaigns --agent opencode --project

# OpenAI Codex install to user home dir ~/.codex/skills
skilz install SpillwaveSolutions_running-marketing-campaigns-agent-skill/running-marketing-campaigns --agent codex

# OpenAI Codex project level ./.codex/skills
skilz install SpillwaveSolutions_running-marketing-campaigns-agent-skill/running-marketing-campaigns --agent codex --project

# Gemini CLI (project level) -- only works with project level
skilz install SpillwaveSolutions_running-marketing-campaigns-agent-skill/running-marketing-campaigns --agent gemini
```

See [Skill Listing](https://skillzwave.ai/skill/SpillwaveSolutions__running-marketing-campaigns-agent-skill__running-marketing-campaigns__SKILL/) to see how to install this exact skill to 14+ different coding agents.

### Other Supported Agents

Skilz supports 14+ coding agents including Windsurf, Qwen Code, Aidr, and more.

For the full list of supported platforms, visit [SkillzWave.ai/platforms](https://skillzwave.ai/platforms/) or see the [skilz-cli GitHub repository](https://github.com/SpillwaveSolutions/skilz-cli).

---

## Manual Installation

### Claude Code

```bash
# Clone to your Claude skills directory
git clone https://github.com/SpillwaveSolutions/running-marketing-campaigns-agent-skill.git \
  ~/.claude/skills/running-marketing-campaigns
```

### Other Methods

1. Download or clone this repository
2. Copy the contents to `~/.claude/skills/running-marketing-campaigns/`
3. Restart Claude Code to load the skill

## Usage

The skill activates automatically when you ask Claude about:

- Creating marketing campaigns
- Planning content strategy
- Building email sequences
- Setting up campaign tracking
- Analyzing marketing metrics
- Launching products
- Defining brand voice

### Example Prompts

```
"Help me plan a product launch campaign"
"Generate UTM parameters for my email newsletter"
"Create a content calendar for Q1"
"What KPIs should I track for social media?"
"Define our brand voice guidelines"
"Check if my marketing copy follows brand guidelines"
```

## Scripts

Two Python utilities are included for automation:

### utm_tools.py

Generate, validate, and audit UTM tracking URLs.

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

# Audit URLs for case inconsistencies
python scripts/utm_tools.py audit -f urls.txt

# Generate QR code (requires: pip install qrcode pillow)
python scripts/utm_tools.py qr -u "https://example.com?utm_source=qr" -o code.png
```

### brand_checker.py

Validate marketing copy against brand guidelines.

```bash
# Full compliance check
python scripts/brand_checker.py check --file marketing_copy.txt

# Check readability score
python scripts/brand_checker.py readability --text "Your marketing copy here"

# Find banned words and phrases
python scripts/brand_checker.py banned --file email_draft.txt

# Check terminology consistency
python scripts/brand_checker.py terminology --file copy.txt

# Full audit with JSON output
python scripts/brand_checker.py full-audit --file campaign.txt --output report.json

# List all banned words
python scripts/brand_checker.py list-banned
```

## Structure

```
running-marketing-campaigns/
├── SKILL.md                          # Main skill definition
├── README.md                         # This file
├── LICENSE                           # MIT License
├── references/
│   ├── analytics-measurement.md      # KPIs, GA4, attribution, ROI
│   ├── brand-guidelines.md           # Voice, tone, messaging, terminology
│   ├── content-strategy.md           # Topic clusters, calendars, funnel mapping
│   ├── email-marketing.md            # Sequences, subject lines, deliverability
│   ├── geo-optimization.md           # GEO, LLMO, AEO, AI visibility
│   ├── gtm-tools.md                  # Launch frameworks, positioning
│   ├── seo-optimization.md           # Technical, on-page, content SEO
│   ├── social-media.md               # Platform tactics, benchmarks
│   └── utm-tracking.md               # UTM formatting, GA4 alignment
└── scripts/
    ├── brand_checker.py              # Brand voice compliance checker
    └── utm_tools.py                  # UTM generation and validation
```

## Reference Guides

| Reference | Purpose |
|-----------|---------|
| [content-strategy.md](references/content-strategy.md) | Topic clusters, Hero-Hub-Hygiene, funnel mapping, atomization |
| [social-media.md](references/social-media.md) | Platform-specific tactics, posting times, algorithm priorities |
| [email-marketing.md](references/email-marketing.md) | Sequences, subject lines, segmentation, deliverability |
| [utm-tracking.md](references/utm-tracking.md) | UTM parameters, naming conventions, GA4 channel alignment |
| [analytics-measurement.md](references/analytics-measurement.md) | Marketing funnel KPIs, attribution models, reporting templates |
| [gtm-tools.md](references/gtm-tools.md) | SOSTAC, RACE, AARRR frameworks, launch planning |
| [brand-guidelines.md](references/brand-guidelines.md) | Voice dimensions, tone adaptation, messaging framework |
| [seo-optimization.md](references/seo-optimization.md) | Technical SEO, on-page, content SEO, link building, E-E-A-T |
| [geo-optimization.md](references/geo-optimization.md) | Generative Engine Optimization, LLMO, AEO, AI visibility |

## Brand Voice Features

The skill includes comprehensive brand voice tooling:

### Voice Dimensions Matrix

Define brand voice across 4 spectrums:
- **Formality**: Formal ↔ Casual
- **Energy**: Reserved ↔ Enthusiastic
- **Humor**: Serious ↔ Playful
- **Authority**: Peer ↔ Expert

### This-But-Not-That Chart

Clarify voice traits with boundaries:

| Trait | This Means... | But NOT... |
|-------|---------------|------------|
| Helpful | Guiding with expertise | Patronizing |
| Confident | Speaking with authority | Arrogant |
| Clear | Simple explanations | Dumbed down |

### Banned Words Detection

Automatically flag:
- Unsubstantiated superlatives ("best-in-class", "revolutionary")
- Corporate jargon ("synergy", "leverage", "circle back")
- Vague promises ("seamless", "frictionless", "robust")

## Requirements

- Claude Code CLI
- Python 3.8+ (for scripts)
- Optional: `qrcode`, `pillow` (for QR code generation)
- Optional: `requests` (for URL shortening via bit.ly)

## License

MIT License - See [LICENSE](LICENSE) for details.

## Contributing

Contributions welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## Related Resources

- [Claude Code Documentation](https://docs.anthropic.com/claude-code)
- [Claude Skills Specification](https://github.com/anthropics/claude-code/blob/main/docs/skills-spec.md)
- [GA4 Default Channel Groupings](https://support.google.com/analytics/answer/9756891)

---

<p align="center">
  <a href="https://skillzwave.ai/">SkillzWave.ai - Largest Agentic Marketplace for AI Agent Skills</a>
  <br>
  <a href="https://spillwave.com/">SpillWave - Leaders in AI Agent Development</a>
</p>
