# 🚀 Serverless Full-Stack DevSecOps Cloud Resume

A production-ready, full-stack serverless web application engineered to host a live professional portfolio. Built entirely under corporate environment constraints using cloud-native services, automated delivery pipelines, and hardened DevSecOps configurations.

👉 **Live Application Link:** [https://brandonresume2026.z13.web.core.windows.net/](https://brandonresume2026.z13.web.core.windows.net/)

---

## 🛠️ The Tech Stack

| Layer | Technology | Service Model |
| :--- | :--- | :--- |
| **Frontend Hosting** | Azure Blob Storage | Static Web Hosting |
| **API/Compute Tier** | Python / Azure Functions | Serverless (Flex Consumption Plan) |
| **Database/Storage** | Azure Cosmos DB | NoSQL (Serverless Capacity Mode) |
| **CI/CD Pipeline** | GitHub Actions | GitOps Automation |
| **Logic/Frontend Integration** | JavaScript (Fetch API) | Client-side Execution |

---

## 📐 Architecture Overview

```text
[ Visitor Browser ] 
        │
        ├──► (HTTPS) ──► [ Azure Blob Storage ] ($web static frontend bundle)
        │
        └──► (Fetch API) ──► [ Azure Functions API ] (Python Serverless Tier)
                                    │
                                    └──► (Cosmos SDK) ──► [ Azure Cosmos DB ] (NoSQL State Persistence)

```

1. Frontend: Client loads static HTML/CSS assets securely streamed over HTTPS from an optimized Azure Storage container.

2. API Trigger: Client-side JavaScript fires an asynchronous DOM payload retrieval request to the backend.

3. Database Transaction: The serverless Python function invokes the Cosmos SDK client via connection strings stored inside secure runtime environment flags, securely reading, incrementing, and updating the database document counter.

4. Data Return: The API updates state, structuring an integer payload inside a JSON block accompanied by explicit cross-origin policy safety values.

🔒 Hardening & Security Implementation (DevSecOps)
This architecture applies industry-standard security principles to defend serverless resources against deployment and runtime vulnerabilities:

1. MITRE T1552 Mitigation (Unsecured Credentials): Absolute separation of logic and credentials. Zero connection strings or primary access keys are hardcoded in source control. Infrastructure handles backend connection strings via native application flags, while the delivery platform injects continuous deployment variables dynamically through GitHub Encrypted Secrets (AZURE_STORAGE_CONNECTION_STRING).

2. CORS Domain Defense: The Python serverless backend configuration utilizes hardened Cross-Origin Resource Sharing (CORS) headers, completely restricting unauthorized domains from forging cross-site request transactions or manipulating database metrics.

3. Least Privilege Identity Management: Deployments run isolated automation routines restricting broader platform control planes to target specific application resource footprints.

⚡ Engineering Breakthroughs under Constraints
1. Navigating Bleeding-Edge Platform Architecture Changes: Built during the global rollout of Azure's next-generation Flex Consumption serverless tier. This modern architecture decouples legacy local UI tooling runtimes. Standard portal-based graphical updates were unavailable.

2. Bypassing Environment Restrictions via Azure Cloud Shell: Restricted local terminal access on production devices prohibited traditional tooling. Solved this constraint by engineering completely within the browser using Azure Cloud Shell, managing workspace state, and packaging deployment payload dependencies cleanly via the Azure CLI zip-stream module.

3. GitOps CI/CD Automation: Standardized infrastructure delivery through a complete GitHub Actions automation model, executing automatic code checks and batch streaming production updates cleanly on active repository pushes.

📁 Repository Blueprint
```text
├── .github/workflows/
│   └── frontend-deploy.yml    # GitHub Actions CI/CD automation pipeline configuration
├── index.html                  # Core resume portfolio structural asset with embedded counter driver
├── style.css                   # Responsive layout visual presentation engine
└── README.md                   # Technical breakdown, architectural mapping, and asset catalog
```
💡 Engineered as part of the Azure Cloud Resume Challenge to demonstrate advanced competencies in cloud infrastructure design, serverless software configurations, and continuous deployment automation pipelines.
