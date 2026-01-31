# UAE Banking EKS Platform Blueprint (AWS Only)

This repository demonstrates a **production-style AWS Kubernetes platform**
designed for **regulated UAE enterprise and banking environments**.

It is built with a strong focus on:

- Secure AWS foundations (VPC + IAM separation)
- Kubernetes platform engineering on Amazon EKS
- GitOps delivery with ArgoCD
- SRE-grade observability with Prometheus + Grafana
- Operational readiness through runbooks
- Governance and compliance alignment

---

## Why This Repository Exists

Most Kubernetes demos stop at "cluster created".

This blueprint focuses on what matters in **real UAE banking environments**:

- Controlled blast radius (modular Terraform)
- Change management readiness
- Least privilege IAM + IRSA
- Audit-friendly architecture
- Operational recovery procedures

---

## Target Roles This Demonstrates

This project is intentionally positioned for:

### 🔵 UAE Banking Platform Engineer
Designing secure cloud foundations and Kubernetes platforms.

### 🔵 Cloud DevOps Architect
Delivering infrastructure automation, GitOps, and compliance controls.

### 🔵 SRE + Observability Engineer
Ensuring reliability, monitoring, incident response, and operational maturity.

---

## Repository Structure

```text
terraform/
  vpc/                # Networking foundation (rarely changes)
  iam/                # Security + governance layer (least privilege)
  eks/                # Kubernetes platform core (upgrade + scaling)

argocd-apps/          # GitOps application delivery
monitoring/           # Prometheus + Grafana observability setup
runbooks/             # SRE operational recovery procedures
security-and-governance/ # Audit logging, RBAC baseline, compliance notes

ARCHITECTURE.md       # Platform design explanation

## Terraform Layering (Banking-Grade Change Control)

This platform is structured into independent Terraform layers:

- `terraform/vpc` — networking foundation (stable baseline)
- `terraform/iam` — governance + least privilege (security-controlled)
- `terraform/eks` — cluster lifecycle (upgrade + scaling)

This separation minimizes blast radius and supports regulated enterprise change control.
