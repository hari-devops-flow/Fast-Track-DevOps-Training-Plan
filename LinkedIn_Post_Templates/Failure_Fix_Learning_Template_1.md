#  Failure → Fix → Learning Template #1: “The Hard Lesson”
## 😅 I broke production. Here’s what I learned.

📍Context: While setting up a CI/CD pipeline with GitHub Actions and Terraform, I mistakenly applied a config that deleted a production S3 bucket. Ouch!

### ❌ What went wrong?
- Missing `prevent_destroy = true` in Terraform
- Lack of approval stage in the pipeline
- No S3 versioning enabled

### ✅ How I fixed it:
- Restored from partial backup
- Implemented plan-apply separation
- Enabled bucket versioning and added lifecycle hooks

### 📚 What I learned:
- Automate with guardrails
- Every tool has sharp edges — use them wisely
- Postmortems are learning tools, not blame sessions

#DevOps #CICD #Terraform #FailureFixLearn #GrowthMindset #BuildInPublic
