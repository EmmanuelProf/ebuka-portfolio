# WORKFLOW_VISUALS.md
## Portfolio Case Studies — Ebuka Anulugwo
### For Claude Code: Image placement guide + full case study content

---

## IMAGE FILES

All 6 screenshots are in `/public/screenshots/` as `.png` files.
Update ALL image references from `.jpg` to `.png`.

| File | Workflow | Notes |
|---|---|---|
| `aurelius.png` | Aurelius Customer Support Agent v2 | Complex multi-section canvas, colour-coded with sticky notes |
| `apex.png` | APEX #1 — Lead Qualification & CRM | 3-way Hot/Warm/Cold routing, branching clearly visible |
| `video.png` | BETRAYAL-6 — Video Generator | Long horizontal linear pipeline |
| `social-factory.png` | African Stories — YouTube Auto-Poster | Content-to-publish pipeline |
| `lifi.png` | Solana Token Scanner | DeFi/fintech AI agent pipeline |
| `whatsapp.png` | Agent — Smart Onboarding System | Multi-channel agent: Chat, Telegram, Form triggers |

---

## SECTION 1: FEATURED WORKFLOW CARDS

Each of the 6 workflow cards on the homepage uses one of these images as a background (dark overlay + text on top). Wire them as follows:

| Card | Image file |
|---|---|
| Aurelius Customer Support Agent v2 | `aurelius.png` |
| APEX Sales Automation Suite | `apex.png` |
| Multi-Platform Social Media Factory | `social-factory.png` |
| AI Viral Video Generator | `video.png` |
| LI.FI Autonomous Capital Manager | `lifi.png` |
| WhatsApp AI Assistant | `whatsapp.png` |

---

## SECTION 2: APEX SALES SUITE — CASE STUDY

**Page section heading:** "Case Study: APEX Sales Automation Suite"
**Subheading:** "3 workflows. 46 nodes. A full sales pipeline — from first contact to signed proposal — running without a single manual step."

**Hero image:** `apex.png` — full width, dark overlay, title text on top.
**What the screenshot shows:** The APEX #1 canvas with Contact Form Webhook on the left feeding into Normalise, AI Lead Scorer, Parse Score, then a Switch node branching into 3 paths — Airtable Hot Lead + Slack alert (top), Airtable Warm Lead + Slack alert (middle), Airtable Cold Lead + Gmail acknowledgement (bottom) — all converging at Google Sheets on the far right.

### WRITTEN CONTENT — paste directly into the page:

---

**The Problem**

A sales team was manually qualifying every inbound lead, writing every follow-up email by hand, and drafting proposals from scratch each time. Hours of work per day, inconsistent results, leads falling through the cracks.

**What was built**

Three connected n8n workflows that handle the entire pipeline automatically.

**APEX #1 — Lead Qualification & CRM Auto-Update (13 nodes)**

The moment a contact form is submitted, the workflow fires. It immediately sends a `200 OK` back to the user so they never wait, then in parallel: cleans and enriches the lead data (extracts first name, identifies business vs personal email, maps team size to a numeric signal), sends everything to Claude 3.5 Haiku via OpenRouter with a system prompt that returns a strict JSON score from 0–100, a tier (hot/warm/cold), the primary pain point, recommended action, and deal value estimate.

A Switch node reads the tier and routes to one of three paths. Hot leads go to Airtable and trigger an immediate Slack alert to the `#sales` channel: score, pain point, deal value, recommended action, follow up within 2 hours. Warm leads get the same treatment with a 3-day window. Cold leads get a personalised acknowledgement email via Gmail. Every lead — regardless of tier — logs to a Google Sheet with 13 fields.

**APEX #2 — Reply-Aware Follow-Up Sequence (21 nodes)**

Watches the Google Sheet. The moment a hot or warm lead is logged, a 7-day sequence begins. Day 1: wait, check Gmail API for a reply, no reply → send value prop email with Calendly link. Day 3: check again, no reply → send social proof email ("38 hours saved"). Day 7: check one final time, no reply → send soft close. At every checkpoint, if `resultSizeEstimate > 0` from the Gmail API, the sequence stops immediately. No chasing people who already said yes.

**APEX #3 — AI Proposal Generator (12 nodes)**

A 5-field intake form triggers the workflow. AI generates the full proposal content via OpenRouter. A Google Doc template is copied, every placeholder replaced via the Docs batchUpdate API. A Notion record is created for tracking. The sales rep gets notified simultaneously on Slack and Gmail — with the document link — within 30 seconds of submitting the form.

**The result:** Lead submits a form. Within 4 seconds, AI has scored them, they're in the CRM, the team is alerted on Slack, and an acknowledgement email is in their inbox. If they don't reply, a 7-day intelligent sequence runs itself. If they want a proposal, it's generated and delivered in 30 seconds. Zero manual steps.

---

## SECTION 3: AURELIUS AGENT — CASE STUDY

**Page section heading:** "Case Study: Aurelius Customer Support Agent v2"
**Subheading:** "78 nodes. One workflow. The difference between a chatbot and an autonomous support system."

**Hero image:** `aurelius.png` — full width. The screenshot shows a large canvas with distinct colour-coded sections separated by sticky notes (Entry Flow, Intent Routing, department sections for KYC/Finance/Projects/Communications, Output & Logging), dozens of interconnected nodes with curved connection lines showing the complexity of the routing logic.

### WRITTEN CONTENT — paste directly into the page:

---

**This is not a chatbot**

A chatbot answers questions from a script. Aurelius is an autonomous support system — it remembers every conversation, understands context, classifies intent, routes to the right logic, and only involves a human when it genuinely needs to.

**Persistent memory via Mem0**

Before responding to any message, Aurelius queries Mem0 for the user's full conversation history. It knows what they asked last week, what was tried, what their ongoing issue is. After every response, the conversation is written back to Mem0. The next time they message — 5 minutes or 5 weeks later — Aurelius picks up exactly where it left off.

**Intent classification and routing**

Every incoming message is classified before any response is generated. The classification reads the message content and memory context together. "That didn't work" means something completely different depending on the last 3 messages. Based on intent, the workflow routes to the appropriate section — general enquiries, technical issues, billing, complaints, or out-of-scope.

**Deployed on Telegram and WhatsApp simultaneously**

Both platforms feed into the same workflow through a single entry point. The routing logic handles platform differences transparently — the same memory, same intelligence, same quality on both channels.

**Human escalation that actually works**

When Aurelius can't resolve something, it doesn't send a generic "I'll get someone." It packages the full conversation, the memory summary, every attempted resolution step, and a suggested next action — then sends it to the human agent queue. The human opens the ticket and immediately has the full picture. No re-explanation needed from the customer.

**78 nodes.** Each one is a discrete operation — an API call, a decision branch, a data transformation, a memory read or write. The complexity is what makes it reliable. Simpler systems break on edge cases. This one was built to handle them.

---

## SECTION 4: PORTFOLIO PAGE (/portfolio)

**Filter tabs:** All · AI Agents · Sales AI · Fintech · Content AI · Conversational AI · Data · Research

**All workflows to display:**

| Name | Nodes | Category | Image | Description |
|---|---|---|---|---|
| Aurelius Customer Support Agent v2 | 78 | AI Agent | `aurelius.png` | Full AI support: memory, intent routing, escalation — live on Telegram & WhatsApp |
| Multi-Platform Social Media Factory | 57 | Content AI | `social-factory.png` | AI content generation + publish across 6+ platforms simultaneously |
| APEX Sales Automation Suite | 46 | Sales AI | `apex.png` | 3 workflows: AI lead scoring → CRM routing → reply-aware follow-up → AI proposal generation |
| AI Viral Video Generator | 40 | Video AI | `video.png` | Script to published video: ElevenLabs, Pexels, YouTube API |
| WhatsApp AI Assistant | 32 | Conversational AI | `whatsapp.png` | Multimodal agent: text, voice, images, PDFs — multiple entry points |
| AI Data Analyst — Chat with DB | 31 | Data | *(no image)* | Natural language → AI SQL → live database query results |
| ARIA — AI Life Coach | 21 | AI Agent | *(no image)* | Persistent memory life coach with long-term session context via Mem0 |
| LI.FI Autonomous Capital Manager | 24 | Fintech | `lifi.png` | Autonomous DeFi position monitoring and cross-chain execution |
| AI Tech Newsletter | 24 | Content AI | *(no image)* | RSS ingestion → AI curation → automated email delivery |
| Reddit Pain Point Tracker | 20 | Research AI | *(no image)* | Monitors subreddits for business pain points and opportunity signals |
| NFT Mint Tracker v2 | 16 | Fintech | *(no image)* | Watchlist-based NFT mint tracker with sold-out detection |
| APEX #1 — Lead Qualification | 13 | Sales AI | `apex.png` | AI lead scorer → Hot/Warm/Cold CRM routing via Airtable + Slack |
| APEX #3 — AI Proposal Generator | 12 | Sales AI | `apex.png` | AI generates proposal → populates Google Doc → notifies team |
| DYOR Intelligence Agent | 11 | Research AI | *(no image)* | On-chain + narrative research agent for early-stage crypto evaluation |
| CA Intelligence Analyzer | 11 | Fintech | *(no image)* | Contract address intelligence: liquidity, wallet scoring, market cap |

Note at bottom of portfolio page:
*"92 total workflows built. Showing the 15 most complex and commercially relevant. Additional workflows available on request."*

---

## SECTION 5: IMAGE DISPLAY GUIDELINES FOR CLAUDE CODE

- All images are n8n canvas screenshots — dark-ish background with coloured nodes
- Display them with a subtle dark overlay (rgba 0,0,0,0.35) so text on top is readable
- On the workflow cards: image fills the card background, overlay applied, category badge + name + description + node count displayed over it
- On the case study sections: image is full-width hero, 320px height, overlay, title text centred on top
- Images should have `border-radius` matching the card style
- On hover: reduce overlay opacity slightly (0.2) to let the canvas detail show through — this rewards curiosity
- All images are `.png` — no `.jpg` references anywhere in the codebase

---

*Updated June 2026 — screenshots taken via Playwright from live n8n instances*
*aurelius.png, apex.png, video.png: Render instance (n8n-q88i.onrender.com)*
*social-factory.png, lifi.png, whatsapp.png: ngrok instance (ungnawed-imaginational-dione.ngrok-free.dev)*
