# Shaugato Paroi

Systems engineer in Melbourne. I run identity and endpoint for a talent-acquisition SaaS company, and I write the software that runs it.

At work that means JumpCloud as our primary identity provider with SAML, OIDC and SCIM, alongside Microsoft 365, Entra ID and Google Workspace. Conditional Access co-owned with our security engineer. Mobile device management across Windows, macOS, iOS and Android. I am the only support engineer in a two-person internal IT team covering 250+ staff, so I own these systems end to end rather than a slice of them.

The code here came out of that job. Most of it follows one rule: the decision is deterministic and auditable, and the language model sits outside it.

## Projects

**[mainline](https://github.com/Shaugato/mainline)** · a permit-to-work system where the refusal lives in CockroachDB, not in application code, because a check in the app is one migration away from being bypassed. Seven named CHECK constraints, a PL/pgSQL trigger that re-derives the obligation count from base tables in case the counter was forged, and a composite foreign key that turns a late obligation into a referential integrity failure. 271 forward-only migrations building 86 tables, SERIALIZABLE isolation, row-level security, AWS Bedrock embeddings, Terraform for Lambda and IAM. You can try to defeat it over a public Lambda URL with no credentials.

**[find-evil](https://github.com/Shaugato/find-evil)** · autonomous DFIR for the SANS Find Evil hackathon, where the language model structurally cannot change a verdict. Dempster-Shafer evidence fusion decides with no model in the loop, Shapley attribution says which sensor moved the answer, and the narrator is a separate daemon that reads the result afterwards. Findings land in an append-only ledger signed with Ed25519 over deterministic canonical JSON. A custom MCP server exposes 62 typed tools with no raw shell anywhere. 97 tests, three of which assert the Shapley axioms.

**[AI-powered-DevOps-Agent](https://github.com/Shaugato/AI-powered-DevOps-Agent)** · AutoCloud, an AWS architecture advisor with a deterministic core. TOPSIS multi-criteria analysis ranks the design, not the model, with criterion weights derived from Well-Architected pillar priorities. Cross-account read-only discovery through STS AssumeRole, with an inline policy scoped to exactly the ten API calls the discovery code makes. Emits Terraform across 14 resource types. Demoed at GDG Melbourne.

**[kinesys](https://github.com/Shaugato/kinesys)** · real-time webcam pose control in about 6,500 lines of Rust. A lock-free triple buffer splits perception from rendering, and a committed log line shows it working: 31 Hz sustained while the render thread blocked for 252 ms. I chose the model by measuring and rejecting two candidates before shipping one that cleared the bar. Two-bone analytic inverse kinematics and YOLOX decode written by hand.

**[aether-energy](https://github.com/Shaugato/aether-energy)** · a home energy optimiser that will not trust its own solver. It builds a schedule twice, as a mixed integer program and as a greedy heuristic, re-simulates both, and accepts the MILP result only if it is no worse on peak load and on cost. Two tests lock that property.

**[citether-follow-me-power](https://github.com/Shaugato/citether-follow-me-power)** · a 3D simulation of solar credit that follows the person rather than the meter. Every on-screen figure derives from one deterministic model, so the scene, the ledger and the economics panel cannot disagree. Built after Watt The Hack 2026 and [deployed](https://citether-sim.vercel.app).

## What I work with

Identity and endpoint: JumpCloud, Microsoft 365, Entra ID, Google Workspace, Intune, Jamf, Conditional Access, SAML, OIDC, SCIM, MDM across Windows, macOS, iOS and Android.

Building: Python, Rust, TypeScript, PowerShell, Bash, PostgreSQL and CockroachDB, Terraform, Docker, AWS, FastAPI, React.

Certifications: AWS Certified Developer Associate, Cisco CCNA, CompTIA Security+, CompTIA Network+, Microsoft SC-900.

Bachelor of Computer Science, Swinburne University of Technology, majoring in cybersecurity and software development.

## Elsewhere

[LinkedIn](https://www.linkedin.com/in/shaugato-paroi-062401236/)
