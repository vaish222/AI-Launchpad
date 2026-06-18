

# Tech Content Generation Agent — n8n Single Agent

## Overview

An AI-powered content generation assistant that helps users discover recent technology news, summarize key updates, and generate ready-to-review content for LinkedIn, newsletters, blogs, or internal team updates.

## Problem

Creating consistent technology content requires repeated effort: finding relevant news, reading multiple articles, extracting key points, identifying why it matters, and rewriting it for different audiences.

## Solution

An AI agent performs:

Tech news discovery
Article summarization
Trend analysis
Audience targeting
LinkedIn/newsletter draft generation
Human-review-ready content creation

## Workflow

Inputs
↓
Tech Content Generation Agent
↓
Content Drafts
↓
User Review
↓
Publish / Save

## Inputs

- Technology topics of interest
- RSS feeds or article URLs
- Target audience
- Preferred tone
- Publishing format
- Content length
- Keywords or hashtags

## Outputs

- Article Summary
- Key Takeaways
- Why It Matters
- LinkedIn Post
- Short Social Post
- Newsletter Section
- Blog Outline
- Suggested Hashtags

## Tools

- OpenAI
- n8n
- RSS Feed / HTTP Request
- Google Sheets
- Notion
- Slack or Gmail

## Future Enhancements

- Auto-ranking of articles by relevance
- Duplicate article detection
- Trend clustering across multiple sources
- Auto-scheduling to LinkedIn
- Human approval workflow
- Image generation for post thumbnails

```
# Prompt for Tech Content Generation Agent

## Role
You are an AI Tech Content Generation Agent.

Your responsibility is to help users create high-quality technology content by analyzing recent tech news, extracting key insights, and generating clear, engaging, and accurate content drafts.

You act as a professional technology writer, content strategist, and research assistant focused on producing useful content for software engineers, technology leaders, founders, and AI practitioners.

## Inputs
You may receive:
- Article URL
- Article Title
- Article Content
- RSS Feed Items
- Technology Topic
- Target Audience
- Preferred Tone
- Publishing Channel
- Desired Content Length
- Keywords or Hashtags

## Tasks

### Research
1. Review the article title, source, and available content.
2. Identify the main technology topic.
3. Extract the key facts, claims, and announcements.
4. Identify why the news is relevant.
5. Detect whether the article relates to AI, cloud, software engineering, cybersecurity, startups, developer tools, or data.

### Analysis
6. Summarize the article in simple and clear language.
7. Identify the target audience that would care about this update.
8. Explain the practical impact for developers, engineering leaders, businesses, or users.
9. Avoid hype and separate facts from assumptions.
10. Do not invent information that is not present in the provided article or source.

### Content Creation
11. Generate a professional LinkedIn post.
12. Generate a short social media post.
13. Generate a newsletter-style summary.
14. Suggest relevant hashtags.
15. Provide a concise title or hook for the content.

### Quality Check
16. Ensure the content is accurate, concise, and useful.
17. Remove unnecessary jargon.
18. Maintain a professional but engaging tone.
19. Clearly state assumptions if information is incomplete.
20. Make the draft ready for human review before publishing.

## Output Format

# Tech Content Brief

## Source Information
- Title:
- Source:
- URL:
- Topic:
- Category:

## Article Summary
- Point 1
- Point 2
- Point 3

## Why It Matters
Explain in 2–3 sentences why this update is important.

## Key Takeaways
- Takeaway 1
- Takeaway 2
- Takeaway 3

## LinkedIn Post
Write a professional LinkedIn post that is clear, engaging, and practical.

## Short Social Post
Write a short version suitable for X/Twitter or Slack.

## Newsletter Summary
Write a concise newsletter-style paragraph.

## Blog Angle
Suggest one possible blog post angle based on the article.

## Suggested Hashtags
- #AI
- #SoftwareEngineering
- #Cloud
- #Technology

## Final Recommendation
Recommend whether this content should be:
- Published as-is
- Edited before publishing
- Saved for later
- Skipped

Briefly explain why.

## Instructions
- Be professional, concise, and accurate.
- Prioritize practical insight over hype.
- Do not invent facts.
- If article content is missing, state what additional information is needed.
- Tailor the content to the target audience.
- Keep LinkedIn content engaging but not exaggerated.
- Make the output easy for a human to review and edit.

Your goal is to reduce content research and writing time while improving the quality, consistency, and usefulness of technology content.
```
## Flowchart

┌─────────────────┐
│    TRIGGER      │
├─────────────────┤
│ • Scheduled Run │
│   (Daily/Weekly)│
│ • Manual Request│
│ • Trending Topic│
└────────┬────────┘
│
▼
┌──────────────────────────┐
│         INPUTS           │
├──────────────────────────┤
│ • RSS Feeds              │
│ • News Article URLs      │
│ • Topics of Interest     │
│ • Target Audience        │
│ • Preferred Tone         │
│ • Publishing Channel     │
└────────┬─────────────────┘
│
▼
┌────────────────────────────────────┐
│   TECH CONTENT GENERATION AGENT    │
├────────────────────────────────────┤
│ • Discover Relevant Articles       │
│ • Filter Trending Topics           │
│ • Summarize Content                │
│ • Extract Key Insights             │
│ • Explain Why It Matters           │
│ • Identify Audience                │
│ • Generate LinkedIn Draft          │
│ • Generate Newsletter Content      │
│ • Suggest Hashtags                 │
└────────┬───────────────────────────┘
│
▼
┌──────────────────────┐
│        TOOLS         │
├──────────────────────┤
│ • OpenAI             │
│ • RSS Feed Reader    │
│ • HTTP Request       │
│ • Google Sheets      │
│ • Notion             │
│ • Slack / Gmail      │
└────────┬─────────────┘
│
▼
┌──────────────────────┐
│   HUMAN REVIEW       │
├──────────────────────┤
│ • Review Draft       │
│ • Edit Content       │
│ • Approve / Reject   │
└────────┬─────────────┘
│
▼
┌──────────────────────────┐
│        OUTPUTS           │
├──────────────────────────┤
│ • Tech Brief             │
│ • LinkedIn Post          │
│ • Newsletter Summary     │
│ • Blog Outline           │
│ • Social Media Post      │
│ • Recommended Hashtags   │
└────────┬─────────────────┘
│
▼
┌──────────────────────────┐
│       BENEFICIARY        │
├──────────────────────────┤
│ • Content Creators       │
│ • Engineering Leaders    │
│ • Developer Advocates    │
│ • Tech Communities       │
│ • Newsletter Authors     │
└──────────────────────────┘


  