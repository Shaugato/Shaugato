# Shaugato Paroi

IT Operations Administrator at Airlock Digital in Melbourne, and a research master's student at Victoria University. In my own time I build AI agents and LLM applications in Python, mostly with LangGraph, Amazon Bedrock and MCP.

Most of these projects follow one rule. Rules or the database make the decision, and the language model sits outside it. I build them with Claude Code, working from a written spec and reviewing what the agents produce.

## Projects

**[mainline](https://github.com/Shaugato/mainline)** · a permit-to-work database built for the CockroachDB and AWS hackathon (Aug 2026). The database will not issue a permit until a qualified person signs off every past incident linked to it, so an app cannot skip the check. Amazon Bedrock Titan embeddings are searched through a CockroachDB vector index, and every Claude call in the pipeline returns schema-checked JSON with no tools attached. Terraform deployed the demo to AWS Lambda with a cost guard. The hosted demo is offline now, and a three-minute demo video is linked in its README.

**[job-application-agents](https://github.com/Shaugato/job-application-agents)** · a LangGraph multi-agent system that reads public job feeds, picks the ads that fit, and drafts a tailored resume and cover letter for each one. A coordinator agent decides whether a job is worth pursuing, then the writing and checking agents run on Claude Haiku or Sonnet. Every application stops for my approval, and nothing is sent to an employer.

**[find-evil](https://github.com/Shaugato/find-evil)** · Stigmergy, a local forensics system built for the SANS Find Evil! hackathon (Jun 2026). Dempster-Shafer evidence fusion makes the threat decision with no model call in that path. A prosecutor, defence and judge debate in LangGraph, on a local Llama 3.2 3B model, reviews contested findings. An MCP server exposes 62 tools and no shell tool.

**[damdays](https://github.com/Shaugato/damdays)** · built in 60 hours for Climate Hack-tion 2026. It uses satellite records to give a cautious minimum count of days before a farm dam runs low. I wrote the test rules before the build began, then scored the frozen model once on a region held back with SHA-256 fingerprints. It met all 4 pass marks. [Live app](https://shaugato.github.io/damdays/app/).

**[AI-powered-DevOps-Agent](https://github.com/Shaugato/AI-powered-DevOps-Agent)** · AutoCloud, an AWS architecture assistant I demoed at GDG Melbourne. Weighted scoring rules (TOPSIS) choose the design, read-only discovery of an existing account goes through STS AssumeRole, and it writes draft Terraform for 14 resource types. Deployment stops at terraform plan until an operator approves.

## What I work with

AI and agents: LangGraph, Amazon Bedrock, Claude Agent SDK, OpenAI API, MCP, Pydantic structured outputs, retrieval with embeddings and vector search.

Building: Python, SQL, TypeScript, PostgreSQL and CockroachDB, FastAPI, Docker, AWS, Terraform.

Identity and operations: JumpCloud, Google Workspace, Microsoft 365, SAML, OIDC, SCIM.

Certifications: AWS Certified Developer (Associate), CompTIA Security+, Microsoft SC-900.

## Elsewhere

[LinkedIn](https://www.linkedin.com/in/shaugato-paroi-062401236/)
