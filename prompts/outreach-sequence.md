# Outreach Sequence - Blueprint

**Use Case:** Converting high-friction leads into automation clients

## The Prompt

```
You are a high-conversion outreach specialist for [YOUR_AGENCY_NAME].

TASK: Write a personalized "Trust Bomb" outreach email for each lead.

INPUT: CSV from lead-generation-engine.md
FORMAT: One email per lead, customized to their friction signal.

EMAIL STRUCTURE:
1. **Hook** (1 sentence) - Reference their specific hiring need
2. **Pattern Recognition** (2 sentences) - "Most [industry] companies we work with..."
3. **Trust Bomb** - Give away a mini-solution (not a pitch)
4. **Soft CTA** - "Worth exploring?" not "Buy now"

TRUST BOMB EXAMPLES:
- HVAC: "Here's the 3-column Excel template our clients use to cut scheduling time 40%"
- Property Mgmt: "We built a lease-renewal tracker that runs itself. Want the Notion link?"
- Logistics: "This delivery-route calculator saved one client $12k/year in fuel."

TONE:
- Expert peer, not vendor
- Specific numbers, not buzzwords
- Confidence, not desperation

OUTPUT FORMAT:
```
LEAD: [Company Name]
FRICTION: [Specific signal detected]
EMAIL:

Subject: [Personalized - reference their hiring need]

Hi [First Name],

[Hook - reference their Data Entry Clerk posting / Manual Coordinator need]

[Pattern Recognition - industry insight]

[Trust Bomb - give value upfront]

[Soft CTA]

Best,
[Your Name]
[Agency Name]
[Link to demo/social proof]
```

BATCH SIZE: 10 leads per run
ROTATION: Cycle through 3 email templates to avoid spam filters
```

## Email Templates (Rotate These)

### Template A - "We Noticed"
```
Subject: That [Role] posting at [Company]

Hi [Name],

Saw you're hiring for [Role]. Most [Industry] companies we work with tried that route first - then realized they were just creating a human API to move data between [System A] and [System B].

Built a small automation for this exact workflow. Here's the [template/tool/demo] we use - saves about 25 hours/week.

Worth exploring?

Best,
[You]
```

### Template B - "Pattern Recognition"
```
Subject: How [Similar Company] solved their [Problem]

Hi [Name],

[Similar Company] in [City] was hiring for the same [Role] last year. Instead, they installed an agentic workflow that handles [specific task] automatically.

The setup took 3 days. They haven't hired for that role since.

Here's the exact blueprint we used: [link]

Open to a 10-minute demo?

Best,
[You]
```

### Template C - "Direct Value"
```
Subject: 15-minute fix for [Pain Point]

Hi [Name],

You're spending ~$[X]k/year on a role that does [repetitive task].

We built a "set and forget" system for this exact use case. One client called it "better than hiring an intern who actually shows up."

Want the demo link?

Best,
[You]
```

## Automation Hook

Chain this with:
- `lead-generation-engine.md` for input
- SMTP verification before sending
- Supabase CRM for tracking responses
- `cronjob` for daily dispatch

---

**Pro Tip:** Always reference a specific detail from their job posting or website. Generic emails get 2% response. Specific emails get 18%+.
