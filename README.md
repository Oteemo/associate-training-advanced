# Advanced DevOps Hands-On Lab: Deploying Nginx with Docker and Kubernetes

## Lab Overview

This advanced hands-on lab challenges you to deploy a custom Nginx website using containerization and orchestration technologies. You'll work independently to research, design, and implement a complete solution from development to production-ready deployment.

**Estimated Time:** 4-6 hours

**Difficulty Level:** Advanced

---

## Learning Objectives

By the end of this lab, you will be able to:

- Build and optimize custom Docker images for web applications
- Implement Docker best practices for security and efficiency
- Deploy containerized applications to a Kubernetes cluster
- Configure Kubernetes resources including Deployments, Services, and ConfigMaps
- Expose applications externally using appropriate Kubernetes networking
- Implement basic scaling and self-healing capabilities
- Debug containerized applications in a Kubernetes environment

---

## Prerequisites

Before starting this lab, you should have:

- Working knowledge of Linux command line
- Understanding of container concepts and Docker basics
- Familiarity with YAML syntax
- Basic understanding of networking concepts (ports, protocols, DNS)
- Access to a machine with Docker installed
- Access to a Kubernetes cluster (local or cloud-based)
- If you do not have experience with these tools, research them as you work on this project

---

## Lab Goals

### Phase 1: Docker Implementation

**Primary Goal:** Create a custom Docker image running Nginx with a personalized static website.

**Requirements:**
- Create a custom HTML website (minimum 2 pages with navigation)
- Write an optimized Dockerfile using best practices
- Build and tag your Docker image appropriately
- Run and test the container locally
- Verify the website is accessible via browser

**Success Criteria:**
- Docker image builds without errors
- Container runs successfully and serves web content
- Image follows multi-stage build patterns (if applicable)
- Image size is optimized
- Container logs are accessible and meaningful

### Phase 2: Kubernetes Deployment

**Primary Goal:** Deploy your containerized Nginx application to a Kubernetes cluster.

**Requirements:**
- Create Kubernetes manifests for your application
- Deploy the application using a Deployment resource
- Ensure the application is highly available (multiple replicas)
- Implement proper resource requests and limits
- Configure liveness and readiness probes
- Expose the application internally within the cluster

**Success Criteria:**
- Deployment successfully creates and manages pods
- Pods are running and healthy
- Application automatically recovers from pod failures
- Resource constraints are properly defined
- Health checks function correctly

### Phase 3: External Access and Configuration

**Primary Goal:** Make your application accessible from outside the cluster and implement external configuration.

**Requirements:**
- Expose your application to external traffic
- Implement a Service resource with appropriate type
- Use ConfigMaps to externalize configuration
- Make at least one aspect of your website configurable without rebuilding the image

**Success Criteria:**
- Application is accessible via external IP or domain
- Service correctly routes traffic to pods
- Configuration can be updated without image rebuild
- Changes to ConfigMaps can be applied to running pods

### Phase 4: Enhancement (Optional Challenge)

**Choose at least TWO of the following enhancements:**

- Implement horizontal pod autoscaling based on CPU or memory
- Add persistent storage for application logs
- Configure Ingress for path-based or host-based routing
- Implement a custom error page
- Add TLS/SSL certificates for HTTPS access
- Create a Helm chart for your application
- Implement namespace isolation
- Add network policies for security
- Configure a rolling update strategy with zero downtime

---


## Recommended Resources

### Docker Resources
- Official Docker Documentation: https://docs.docker.com/
- Docker Best Practices: https://docs.docker.com/develop/dev-best-practices/
- Dockerfile Reference: https://docs.docker.com/engine/reference/builder/
- Nginx Official Docker Image: https://hub.docker.com/_/nginx

### Kubernetes Resources
- Official Kubernetes Documentation: https://kubernetes.io/docs/home/
- Kubernetes Concepts: https://kubernetes.io/docs/concepts/
- kubectl Cheat Sheet: https://kubernetes.io/docs/reference/kubectl/cheatsheet/
- Kubernetes Best Practices: https://kubernetes.io/docs/concepts/configuration/overview/

### Tutorials and Guides
- Kubernetes Tutorials: https://kubernetes.io/docs/tutorials/
- Docker Getting Started: https://docs.docker.com/get-started/
- Nginx Configuration Guide: https://nginx.org/en/docs/

### Tools You May Need
- Docker Desktop (for local development)
- kubectl (Kubernetes command-line tool)
- minikube or kind (for local Kubernetes clusters)
- k9s (optional - terminal-based Kubernetes UI)

### Additional Learning
- Play with Docker: https://labs.play-with-docker.com/
- Play with Kubernetes: https://labs.play-with-k8s.com/
- Katacoda Kubernetes Scenarios: https://www.katacoda.com/courses/kubernetes

---

## Hints and Considerations

**Think About:**
- What base image should you use? Consider size and security.
- How will you handle configuration that might change between environments?
- What happens if a pod crashes? How does Kubernetes handle this?
- How do you ensure zero-downtime deployments during updates?
- What security considerations should you implement?
- How will you debug issues when they arise?

**Common Pitfalls to Avoid:**
- Running containers as root user
- Hardcoding configuration values in images
- Not setting resource limits
- Exposing unnecessary ports
- Not implementing health checks
- Using `latest` tags in production

---

## Getting Started

1. Set up your development environment with Docker and kubectl
2. Verify access to your Kubernetes cluster
3. Create a project directory structure
4. Start with Phase 1 and progress sequentially
5. Test thoroughly at each phase before moving forward
6. Document your process as you go

**Remember:** This is a research-based lab. You're expected to search documentation, troubleshoot errors, and find solutions independently. The struggle is part of the learning process!

---

## Support

While you should work independently, consider these resources when stuck:
- Review error messages carefully - they often contain the solution
- Check pod logs using `kubectl logs`
- Describe resources using `kubectl describe` for detailed status
- Use the official documentation first before searching elsewhere
- Community forums like Stack Overflow for specific technical issues
- If you use AI, always test, and always fact check

**Good luck, and happy containerizing!**
