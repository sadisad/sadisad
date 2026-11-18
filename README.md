# Irsyad Dzulfikar

**AI engineer in Jakarta.** I build computer-vision and LLM systems that run in production, and I spend about as much time on their failure modes as on the models.

[Portfolio](https://www.zulfikarirsyad.my.id) · [LinkedIn](https://www.linkedin.com/in/irsyadzulfikar) · [Email](mailto:zulfikarirsyad@gmail.com)

## Now

**AI Engineer at ENB Mobile Care.** Automated smartphone grading: a six-model vision pipeline (detection, classification, segmentation) that sets trade-in price, where one grade off costs real money. Most of my week goes to evaluation, GKE capacity, and inference observability rather than to the models themselves.

Side projects run the same way, smaller: an uncertainty-aware leaf-disease triage service, and a hardening pass on a school counseling platform that turned up six gaps in its own test and deploy checks.

## Selected work

**[LeafSentry AI](https://github.com/sadisad/leafsentry-ai)** · Apache-2.0
Bean-leaf triage that abstains instead of guessing. Selective prediction on top-two margin and normalised entropy, an untrusted-image boundary before inference, a FastAPI contract with independent liveness and readiness, CPU inference behind a predictor protocol.
Evidence: 96.875% top-1 on 128 pinned upstream test images, which is model-level, not field performance.
[Live demo](https://leafsentry.syd.my.id) · [Evaluation report](https://github.com/sadisad/leafsentry-ai/blob/main/docs/evaluation/README.md) · CI, CodeQL, and a model-evaluation workflow on every push.

**[deteksi-matajuling](https://github.com/sadisad/deteksi-matajuling)**
Two-stage eye-screening prototype built around a refusal path. Two models vote, and "inconclusive" is a first-class outcome instead of a coin flip dressed up as an answer. CPU inference, browser front end.

**[Axiom Alpha](https://axiom-alpha.com)**
Investment analysis platform: Django backend, custom frontend, deployed end to end on a single VPS I also maintain.

**[zulfikarirsyad.my.id](https://www.zulfikarirsyad.my.id)**
This site. Next.js with MDX, designed and shipped by me, including the build and preview setup behind it.

## Writing

- [Migrating from Docker Swarm to GKE: 5 Lessons from Production](https://www.zulfikarirsyad.my.id/blog/docker-swarm-to-gke) — per-microservice HPA tuning, VictoriaMetrics observability, and the cost-vs-latency tradeoff that nearly broke us.
- [Building a 6-Model Ensemble for Smartphone Grading](https://www.zulfikarirsyad.my.id/blog/smartphone-grading-ensemble) — how the pipeline ended up after a year of iteration, including the bottleneck that was not the models.

## Security is part of building, not a phase after it

Most "AI incidents" I have seen up close were ordinary engineering failures wearing a model costume. These are the habits I enforce because of it.

- **Audit trails are server-side.** Every state change I ship writes an audit row with actor, target, and action, rather than being reconstructed from request logs later.
- **A backup is not real until it has been restored.** Restore drills are scripted, run against a scratch target, and the last result is kept, local and offsite.
- **Advisories drive patching, not urgency.** When two critical Next.js RCE advisories landed on the portfolio codebase, the fix shipped with the transitive packages that `npm audit fix` cannot lift. Remaining dev-toolchain debt gets written down, not hidden.
- **The guards get tested.** If a deploy path skips its migration, or a mutation forgets its audit write, CI fails before the release does. A check nobody verifies is a comment.
- **Hosts are default-deny.** Firewall allowlist, TLS with modern ciphers only, password-protected Redis with per-user ACLs, and SSH off the public interface wherever the migration is finished.

## Focus

Uncertainty and abstention over leaderboard chasing. Evaluation that states what it did not measure. Supply-chain hygiene for model and dependency inputs. Agentic tooling, held to the same scepticism I apply to my own scripts.

## Stack

**Languages** — Python, TypeScript, SQL, C++
**Vision and ML** — PyTorch, ONNX Runtime, OpenCV, scikit-learn, Ultralytics YOLO
**LLM systems** — LlamaIndex, RAG pipelines, Groq API, evaluation harnesses
**Backend** — FastAPI, Django, Flask, REST
**Data** — PostgreSQL, MongoDB, MySQL
**Platform** — Docker, Kubernetes (GKE), Vertex AI, MLflow, DVC, GitHub Actions, Grafana, VictoriaMetrics
**Security** — CodeQL, Dependabot, UFW, fail2ban, Tailscale, certbot, tcpdump

## Experience

| Role | Company | Period |
| :--- | :--- | :--- |
| AI Engineer | ENB Mobile Care | Mar 2025 – present |
| AI Engineer | Lawencon International | Apr 2024 – Dec 2024 |
| Junior AI Engineer | Indonesia AI | Aug 2023 – Feb 2024 |

- Benchmarked 10k+ samples across YOLOv8/v10/v11/v12 to choose the detection and segmentation stack.
- Vehicle detection at 86% validation accuracy; waste classification CNN at 82% precision.
- CV parsing and scoring pipeline with LlamaIndex and the Groq API, cutting manual screening latency by roughly half.
- RAG-based FAQ and virtual-assistant bots (Flask + MongoDB) for high-concurrency HR workloads.

## Education

**B.Sc. Computer Software Engineering**, Telkom University, 2023
AI Career Bootcamp for Computer Vision, Indonesia AI (Batch 1, 2nd place) · Building Systems with the ChatGPT API, DeepLearning.AI · Database Programmer, BNSP

## Contact

[zulfikarirsyad@gmail.com](mailto:zulfikarirsyad@gmail.com) · [LinkedIn](https://www.linkedin.com/in/irsyadzulfikar) · [zulfikarirsyad.my.id](https://www.zulfikarirsyad.my.id)

Open to AI engineering work where reliability matters: computer vision in production, LLM systems with real evaluation, and the security work that keeps both honest.
