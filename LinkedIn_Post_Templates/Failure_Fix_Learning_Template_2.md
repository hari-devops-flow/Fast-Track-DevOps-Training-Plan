# 🧯 Failure → Fix → Learning Template #2: “Debug Diary”

## 🚨 I spent 4 hours debugging a “Kubernetes issue.” It wasn’t Kubernetes.

Here’s the story 👇

### 🧪 The Setup:
Deployed a Node.js app via Helm to my EKS cluster. The pod would start, then crash with no logs.

### ❌ The Assumptions:
- Maybe liveness probes are wrong?
- Could be a memory limit issue?

### 🛠️ The Real Fix:
I had a bad Docker image. It was built from an old, broken Dockerfile with the wrong Node version. My local dev container was masking the issue.

### 🎯 Key Learnings:
- Always test images *before* deploying to K8s
- Enable verbose logging in `readinessProbe` and app start
- Assumptions slow you down — isolate variables fast

#DevOpsJourney #Debugging #Kubernetes #LessonsLearned #Helm #Containers
