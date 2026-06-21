---
title: "The State of LLMs"
publishDate: 2026-06-21
description: "A post on my thoughts about the current LLM landscape"
tags: ["ai", "llm", "agents"]
draft: true
---

The LLMs are EVERYWHRE on the internet. People
use it for writing homework, documentation, some companies use it for charging a lot to write reports
like [Delloite](https://fortune.com/2025/10/07/deloitte-ai-australia-government-report-hallucinations-technology-290000-refund/) (6 months ago) provided a report with AI hallucinations to the Australian Government
and [KPMG](https://finance.yahoo.com/sectors/technology/articles/kpmg-drops-ai-report-false-093631620.html) pulled a report because of hallucinations in it.
This post is about AI/LLM is growing across the whole world

## Usage of AI

The usage of AI has grown at a pace never experienced on the internet, in [Google I/O 2026](https://blog.google/intl/en-in/company-news/technology/sundar-pichai-io-2026/#momentum), CEO of Google, Sundar Pichai, said AI measured by token usage, has grown from 9.7 trillion tokens in May 2024 to 480 trillion and then to 3.2 Quadrillion tokens in May 2026, that's 7 fold jump from 2025 to 2026. LLM usage does not seem to be going down at any noticeable rate. This is also primarily why the cost of hardware like RAM has gone up wayy too much,
LLMs require a lot of memory to hold the Embeddings, Key Value matrices, etc. Micron Technology, one of only 3 major consumer RAM suppliers shut down their consumer brand, Crucial
last year to cater to serving data centres. SK Hynix, another RAM supplier, announced bonuses of 400,000+ USD for it's workers due to LLM generated demand. The demand is so high that in December 2025, Samsung Semiconductor refsued to service an order made by Samsung Mobile Experience!.

> **Side Note:**
> Until Meta's Threads App came along, ChatGPT held the record of gaining 100 million Monthly Active Users the fastest, reaching it in 2 months after launch (Threads did it in 5 days). To put this in context, Tiktok took 9 months to reach 100 million and Netflix took 10 YEARS to do the same, granted they started at the very beginbing of the Internet.
> The point of this note is to show that LLM usage is not tied only to programming, even before anyone thought to generate code from an LLM, usage had blown up.

## The Data Problem

[Forbes](https://www.forbes.com/sites/joemckendrick/2026/04/14/ai-may-be-running-out-of-data-stanford-report-warns/) in this article talks about high quality training data
from the internet may be running out, a lot of synthetic data is being used now to train the LLMs, as in already trained LLMs are generating data to train new LLMs (this feels like a bad idea). This can cause somewhat of an echo chamber effect. [Epoch AI](https://epoch.ai/publications/will-we-run-out-of-data-limits-of-llm-scaling-based-on-human-generated-data)'s (research non-profit) states that we may run out of human generated text between 2026 and 2032.

## Internet Traffic

Matthew Prince, CEO of Cloudflare on June 03 2026, tweeted [Bot Traffic](https://x.com/eastdakota/status/2062212701414187452), he says due to agentic systems,
for the first time in history had exceeded human traffic

<iframe class="cf-radar-embed" width="800" height="447" src="https://radar.cloudflare.com/embed/BotHumanXY?theme=system&dateStart=2026-06-03&dateEnd=2026-06-10&ref=%2Ftraffic" title="Cloudflare Radar - Bot vs. Human" loading="lazy" style="border:0;max-width:100%;"></iframe>

Even GitHub has had problems dealing with this exponential growth in traffic, stated in April, [Github Blog](https://github.blog/news-insights/company-news/an-update-on-github-availability/). They have had multiple hour long incidents since then.
