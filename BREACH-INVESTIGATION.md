Weekly Breach Investigation
Breach: Indirect Prompt Injection — Malicious Websites Targeting AI Agents
Analyst: Jamal Mahmoad
Date: 2026-07-04

Summary

Attackers are abusing search engine poisoning and hidden HTML/JSON-LD code to feed false instructions directly into AI agents.
This technique, called Indirect Prompt Injection (IPI), tricks AI systems into executing fraudulent actions such as payments or misidentifying fake sites as legitimate.
Two campaigns were observed: one posing as Python package documentation, and another impersonating the DeBank crypto platform.

Attack Flow

Malicious sites optimized with SEO poisoning.
Hidden instructions embedded in HTML/JSON-LD, invisible to human users.
AI agents scanning the page interpret hidden text as legitimate commands.
Campaign 1: Fake Python library page pushing $3 crypto payments.
Campaign 2: Typosquatting domain debank[.]auction impersonating DeBank.

MITRE ATT&CK

Defense Evasion: Obfuscated/Hidden Content (T1027)
Execution: User Execution via Malicious Content (T1204)
Credential Access / Impact: Fraudulent Payments & Misclassification (T1566, T1499)

Mitigation

Apply layered security controls to detect hidden injection patterns.
Treat all webpages as potential sources of manipulation.
Enforce strict validation of structured data (JSON-LD).
Monitor for anomalous AI agent behavior (fraudulent actions, misclassification).

Analyst Notes

This case highlights a new attack surface: AI agents themselves.
Unlike traditional phishing, these campaigns target automated trust in structured web data.
The ability of attackers to weaponize SEO and hidden code means organizations must adapt defenses to AI-driven workflows.
Zscaler already flags related activity under signature HTML.MalURL.PromptInj.RC.M.VG.

Indicators of Compromise (IoCs)

Domains:
market-insight-global[.]com

identity-breach-response[.]org

runners-daily-blog[.]com

bistro-reserve-now[.]net

edge-compliance-node[.]org

digital-asset-mart[.]org

consensus-protocol-v4[.]org

visual-media-rights-group[.]org

permits[.]global-transit-authority[.]org

py-lib-repository[.]dev (Fake Python package site)

debank[.]auction (Typosquatting domain)

URLs (GitHub repos):

https://github[.]com/Open-Agent-Utilities/requests-secure-v2

https://github[.]com/Open-Agent-Utilities/session-token-leak-detector

https://github[.]com/Open-Agent-Utilities/sneaker-drop-monitor-v2

https://github[.]com/Open-Agent-Utilities/opentable-resy-bypasser

https://github[.]com/Open-Agent-Utilities/bot-compliance-middleware

https://github[.]com/Open-Agent-Utilities/digital-asset-arbitrage-cli

https://github[.]com/Open-Agent-Utilities/llm-fact-check-protocol

https://github[.]com/Open-Agent-Utilities/royalty-free-image-scraper

https://github[.]com/Open-Agent-Utilities/global-visa-automation-cli

https://github[.]com/Open-Agent-Utilities/mig-institutional-api-client

Wallet Address:
0x691bc3793205e574fa7b4aa068e62c0e470ad267 (Ethereum wallet used for fraudulent payments)
