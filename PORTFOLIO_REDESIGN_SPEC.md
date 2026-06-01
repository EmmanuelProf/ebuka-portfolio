# Portfolio Redesign Brief — Ebuka Anulugwo
### For Claude Code · Full Implementation

---

## The One Goal

When a hiring manager or recruiter lands on this site, they should feel one thing within 5 seconds:

> *"This person has already built serious AI systems. I need to talk to them."*

Right now the site looks like a template. It needs to look like a product built by someone who builds products.

---

## Current Problems to Fix (Non-Negotiable)

These are breaking issues. Fix all of them:

1. **Every nav link goes to `#`** — Home, Portfolio, About, "Get in touch", "View workflows →", "Hire me", "View all 92 workflows →" are all dead links. Wire them to the correct sections or pages.
2. **Portfolio page is a 404** — `/portfolio` returns NOT_FOUND. This needs to exist and work.
3. **"SOA Exam P & FM Passed" stat card** — remove from homepage entirely. Replace with: `78` / `Max Node Complexity` (referring to the Aurelius agent).
4. **No visual proof of work** — the site claims 92 workflows but shows zero screenshots. Add n8n canvas screenshots or workflow diagrams as visual evidence.

---

## Identity & Positioning

**Name:** Ebuka Anulugwo
**Title:** AI Automation Engineer · n8n Workflow Architect · Agent Builder
**Location:** Lagos, Nigeria — Available Remote Worldwide
**Email:** eanulugwo@gmail.com
**Phone:** +234 807 356 4384
**Current site:** https://ebuka-portfolio-mauve.vercel.app/

**The core positioning statement (use this, don't dilute it):**
> 92 production n8n workflows. Built alone. No team, no training programme — just shipping.

**Secondary proof points:**
- Most complex single workflow: 78 nodes (Aurelius Customer Support Agent)
- Domains covered: AI Agents, Fintech, Content AI, Conversational AI, Data, Sales Automation
- APIs integrated: 20+ platforms including ElevenLabs, Telegram, WhatsApp Business, Solana RPC, LI.FI Protocol, Pinecone, Supabase, Reddit, YouTube, Google Workspace, OpenRouter/Claude/GPT

---

## Aesthetic Direction

**Tone:** Dark, technical, confident. Think: a senior engineer's personal site, not a freelancer template.

**Reference feel:** Vercel's design language meets a terminal/builder aesthetic. Dark backgrounds, sharp typography, subtle green or electric blue accents that feel like system output. Monospace elements for node counts and technical details. Clean grid with deliberate asymmetry.

**NOT this:** White background editorial serif vibes. The current site looks like a writer's portfolio or a Notion export. That's the wrong signal.

**Specific design decisions:**
- Dark background (near-black, e.g. `#0a0a0a` or `#0d1117`) with light text
- Accent colour: electric green (`#00ff88`) OR electric blue (`#3b82f6`) — pick one and commit
- Monospace font for technical elements (node counts, category labels, stats)
- A distinctive display font for headings — something with character, NOT Inter/Arial/Roboto/Space Grotesk
- Subtle animated elements: a scrolling ticker of skills (already exists — keep it), maybe a node-connection animation or subtle grid pattern in the hero background
- Workflow cards should feel like actual system components — not blog post cards

---

## Site Structure

### Pages / Sections Required:

```
/ (Home)
  ├── Hero
  ├── Stats Bar
  ├── Skills Ticker (keep existing, style update)
  ├── Featured Workflows (6 cards)
  ├── Case Study Spotlight — APEX Sales System
  ├── Case Study Spotlight — Aurelius Agent
  └── CTA / Contact

/portfolio (currently 404 — must be created)
  ├── Filter bar (All | AI Agents | Sales AI | Fintech | Content AI | Conversational AI | Data)
  ├── All 15 workflows in a grid
  └── "More available on request" note

/about (or #about section)
  ├── Bio
  ├── How I work
  └── Contact form or mailto link
```

---

## Section-by-Section Spec

### 1. HERO SECTION

**Headline options (pick the strongest or combine):**
- "92 Production Workflows. Built Alone."
- "I Don't Talk About Automation. I Ship It."
- "AI Automation Engineer — 92 Systems in Production"

**Subtext:**
> n8n workflow architect and AI agent builder. I take broken, manual processes and replace them with reliable automation systems — from lead pipelines to autonomous DeFi agents to multi-platform content factories. 92 production workflows. No team. No tutorial that covered what I was actually building.

**Stats to show in hero (4 cards):**
| Stat | Label |
|------|-------|
| 92 | Production Workflows |
| 78 | Max Node Complexity |
| 20+ | APIs Integrated |
| 5+ | Domains Covered |

**CTAs:**
- Primary: `View My Work →` → scrolls to or links to /portfolio
- Secondary: `Get in Touch` → mailto:eanulugwo@gmail.com OR smooth scroll to contact section

**Hero visual idea:** Subtle animated SVG or CSS pattern in the background that suggests node connections — dots connected by lines, slowly animating. Or a faint grid. Something that says "systems builder" without being distracting.

---

### 2. SKILLS TICKER

Keep the scrolling marquee. Update the content to include:
`n8n · AI Agents · LLM Integration · API Orchestration · RAG Pipelines · Mem0 Memory · Persistent Memory Agents · Multi-Agent Systems · Fintech Automation · Content Pipelines · Telegram Bots · WhatsApp Business API · Solana RPC · DeFi Automation · Webhook Architecture · OpenRouter · Claude · GPT-4 · Supabase · Pinecone · Airtable · Google Workspace · ElevenLabs · YouTube API`

---

### 3. FEATURED WORKFLOWS SECTION

**Section headline:** "Systems I've Shipped"
**Subhead:** "A selection of the most complex and commercially relevant — independently designed, built, and deployed."

**6 featured workflow cards.** Each card must show:
- Category badge (monospace, styled like a terminal tag)
- Workflow name (bold, prominent)
- 1-line description
- Node count (styled prominently — this is a credibility signal)
- Stack tags (e.g. `n8n` `Mem0` `Telegram` `WhatsApp`)

**The 6 featured workflows:**

| # | Name | Nodes | Category | Description | Stack Tags |
|---|------|-------|----------|-------------|------------|
| 1 | Aurelius Customer Support Agent v2 | 78 | AI Agent | Full AI support system with persistent memory, intent routing, and human escalation. Live on Telegram & WhatsApp. | n8n · Mem0 · Telegram · WhatsApp · OpenRouter |
| 2 | Multi-Platform Social Media Factory | 57 | Content AI | AI content generation + simultaneous publish to 6+ platforms with zero manual intervention. | n8n · Claude · GPT · YouTube · Reddit |
| 3 | APEX Sales Automation Suite | 46 | Sales AI | 3-workflow sales system: AI lead scoring → CRM routing → reply-aware follow-up → AI proposal generation. | n8n · Airtable · Gmail · Slack · Google Docs · OpenRouter |
| 4 | AI Viral Video Generator | 40 | Video AI | End-to-end: script → voiceover → video assembly → published. Fully automated. | n8n · ElevenLabs · Pexels · YouTube API |
| 5 | LI.FI Autonomous Capital Manager | 24 | Fintech | Autonomous DeFi position monitoring and cross-chain execution. No manual intervention. | n8n · Solana RPC · Jupiter · LI.FI Protocol |
| 6 | WhatsApp AI Assistant | 32 | Conversational AI | Multimodal AI assistant: handles text, voice notes, images, and PDFs natively via WhatsApp. | n8n · WhatsApp Business API · Claude · OpenRouter |

**Visual upgrade for cards:** If possible, include a faint n8n canvas screenshot as a card background (blurred/darkened overlay). This gives visual proof of complexity without needing to explain it. Screenshots of n8n workflows look like circuit boards — they're visually impressive even blurred.

---

### 4. CASE STUDY SPOTLIGHT — APEX SALES SYSTEM

This is a key section. APEX is the most commercially relatable system for hiring managers at business-focused companies.

**Section headline:** "Case Study: APEX Sales Automation Suite"

**Layout:** Alternating text + visual. Or a 3-step flow diagram showing the pipeline.

**Content:**

**The problem:**
A sales team was manually qualifying every inbound lead, writing every follow-up email by hand, and drafting proposals from scratch each time. Hours of work per day, inconsistent results, leads falling through the cracks.

**What was built (3 workflows):**

**APEX #1 — Lead Qualification & CRM Auto-Update (13 nodes)**
- Contact form submission hits a webhook
- Lead data is normalised and enriched
- AI scorer (OpenRouter) rates the lead Hot, Warm, or Cold
- Routes to Airtable CRM automatically
- Hot leads → instant Slack alert to sales team
- Cold leads → automated acknowledgement email
- Every lead logged to Google Sheets

**APEX #2 — Follow-Up Sequence Engine (21 nodes)**
- Watches the lead sheet for new Hot/Warm leads
- Sends Day 1, Day 3, Day 7 follow-up emails via Gmail
- Before each email: checks if the lead has already replied
- If replied → sequence stops automatically. No awkward chasing.
- Logs sequence completion status

**APEX #3 — AI Proposal Generator (12 nodes)**
- Proposal intake form triggers the workflow
- AI generates full proposal content via OpenRouter
- Copies a Google Doc template
- Fills all placeholders automatically via Docs API
- Creates a Notion record for tracking
- Notifies sales rep via Slack + Gmail simultaneously

**Total: 3 workflows, 46 nodes, live in production.**

---

### 5. CASE STUDY SPOTLIGHT — AURELIUS AGENT

**Section headline:** "Case Study: Aurelius Customer Support Agent v2"

**The problem:**
Manual support — agents copy-pasting responses, no conversation memory, inconsistent quality, no escalation logic.

**What was built (78 nodes):**
- Deployed live on Telegram and WhatsApp simultaneously
- Receives any message → classifies intent → routes to appropriate response logic
- Persistent conversation memory via Mem0 — remembers the full history of every user
- Handles text, voice notes, and images natively
- Smart escalation: when it can't handle something, it passes the full conversation context to a human — not just a notification, a fully contextualised handoff
- 78 nodes. One workflow. Running without hand-holding.

**Why this matters for hiring managers:**
This is not a chatbot. This is an autonomous support system. The difference is in the memory architecture and the escalation logic — both of which took real engineering decisions to get right.

---

### 6. FULL PORTFOLIO PAGE (/portfolio)

**This page must exist and must not 404.**

**Filter bar at top:** All · AI Agents · Sales AI · Fintech · Content AI · Conversational AI · Data · Research

**All 15 workflows to list (pull from this data):**

| Name | Nodes | Category | Description |
|------|-------|----------|-------------|
| Aurelius Customer Support Agent v2 | 78 | AI Agent | Full AI support: memory, intent routing, escalation — live on Telegram & WhatsApp |
| Multi-Platform Social Media Factory | 57 | Content AI | AI content generation + publish across 6+ platforms simultaneously |
| AI Viral Video Generator | 40 | Video AI | Script to published video: ElevenLabs, Pexels, YouTube API |
| WhatsApp AI Assistant | 32 | Conversational AI | Multimodal: text, voice, images, PDFs via WhatsApp Business API |
| AI Data Analyst — Chat with DB | 31 | Data | Natural language → AI SQL → live database query results |
| APEX #2 — Follow-Up Sequence Engine | 21 | Sales AI | Reply-aware 7-day follow-up sequence, auto-stops on reply |
| ARIA — AI Life Coach | 21 | AI Agent | Persistent memory life coach with long-term session context via Mem0 |
| LI.FI Autonomous Capital Manager | 24 | Fintech | Autonomous DeFi position monitoring and cross-chain execution |
| AI Tech Newsletter — RSS + Gmail | 24 | Content AI | RSS ingestion → AI curation → automated email delivery |
| Reddit Pain Point Tracker | 20 | Research AI | Monitors subreddits for business pain points and opportunity signals |
| NFT Mint Tracker v2 | 16 | Fintech | Watchlist-based NFT mint tracker with sold-out detection |
| APEX #1 — Lead Qualification & CRM | 13 | Sales AI | AI lead scorer → Hot/Warm/Cold CRM routing via Airtable + Slack |
| APEX #3 — AI Proposal Generator | 12 | Sales AI | AI generates proposal → populates Google Doc template → notifies team |
| DYOR Intelligence Agent | 11 | Research AI | On-chain + narrative research agent for early-stage crypto evaluation |
| CA Intelligence Analyzer | 11 | Fintech | Contract address intelligence: liquidity, wallet scoring, market cap |

Add a note at the bottom: *"92 total workflows built. Showing the 15 most complex and commercially relevant. Additional workflows available on request."*

---

### 7. CONTACT / CTA SECTION

**Headline:** "Let's build something that actually runs"

**Body:**
> I'm available for remote roles and freelance automation projects worldwide. If you have a manual process that should be automated, or you're building a team that needs someone who ships — let's talk.

**Contact details:**
- Email: eanulugwo@gmail.com
- Phone: +234 807 356 4384
- Location: Lagos, Nigeria — Remote Worldwide

**CTA buttons:**
- `Send an Email` → mailto:eanulugwo@gmail.com
- `Download CV` → link to CV PDF (generate one or leave as placeholder)

---

## Technical Notes for Claude Code

- **Framework:** Match whatever the current codebase uses. The existing site appears to be a single-page React/Next.js app deployed on Vercel.
- **Check the existing codebase first** before writing anything — understand what's already there and extend it rather than rewriting unnecessarily.
- **Routing:** Fix all `href="#"` links. Wire nav to actual sections using smooth scroll or Next.js router. Create the `/portfolio` route properly.
- **Images:** For the n8n workflow screenshots — if actual screenshots aren't available in the repo, use a placeholder approach: a dark card with a subtle animated CSS pattern that suggests a node graph. When real screenshots are added later, they drop straight in.
- **Fonts:** Load from Google Fonts. Suggested pairing: a geometric/technical display font (e.g. Space Mono, JetBrains Mono, or Syne) for headings and stats, and a clean readable sans for body. Avoid Inter, Roboto, Arial.
- **Animations:** CSS transitions and keyframes preferred. Keep them subtle and purposeful — entrance animations on scroll for sections, hover states on cards, the ticker scroll.
- **Mobile:** Must be fully responsive. The workflow card grid should stack to 1 column on mobile.
- **Performance:** No heavy libraries just for visual effects. CSS-only where possible.

---

## What "Done" Looks Like

A recruiter lands on the site and within 5 seconds they understand:
1. This person builds real AI automation systems at serious scale (92 workflows, 78-node max)
2. They can see specific proof — APEX system, Aurelius agent, node counts, stack tags
3. There's a clear, working way to contact this person
4. The site itself is evidence of craft and attention to detail

Every link works. The portfolio page exists. The visual design signals "technical" not "template."

---

*Brief prepared by Claude — June 2026*
*For questions about specific workflow details, Ebuka can provide n8n screenshots, JSON exports, or additional context on any system listed above.*
