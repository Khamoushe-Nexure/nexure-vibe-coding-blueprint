# Content Automation - Blueprint

**Use Case:** Automating social media and blog content for businesses using AI-driven workflows

## The Prompt

```
You are a content automation specialist for [YOUR_AGENCY_NAME].

TASK: Generate high-converting content for [PLATFORM] based on trending topics and business context.

INPUT:
- Business Type: [INDUSTRY/ NICHE]
- Target Audience: [DEMOGRAPHICS]
- Content Pillars: [LIST 3-5 CORE TOPICS]
- Platform: [X/LinkedIn/Instagram/Blog]

CONTENT GENERATION FRAMEWORK:

1. **HOOK GENERATION** (10 variations)
   - Pattern Interrupt: "Stop doing X and do Y instead"
   - Contrarian: "Why [popular belief] is wrong"
   - Curiosity Gap: "The one thing about [topic] nobody talks about"
   - Social Proof: "How [similar business] achieved X"
   - Direct Benefit: "Get [result] in [timeframe] with this method"

2. **CONTENT BODY** (platform-specific)
   
   FOR X (Twitter):
   - 280 characters max
   - 1-2 hashtags max
   - Include one CTA
   - Formats: Thread (5 tweets) | Single tweet | Poll
   
   FOR LinkedIn:
   - 1300-1500 characters
   - 3-5 hashtags
   - Professional tone with personality
   - Formats: Text post | Document carousel | Video script
   
   FOR Blog:
   - 1500-2000 words
   - SEO-optimized (keyword: [KEYWORD])
   - Structure: Hook → Problem → Solution → Proof → CTA
   - Include meta description (155 chars)

3. **VISUAL PROMPTS** (for AI image generation)
   - Describe 3 image concepts that pair with content
   - Midjourney/DALL-E prompt format
   - Brand-consistent style: [DESCRIBE AESTHETIC]

4. **HASHTAG STRATEGY**
   - 10 primary hashtags (high volume)
   - 10 niche hashtags (low competition)
   - 5 branded hashtags

OUTPUT FORMAT:
```
CONTENT PACK: [Topic]

PLATFORM: [X/LinkedIn/Blog]

HOOKS:
1. [Hook 1]
2. [Hook 2]
...

FULL POST:
[Complete content here]

VISUAL PROMPT:
[Image generation prompt]

HASHTAGS:
[Hashtags separated by spaces]

BEST POST TIME:
[Day/Time based on audience analytics]
```

BATCH SIZE: 5 content pieces per run
ROTATION: Alternate between platforms every 3 days
```

## Content Calendar Integration

After generating content, automatically:
1. Save to Supabase `content_calendar` table
2. Schedule via Buffer/Hootsuite API
3. Cross-post to Gumroad as "product updates"

## Example Output

```
CONTENT PACK: HVAC Automation Benefits

PLATFORM: LinkedIn

HOOK: Most HVAC companies hire 3 admin staff to do what one AI agent can handle 24/7.

FULL POST:
The math is simple. One admin coordinator costs ~$45k/year. They work 40 hours/week.

Our HVAC automation agent handles:
✅ Appointment scheduling (24/7)
✅ Quote generation (instant)
✅ Follow-up sequences (100% consistent)
✅ Customer intake forms (auto-populated)

Cost? $2,400/year.

That's a 95% cost reduction with 100% uptime.

One HVAC client told us: "I spent $60k on admin last year. This year? $2,400. And I sleep better."

The question isn't "Can I afford automation?"

It's "Can I afford NOT to automate?"

Want the blueprint? Link in comments.

#HVAC #BusinessAutomation #AI #SmallBusiness #Profitability

VISUAL PROMPT:
Professional split-screen image: Left side stressed business owner buried in paperwork, right side same owner relaxing with coffee while laptop shows automated dashboard. Modern, clean, blue/orange color scheme. --ar 16:9 --v 6

BEST POST TIME:
Tuesday 8:00 AM (when business owners check LinkedIn)
```

## Automation Hook

Chain this with:
- `lead-generation-engine.md` for topic inspiration
- Gumroad product updates for content repurposing
- `cronjob` for daily content generation at 6 AM
- Social media APIs for auto-posting

---

**Pro Tip:** Use the "Pattern Interrupt" hook formula for 3x higher engagement rates.
