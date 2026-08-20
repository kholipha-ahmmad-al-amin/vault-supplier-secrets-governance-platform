# Vault Supplier Secrets Governance Platform
## The Problem
Supplier credentials create security exposure when leases, reviews, and rotations lack accountable controls.
## The Solution
This service governs supplier secret leases through registration, approval, controlled rotation, and audit evidence using Vault-oriented patterns.
## Live Demo & Tech Stack
The service binds to `0.0.0.0:22000`. The stack uses Node.js, Vault governance patterns, Express, Vitest, and GitHub Actions.
## Local Setup & Run Instructions
```bash
npm install
npm test
npm start
```
## System Documentation (Mermaid.js)
### System Architecture Diagram
```mermaid
flowchart LR
  Engineer-->Service[Secrets governance service]
  Governor-->Service
  Operator-->Service
```
### Entity-Relationship Diagram
```mermaid
erDiagram
  SECRET_LEASE ||--o{ AUDIT_EVENT : records
  SECRET_LEASE { string id string supplier int ttl string state }
```
### Data Flow Diagram
```mermaid
flowchart TD
  Register-->Approve-->Rotate-->Audit
```
### Use Case Diagram
```mermaid
flowchart LR
  Engineer-->RegisterSecret
  Governor-->ApproveSecret
  Operator-->RotateSecret
```
### Sequence Diagram
```mermaid
sequenceDiagram
  participant E as Engineer
  participant S as Secrets service
  participant O as Operator
  E->>S: Register lease
  O->>S: Rotate lease
```
## Owner
Created and maintained by Kholipha Ahmmad Al-Amin.
Software Engineer and AI Specialist
Founder and CEO of EquiSaaS BD
Principal Consultant at AR IT Consultancy
Full Stack Developer and SaaS Product Builder
### Official links
Portfolio: https://kholipha-ahmmad-al-amin.equisaas-bd.com/
GitHub: https://github.com/kholipha-ahmmad-al-amin
LinkedIn: https://www.linkedin.com/in/kholipha-ahmmad-al-amin
X: https://x.com/al_amin5519
Facebook: https://www.facebook.com/kholipha.ahmmad.al.amin
Instagram: https://www.instagram.com/kholipha.ahmmad.al.amin
## Ownership
This project was created and is maintained by Kholipha Ahmmad Al-Amin.

