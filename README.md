# Terraform Infrastructure-as-Code (IaC) Demo

This repository contains a simple Terraform demo designed to illustrate basic Infrastructure as Code (IaC) principles, as practiced through the HashiCorp Hands-On Labs. Specifically, this work aligns with the concepts explored in the **"Benefits of Infrastructure as Code"** lab from Section 02 of the HashiCorp Terraform workshop.  
(See: [Section 02 – Understand IaC Concepts / Benefits of Infrastructure as Code](https://github.com/btkrausen/hashicorp/blob/master/terraform/Hands-On%20Labs/Section%2002%20-%20Understand%20IAC%20Concepts/02%20-%20Benefits_of_Infrastructure_as_Code.md))

---

##  Repository Structure

- `main.tf` — Core Terraform configuration defining your resources.
- `variables.tf` — Definitions for input variables used within the configuration.
- `.gitignore` — Ensures workspace files and sensitive data are not committed.

---

##  Prerequisites

- Terraform installed (version X.Y.Z or later recommended)
- AWS credentials configured via:
  - Environment variables (`AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, etc.), or  
  - AWS CLI (`aws configure`)
- A valid Terraform backend configured (for remote state), if needed

---

##  Getting Started

1. **Clone the repository:**  
   ```bash
   git clone https://github.com/yosetto/iac_terraform.git
   cd iac_terraform
   ```

2. **Initialize Terraform** (downloads providers and sets up the workspace):  
   ```bash
   terraform init
   ```

3. **Review the execution plan:**  
   ```bash
   terraform plan
   ```

4. **Apply the configuration:**  
   ```bash
   terraform apply
   ```

5. **Clean up:**  
   ```bash
   terraform destroy
   ```

---

##  Variables

Define your variables in `variables.tf`. Provide their values via:

- `terraform.tfvars`
- CLI flags: `terraform apply -var="name=value"`
- Environment variables: `TF_VAR_name=value`

> **Security tip**: Never commit sensitive variables (e.g., secrets, credentials). Use `.gitignore` to exclude `*.tfvars`.

---

##  Best Practices

- **Ignore the `.terraform/` folder** — Terraform automatically handles provider installation.
- **Keep your `terraform.lock.hcl`** — Ensures everyone uses the same provider versions.
- **Use remote backends** for collaborative workflows (e.g., Terraform Cloud, AWS S3 + DynamoDB, Azure Blob Storage).

---

##  About This Practice

This lab exercise is part of the [HashiCorp Terraform Hands-On Labs](https://github.com/btkrausen/hashicorp/tree/master/terraform/Hands‑On%20Labs), specifically the **"Benefits of Infrastructure as Code"** section. It helped reinforce key IaC benefits:

- **Consistency & Reproducibility** — Terraform configurations can be applied repeatedly with the same results.
- **Version Control** — Your infrastructure definition lives alongside your code.
- **Automation** — Manual provisioning is replaced with scriptable workflows.  
- **Collaboration & Reviewability** — Changes can be reviewed via version control (e.g., GitHub PRs).

---

##  License

_Disclaimer: Add licensing info here, if applicable._

---

##  Summary

This repository serves as both a Terraform demo and a hands-on learning artifact from the HashiCorp IaC labs. It demonstrates how configuration file practices, variable management, and provider versioning all contribute to reliable, repeatable, and secure IaC workflows.

Happy Terraforming!
