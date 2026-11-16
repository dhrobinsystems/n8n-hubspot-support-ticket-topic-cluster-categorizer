# ⚠️ Disclaimer & Liability Limitation

**Use at your own risk.** The code, workflows, and scripts in this repository (`n8n-hubspot-support-ticket-topic-cluster-categorizer`) are provided for educational and architectural demonstration purposes.

## No Liability

The author and dhRobin Systems accept no responsibility or liability for any direct, indirect, incidental, or consequential damages that result from using, misusing, or deploying these scripts. This includes, without limitation, regulatory fines or claims arising from sending support data to an AI provider, misclassified or mis-prioritised tickets, missed product or security issues, overwritten or incorrect ticket properties, LLM charges or quota exhaustion, unintended disclosure of customer or support information, and service interruptions.

## No Warranty

All software, n8n JSON blueprints, JavaScript modules and prompts are provided "AS IS", without warranty of any kind, express or implied. This includes, but is not limited to, warranties of merchantability, fitness for a particular purpose, and non-infringement.

No warranty is given that any LLM or NLP provider returns accurate, consistent or unbiased categories, clusters, sentiment, priorities or summaries; that redaction removes every item of personal or confidential data (pattern redaction does not detect names, addresses or free-form identifiers); that cluster merging groups tickets correctly; that protected-diff rules preserve every value you consider valid; or that the integrity guards and circuit breaker prevent every unintended write.

## Production Testing Required

Always test thoroughly in an isolated staging environment, such as a HubSpot developer test account or sandbox, with `SANDBOX_MODE=true`, `DRY_RUN=true` and `SYNC_TO_HUBSPOT=false` enabled, before you connect live HubSpot or LLM credentials. Enable the live LLM, ticket writes and webhook processing one step at a time, start with a small `MAX_TICKETS_PER_RUN`, inspect the redacted LLM input, and confirm that a repeated run makes no new LLM calls before you activate the schedule.

Treat every generated category, cluster, sentiment, priority and summary as triage assistance that a person must be able to review and correct before it's relied on for product or support decisions.

## Third-Party APIs & Compliance

You alone are responsible for complying with the terms of service, rate limits, data privacy regulations (GDPR/CCPA and equivalents), and security policies of HubSpot, your LLM or NLP provider, and any connected services. That includes:

- confirming a lawful basis, and contractual permission under customer agreements, for sending support ticket content to an AI provider;
- executing a data processing agreement with the provider and reviewing its retention, training, sub-processor and international transfer terms;
- extending `REDACT_TERMS`, limiting `MAX_TEXT_CHARS`, and excluding pipelines that carry regulated data;
- keeping personal data out of product-feedback digests and any system they are forwarded to;
- limiting access to n8n execution data, which can contain ticket text, and applying a retention period that matches your policies;
- securing, rotating and restricting access to the HubSpot private app token, the HubSpot app client secret and the LLM API key;
- reviewing every automatically created or updated record.

## No Affiliation

HubSpot, OpenAI and n8n are trademarks of their respective owners. This project is independent and is not affiliated with, endorsed by, or sponsored by any of them. All tickets, customers, identifiers and text in the fixtures and pinned data are fictitious.

## Not Professional Advice

Nothing in this repository constitutes legal, privacy, security, or financial advice. Consult qualified professionals, including your data protection officer, for your specific circumstances.

---

Released under the MIT License. Copyright (c) 2026 DH Robin (dhRobin Systems). See [LICENSE](LICENSE).

Full text: DISCLAIMER.md · Licensed under the MIT License. License: MIT © 2026 dhRobin Systems · Provided as-is, see the disclaimer.
