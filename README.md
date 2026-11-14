<h1>Hi, I'm Maikon Marquez 👋</h1>

**Cloud & DevOps Engineer · SRE** · AWS · Terraform · Kubernetes · Observability · CI/CD · Generative AI
📍 Uberlândia, Brazil · 🌎 Open to remote roles

I build and automate cloud infrastructure end to end: provisioning with **Terraform**, containerizing with **Docker**, orchestrating with **Kubernetes** and shipping through **GitHub Actions** pipelines. Lately I've been combining SRE with **Generative AI** on **Amazon Bedrock**: an agent that turns GitHub issues into pull requests inside a Fargate sandbox, and another that investigates incidents from SLO burn-rate alerts. In both, a human always approves.

- 🏆 Latest: [**AI Dev Agent**](https://github.com/MaikonJm/ai-dev-agent), a serverless agent that plans, waits for approval and opens pull requests; first run on AWS documented in a post-mortem
- 🧪 Before that: [**AWS SRE AI Platform**](https://github.com/MaikonJm/aws-sre-ai-platform), tested end to end with chaos experiments: 11 real bugs found and fixed, two post-mortems
- 🔭 Also building **HumanGov**, a multi-environment AWS platform with Terraform modules, remote state, Ansible, Docker and Kubernetes
- 🌱 Learning: **Azure** and **MLOps / LLMOps**
- ✍️ I document every project step by step on [Medium](https://medium.com/@maikonjm) (PT-BR)

---

### ⭐ Spotlight: AI Dev Agent

<a href="https://github.com/MaikonJm/ai-dev-agent"><img src="https://raw.githubusercontent.com/MaikonJm/ai-dev-agent/main/docs/images/cover.png" alt="AI Dev Agent" width="100%"></a>

An autonomous development agent on AWS. Label a GitHub issue, approve the plan it proposes, and it writes the code and the tests in an isolated **Fargate** sandbox and opens a pull request. It never merges: a human always decides.

- **Ran end to end on AWS:** plan in 9 s, pull request in 43 s with the correct fix, about US$ 0.23 in model spend, merged after human review
- **Six findings** that 78 passing unit tests could not see, fixed in their own PRs or documented in a blameless post-mortem
- **Serverless and 100% Terraform:** API Gateway, Lambda, SQS + DLQ, DynamoDB, ECS Fargate, Bedrock; no idle cost, 52 resources created and destroyed in one session

[Repository](https://github.com/MaikonJm/ai-dev-agent) · [Write-up on Medium (PT-BR)](https://medium.com/@maikonjm/meu-agente-de-ia-passou-em-78-testes-falhou-na-primeira-issue-real-6e09abd29dd6)

### ⭐ Spotlight: AWS SRE AI Platform

<a href="https://github.com/MaikonJm/aws-sre-ai-platform"><img src="https://raw.githubusercontent.com/MaikonJm/aws-sre-ai-platform/main/docs/images/cover.png" alt="AWS SRE AI Platform" width="100%"></a>

An order-processing platform on AWS that investigates its own incidents. When an SLO burn-rate alert fires, an AI agent collects read-only evidence from the cluster, asks **Amazon Bedrock** for the root cause and opens a GitHub issue with the fix. Nothing ships without human approval.

- **Chaos-tested on AWS:** API errors detected in 135 s, worker outage in 225 s (recovered in 45 s), poison messages in 150 s
- **11 real bugs** found by end-to-end tests, each fixed in its own PR and documented in two blameless post-mortems
- **100% Terraform**, GitHub Actions with OIDC (no keys), k3s on EC2, SQS + DLQ, Prometheus, Grafana; two test sessions for **US$ 1.17**

[Repository](https://github.com/MaikonJm/aws-sre-ai-platform) · [Write-up on Medium (PT-BR)](https://medium.com/@maikonjm/meu-agente-de-ia-errou-o-diagn%C3%B3stico-o-teste-de-caos-mostrou-por-qu%C3%AA-be4c60fb1d70)

### 🚀 Featured projects

| Project | What it shows | Stack |
|---|---|---|
| [**ai-dev-agent**](https://github.com/MaikonJm/ai-dev-agent) | Agent that turns a GitHub issue into a pull request after human approval, with guardrails enforced in code and an isolated sandbox per task | Terraform · AWS Lambda · Fargate · SQS · DynamoDB · Bedrock · Python |
| [**aws-sre-ai-platform**](https://github.com/MaikonJm/aws-sre-ai-platform) | SLOs with burn-rate alerts, chaos experiments and an AI SRE agent that opens incident issues for human approval | Terraform · AWS · Kubernetes · SQS · Prometheus · Grafana · Bedrock |
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
<img src="https://skillicons.dev/icons?i=aws,gcp&theme=dark" /> <br>
<img src="https://img.shields.io/badge/Lambda-FF9900?style=for-the-badge&logo=awslambda&logoColor=white" /> <img src="https://img.shields.io/badge/ECS_Fargate-FF9900?style=for-the-badge&logo=awsfargate&logoColor=white" /> <img src="https://img.shields.io/badge/API_Gateway-8C4FFF?style=for-the-badge" /> <img src="https://img.shields.io/badge/SQS-E7157B?style=for-the-badge" /> <img src="https://img.shields.io/badge/DynamoDB-4053D6?style=for-the-badge&logo=amazondynamodb&logoColor=white" />

**IaC & CI/CD** <br>
<img src="https://skillicons.dev/icons?i=terraform,ansible,githubactions,git,github&theme=dark" />

**Containers & OS** <br>
<img src="https://skillicons.dev/icons?i=docker,kubernetes,linux,ubuntu,bash&theme=dark" />

**Observability & SRE** <br>
<img src="https://skillicons.dev/icons?i=prometheus,grafana&theme=dark" /> <br>
<img src="https://img.shields.io/badge/SLOs_%26_error_budgets-0B1220?style=for-the-badge" /> <img src="https://img.shields.io/badge/Chaos_testing-DC2626?style=for-the-badge" /> <img src="https://img.shields.io/badge/Post--mortems-475569?style=for-the-badge" />

**Code, data & AI** <br>
<img src="https://skillicons.dev/icons?i=python,fastapi,mysql,postgres&theme=dark" /> <br>
<img src="https://img.shields.io/badge/Amazon_Bedrock-01A88D?style=for-the-badge&logo=amazonaws&logoColor=white" /> <img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white" /> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge&logo=qdrant&logoColor=white" /> <img src="https://img.shields.io/badge/RAG-6A1B9A?style=for-the-badge" /> <img src="https://img.shields.io/badge/Open_WebUI-1F2937?style=for-the-badge" />

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
