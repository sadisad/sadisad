<img src="./img/kaneki.webp" align="right" width="208" alt="Illustration"/>

# Irsyad Zulfikar

**AI engineer in Jakarta.** I build computer-vision and LLM systems that run in production, and I spend about as much time on their failure modes as on the models.

[Portfolio](https://www.zulfikarirsyad.my.id) · [LinkedIn](https://www.linkedin.com/in/irsyadzulfikar) · [Email](mailto:zulfikarirsyad@gmail.com)

### Now

AI Engineer at **ENB Mobile Care**: a six-model vision pipeline (detection, classification, segmentation) that grades smartphones and sets trade-in price, where one grade off costs real money. Most of the week goes to evaluation, GKE capacity, and inference observability rather than to the models themselves.

### Active projects

- **[LeafSentry AI](https://github.com/sadisad/leafsentry-ai)** — bean-leaf triage that abstains instead of guessing. Apache-2.0, [live demo](https://leafsentry.syd.my.id), [evaluation report](https://github.com/sadisad/leafsentry-ai/blob/main/docs/evaluation/README.md).
- **[deteksi-matajuling](https://github.com/sadisad/deteksi-matajuling)** — two-stage eye-screening prototype that abstains instead of guessing, with the rest of its limits written down.
- **[KenalinIkan](https://kenalinikan.id)** — Indonesian fish encyclopedia for markets and kitchens: 50 species with regional-name search, 50 recipes, a 21-province season map, and a yield/cost calculator for HoReCa. Next.js, PostgreSQL, PWA, read-only JSON API; pre-1.0 and adding species.
- **[Axiom Alpha](https://axiom-alpha.com)** — investment analysis platform on Django, deployed and maintained on one VPS.
- **[zulfikarirsyad.my.id](https://www.zulfikarirsyad.my.id)** — this site, Next.js with MDX.

<br clear="right"/>

---

## Writing

- [Hardening SIMBK: six gaps in the verification process](https://www.zulfikarirsyad.my.id/blog/simbk-hardening-audit) — a maintenance pass that found six defects in a production platform's own test and deploy checks, including a migration that could never have succeeded.
- [Building a 6-Model Ensemble for Smartphone Grading](https://www.zulfikarirsyad.my.id/blog/smartphone-grading-ensemble) — how the pipeline ended up after a year of iteration, including the bottleneck that was not the models.
- [Migrating from Docker Swarm to GKE: 5 Lessons from Production](https://www.zulfikarirsyad.my.id/blog/docker-swarm-to-gke) — per-microservice HPA tuning, VictoriaMetrics observability, and the cost-vs-latency tradeoff that nearly broke us.

## Evidence before adjectives

Anything I put in a README has to survive someone reading the code. That rule shapes how these projects are built:

- **Measurements carry their own scope.** LeafSentry's 96.875% top-1 on 128 pinned upstream test images is labelled model-level evidence, not field performance, in the repo and here.
- **A backup is not real until it has been restored.** Restore drills are scripted, run against a scratch target, and the last result is kept, local and offsite.
- **Guards get tested.** If a deploy path skips its migration, or a mutation forgets its audit write, CI fails before the release does. A check nobody verifies is a comment.
- **Defects go in the README.** [deteksi-matajuling](https://github.com/sadisad/deteksi-matajuling) used to turn "no boxes detected" into "normal, 100% confident". Its README now describes that defect, the abstention that replaced it, and what the decision layer still cannot tell you.
- **Hosts are default-deny.** Firewall allowlist, TLS with modern ciphers only, password-protected Redis with per-user ACLs, and SSH off the public interface wherever the migration is finished.

## Stack

<table>
  <tr>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/python/8b949e" width="44" alt="Python"/><br/>Python
    </td>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/typescript/8b949e" width="44" alt="TypeScript"/><br/>TypeScript
    </td>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/cplusplus/8b949e" width="44" alt="C++"/><br/>C++
    </td>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/postgresql/8b949e" width="44" alt="PostgreSQL"/><br/>PostgreSQL
    </td>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/pytorch/8b949e" width="44" alt="PyTorch"/><br/>PyTorch
    </td>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/opencv/8b949e" width="44" alt="OpenCV"/><br/>OpenCV
    </td>
  </tr>
  <tr>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/fastapi/8b949e" width="44" alt="FastAPI"/><br/>FastAPI
    </td>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/django/8b949e" width="44" alt="Django"/><br/>Django
    </td>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/docker/8b949e" width="44" alt="Docker"/><br/>Docker
    </td>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/kubernetes/8b949e" width="44" alt="Kubernetes"/><br/>Kubernetes
    </td>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/googlecloud/8b949e" width="44" alt="Google Cloud"/><br/>GCP
    </td>
    <td align="center" width="108">
      <img src="https://cdn.simpleicons.org/githubactions/8b949e" width="44" alt="GitHub Actions"/><br/>Actions
    </td>
  </tr>
</table>

Also in daily use: MLflow, DVC, Vertex AI, Grafana, VictoriaMetrics, MongoDB, Flask, Redis, nginx, Tailscale, UFW, fail2ban, CodeQL, Dependabot, Gitleaks.

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

---

[zulfikarirsyad@gmail.com](mailto:zulfikarirsyad@gmail.com) · [LinkedIn](https://www.linkedin.com/in/irsyadzulfikar) · [zulfikarirsyad.my.id](https://www.zulfikarirsyad.my.id)
