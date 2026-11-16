# Helpdesk Cloud — Projet « Du code à la supervision » (BC3)

Application de tickets (front + API + worker + PostgreSQL + RabbitMQ + MinIO) avec toute la chaîne d'exploitation :
Docker, Kubernetes (Kustomize), Terraform, GitHub Actions, Prometheus/Grafana/Loki, sécurité ISO 27001, FinOps.

Démarrage : lire **LANCEMENT.md**, puis `./launch.sh help` (ou `./launch.sh all-local` pour tout enchaîner).

```
app/        backend (FastAPI), worker, frontend (Nginx + SPA)
k8s/        manifests Kustomize (base + overlays dev/prod/ci) et règles de supervision
terraform/  cluster/ (kind + registre) puis platform/ (ingress, quotas, supervision)
monitoring/ Prometheus, règles, dashboard Grafana (utilisés par compose et Kubernetes)
scripts/    déploiement, secrets, TLS, tests d'exploitation, FinOps
.github/    pipeline CI/CD, CODEOWNERS
```
