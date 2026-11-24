<h1>Hi, I'm Maikon Marquez 👋</h1>

**Cloud & DevOps Engineer · SRE** · AWS · Terraform · Kubernetes · Observability · CI/CD · Generative AI
📍 Uberlândia, Brazil · 🌎 Open to remote roles

I build and automate cloud infrastructure end to end: provisioning with **Terraform**, containerizing with **Docker**, orchestrating with **Kubernetes** and shipping through **GitHub Actions** pipelines. Lately I've been combining SRE with **Generative AI**: AI agents on **Amazon Bedrock** that investigate and fix incidents or write code, always behind guardrails written in code, not in prompts.

- 🏆 Latest: [**Autonomous SRE Agent**](https://github.com/MaikonJm/autonomous-sre-agent), a team of 7 AI agents that detects, fixes, verifies and documents incidents on its own: ~1–3 min MTTR, US$0.0002 of LLM per incident
- 🤖 Also new: [**AI Dev Agent**](https://github.com/MaikonJm/ai-dev-agent), an agent that turns a GitHub issue into a tested pull request in an isolated Fargate sandbox, with a human approving the plan and the merge
- 🔭 Also building **HumanGov**, a multi-environment AWS platform with Terraform modules, remote state, Ansible, Docker and Kubernetes
- 🌱 Learning: **Azure** and **MLOps / LLMOps**
- ✍️ I document every project step by step on [Medium](https://medium.com/@maikonjm) (PT-BR)

---

### ⭐ Spotlight: Autonomous SRE Agent

<a href="https://github.com/MaikonJm/autonomous-sre-agent"><img src="https://raw.githubusercontent.com/MaikonJm/autonomous-sre-agent/main/docs/img/capa.png" alt="Autonomous SRE Agent" width="100%"></a>

The next step after [AWS SRE AI Platform](https://github.com/MaikonJm/aws-sre-ai-platform): there the agent diagnosed and a human applied the fix; here a **team of agents closes the loop**. An Investigator (code) gathers evidence, a Diagnostician (LLM) proposes one action from a closed catalog, a Safety Reviewer (LLM) can veto it, a **policy written in code** makes the final call, and the fix only counts once the SLO is back. A Scribe agent writes the post-mortem.

- **4 of 5 failure scenarios fixed with no human**; in the 5th the Reviewer vetoed and escalated, which is the safe behavior
- **MTTD 92 s, MTTR 170 s on average** (best case 62 s), **US$0.00112** of LLM for the whole test run on Bedrock Nova Micro
- **No inbound ports** (SSM only), signed images with **AWS Signer** verified before deploy, NetworkPolicy, least-privilege RBAC, CI with 32 tests, PromQL validation, Semgrep and Trivy as gates

[Repository](https://github.com/MaikonJm/autonomous-sre-agent) · [Write-up on Medium (PT-BR)](https://medium.com/@maikonjm)

### 🤖 Also new: AI Dev Agent

<a href="https://github.com/MaikonJm/ai-dev-agent"><img src="https://raw.githubusercontent.com/MaikonJm/ai-dev-agent/main/docs/images/cover.png" alt="AI Dev Agent" width="100%"></a>

Label a GitHub issue and the agent comments a plan; after `/approve`, it writes the code and the tests in an isolated **Fargate** sandbox and opens a pull request with a report of what changed, how it was tested, tokens and cost. It never merges.

- **Tested end to end on AWS:** plan in 9 s (Claude Haiku 4.5, US$0.015), [PR](https://github.com/MaikonJm/agent-sandbox-shop/pull/4) in 43 s (Claude Sonnet 4.6, US$0.21), reviewed and merged by a human
- **6 problems found on the first real run** that 78 passing unit tests and `terraform validate` could not see, documented in a [post-mortem](https://github.com/MaikonJm/ai-dev-agent/blob/main/docs/postmortems/2026-11-13-first-test-session.md)
- **Serverless with zero idle cost:** API Gateway, Lambda, SQS, DynamoDB and Fargate, 52 resources in Terraform; command allowlist, no shell, per-task cost cap

[Repository](https://github.com/MaikonJm/ai-dev-agent) · [Sandbox repo it works on](https://github.com/MaikonJm/agent-sandbox-shop)

### 🚀 Featured projects

| Project | What it shows | Stack |
|---|---|---|
| [**autonomous-sre-agent**](https://github.com/MaikonJm/autonomous-sre-agent) | A team of AI agents that fixes incidents on its own: the AI proposes, another AI reviews, code decides; signed images, SLO-verified fixes, post-mortems | Terraform · AWS · k3s · Bedrock · Prometheus · Grafana · AWS Signer |
| [**ai-dev-agent**](https://github.com/MaikonJm/ai-dev-agent) | Issue → approved plan → tested PR, written by an AI agent in an isolated Fargate sandbox; a human always merges | Terraform · Lambda · SQS · DynamoDB · Fargate · Bedrock (Claude) |
| [**aws-sre-ai-platform**](https://github.com/MaikonJm/aws-sre-ai-platform) | SLOs with burn-rate alerts, chaos experiments (11 real bugs found, two post-mortems) and an AI SRE agent that opens incident issues for human approval | Terraform · AWS · Kubernetes · SQS · Prometheus · Grafana · Bedrock |
| [**cloud-ai-local-rag**](https://github.com/MaikonJm/cloud-ai-local-rag) | Local AI assistant with RAG: document ingestion, OCR, auto-classification and semantic search, served through an OpenAI-compatible API | Docker Compose · FastAPI · Ollama · Qdrant · Tesseract |
| [**kubernetes-project**](https://github.com/MaikonJm/kubernetes-project) | App deployment on Kubernetes with Ingress, ConfigMaps, Secrets and Horizontal Pod Autoscaler | Kubernetes · Minikube/Kind |
| [**workflow-cicd-github-actions**](https://github.com/MaikonJm/workflow-cicd-github-actions) | CI pipeline running automated tests and Docker image build on every push | GitHub Actions · Docker · Node.js |
| [**multi-conteiner-app**](https://github.com/MaikonJm/multi-conteiner-app) | 3-tier app (frontend, API, database) orchestrated with Docker Compose and built in CI | Docker · Spring Boot · React · PostgreSQL |

<!-- Adicionar quando estiverem públicos:
| [**human-gov-infrastructure**](https://github.com/MaikonJm/human-gov-infrastructure) | Reusable Terraform modules per environment, S3 remote state with locking, CI plan on PRs | Terraform · AWS · GitHub Actions |
| [**aws-ecommerce-iac**](https://github.com/MaikonJm/aws-ecommerce-iac) | Magento stack on AWS provisioned by Terraform and fully configured by Ansible | Terraform · Ansible · AWS |
-->

---

### 🛠️ Tech stack

**Cloud** <br>
<img src="https://skillicons.dev/icons?i=aws,gcp&theme=dark" />

**IaC & CI/CD** <br>
<img src="https://skillicons.dev/icons?i=terraform,ansible,githubactions,git,github&theme=dark" />

**Containers & OS** <br>
<img src="https://skillicons.dev/icons?i=docker,kubernetes,linux,ubuntu,bash&theme=dark" />

**Observability & SRE** <br>
<img src="https://skillicons.dev/icons?i=prometheus,grafana&theme=dark" /> <br>
<img src="https://img.shields.io/badge/SLOs_%26_error_budgets-0B1220?style=for-the-badge" /> <img src="https://img.shields.io/badge/Chaos_testing-DC2626?style=for-the-badge" /> <img src="https://img.shields.io/badge/Post--mortems-475569?style=for-the-badge" /> <img src="https://img.shields.io/badge/Supply_chain_signing-1E40AF?style=for-the-badge" />

**Code, data & AI** <br>
<img src="https://skillicons.dev/icons?i=python,fastapi,mysql,postgres&theme=dark" /> <br>
<img src="https://img.shields.io/badge/Amazon_Bedrock-01A88D?style=for-the-badge&logo=amazonaws&logoColor=white" /> <img src="https://img.shields.io/badge/Multi--agent_systems-7C3AED?style=for-the-badge" /> <img src="https://img.shields.io/badge/LLM_guardrails-0F766E?style=for-the-badge" /> <img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white" /> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge&logo=qdrant&logoColor=white" /> <img src="https://img.shields.io/badge/RAG-6A1B9A?style=for-the-badge" /> <img src="https://img.shields.io/badge/Open_WebUI-1F2937?style=for-the-badge" />

**Learning** <br>
<img src="https://skillicons.dev/icons?i=azure&theme=dark" />

---

### 🎓 Education & training

<!-- Adicionar a pós-graduação: - <Curso> — <Instituição> (<ano>) -->
- The Cloud Bootcamp: **AWS** (completed) · **DevOps Cloud** (in progress)

---

### 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/maikon-marquez)
[![Medium](https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@maikonjm)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:maikonjm@gmail.com)
