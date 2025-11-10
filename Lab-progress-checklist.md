# Nginx Docker & Kubernetes Lab - Progress Checklist

Use this checklist to track your progress through the lab. Check off items as you complete them.
You can pull this repo into your IDE and check things off as you progress, once you push it to Github it will show up with the parts you've marked off. Also, feel free to mark and make notes as you need to as long as you don't iupload this into the Main branch. You can clone this IDE and submit everything into your personal GitHub Account.


---

## Pre-Lab Setup

- [ ] Docker installed and running on local machine
- [ ] kubectl installed and configured
- [ ] Kubernetes cluster accessible (minikube, kind, or cloud cluster)
- [ ] Project directory structure created
- [ ] Text editor/IDE ready for development

---

## Phase 1: Docker Implementation

### Planning & Design
- [ ] Reviewed Docker best practices documentation
- [ ] Decided on base image for Nginx
- [ ] Planned website structure (minimum 2 pages)

### Website Development
- [ ] Created custom HTML homepage
- [ ] Created at least one additional page
- [ ] Added navigation between pages
- [ ] Tested website files locally (optional but recommended)

### Dockerfile Creation
- [ ] Written Dockerfile with appropriate base image
- [ ] Implemented proper COPY/ADD commands for website files
- [ ] Configured Nginx properly in Dockerfile
- [ ] Applied optimization techniques (multi-stage builds if applicable)
- [ ] Followed security best practices (non-root user, minimal layers)
- [ ] Added appropriate EXPOSE directive

### Building & Testing
- [ ] Successfully built Docker image
- [ ] Tagged image with meaningful name and version
- [ ] Ran container locally with proper port mapping
- [ ] Verified website accessible in browser
- [ ] Tested all pages and navigation
- [ ] Checked container logs for errors
- [ ] Verified image size is optimized

### Phase 1 Deliverables
- [ ] Dockerfile saved and documented
- [ ] Website files organized in project directory
- [ ] Build commands documented

---

## Phase 2: Kubernetes Deployment

### Manifest Creation
- [ ] Created Deployment YAML file
- [ ] Configured multiple replicas (minimum 2)
- [ ] Specified container image reference
- [ ] Set appropriate labels and selectors

### Resource Management
- [ ] Defined CPU resource requests
- [ ] Defined memory resource requests
- [ ] Set CPU resource limits
- [ ] Set memory resource limits

### Health Checks
- [ ] Configured liveness probe
- [ ] Configured readiness probe
- [ ] Tested probe endpoints work correctly

### Deployment
- [ ] Applied Deployment to Kubernetes cluster
- [ ] Verified pods are created successfully
- [ ] Confirmed all replicas are running
- [ ] Checked pod status using kubectl get pods
- [ ] Reviewed pod logs for any errors

### Internal Service
- [ ] Created Service YAML for internal access
- [ ] Configured appropriate selector to match pods
- [ ] Set correct port and targetPort
- [ ] Applied Service to cluster
- [ ] Verified Service is accessible within cluster

### Testing & Validation
- [ ] Tested pod self-healing by deleting a pod
- [ ] Verified Deployment recreates deleted pods
- [ ] Confirmed resource limits are enforced
- [ ] Tested health probes by accessing endpoints

### Phase 2 Deliverables
- [ ] Deployment YAML saved
- [ ] Service YAML saved
- [ ] kubectl commands documented
- [ ] Screenshots of running pods captured

---

## Phase 3: External Access and Configuration

### External Service Configuration
- [ ] Decided on Service type (LoadBalancer, NodePort, or Ingress)
- [ ] Created/Updated Service YAML for external access
- [ ] Applied Service configuration to cluster
- [ ] Obtained external IP or access URL
- [ ] Tested external access from browser

### ConfigMap Implementation
- [ ] Identified configuration to externalize
- [ ] Created ConfigMap YAML
- [ ] Applied ConfigMap to cluster
- [ ] Updated Deployment to reference ConfigMap
- [ ] Redeployed application with ConfigMap integration

### Configuration Testing
- [ ] Verified application uses ConfigMap values
- [ ] Tested updating ConfigMap values
- [ ] Confirmed changes can be applied without image rebuild
- [ ] Documented how to update configuration

### Phase 3 Deliverables
- [ ] Updated Service YAML saved
- [ ] ConfigMap YAML saved
- [ ] External access URL documented
- [ ] Configuration update process documented
- [ ] Screenshots of accessible website from external URL

---

## Phase 4: Enhancement (Optional - Choose at Least 2)

### Horizontal Pod Autoscaling
- [ ] Created HorizontalPodAutoscaler YAML
- [ ] Configured scaling metrics (CPU/memory)
- [ ] Set min and max replica counts
- [ ] Applied HPA to cluster
- [ ] Tested scaling behavior under load

### Persistent Storage
- [ ] Created PersistentVolumeClaim YAML
- [ ] Updated Deployment to mount volume
- [ ] Configured log output to persistent storage
- [ ] Verified logs persist across pod restarts

### Ingress Configuration
- [ ] Installed Ingress controller (if not present)
- [ ] Created Ingress YAML with routing rules
- [ ] Configured host-based or path-based routing
- [ ] Applied Ingress to cluster
- [ ] Tested Ingress routing

### Custom Error Pages
- [ ] Created custom error page (404, 502, etc.)
- [ ] Updated Nginx configuration to use custom pages
- [ ] Rebuilt Docker image with new configuration
- [ ] Tested error pages work correctly

### TLS/SSL Configuration
- [ ] Obtained or generated SSL certificates
- [ ] Created Kubernetes Secret for certificates
- [ ] Updated Service/Ingress for HTTPS
- [ ] Configured certificate in Nginx
- [ ] Tested HTTPS access

### Helm Chart
- [ ] Created Helm chart structure
- [ ] Templated Kubernetes manifests
- [ ] Created values.yaml with configurations
- [ ] Tested Helm installation
- [ ] Documented Helm commands

### Namespace Isolation
- [ ] Created dedicated namespace
- [ ] Deployed application to namespace
- [ ] Configured resource quotas for namespace
- [ ] Tested namespace isolation

### Network Policies
- [ ] Created NetworkPolicy YAML
- [ ] Configured ingress/egress rules
- [ ] Applied policies to cluster
- [ ] Tested network restrictions

### Rolling Update Strategy
- [ ] Configured rolling update parameters
- [ ] Set maxSurge and maxUnavailable
- [ ] Tested update with new image version
- [ ] Verified zero-downtime deployment
- [ ] Documented rollback process

---

## Final Deliverables Checklist

### Code & Configuration
- [ ] All Dockerfiles in repository
- [ ] All website files in repository
- [ ] All Kubernetes YAML manifests in repository
- [ ] Files organized in logical directory structure

### Documentation
- [ ] README.md created
- [ ] Architecture decisions explained
- [ ] Build instructions documented
- [ ] Deployment instructions documented
- [ ] Access instructions documented
- [ ] Challenges and solutions documented
- [ ] Verification commands listed

### Verification Evidence
- [ ] Screenshot of running pods
- [ ] Screenshot of service endpoints
- [ ] Screenshot of accessible website
- [ ] Screenshot/output of kubectl describe commands
- [ ] Evidence of optional enhancements (if completed)

### Quality Checks
- [ ] All YAML files validated (proper syntax)
- [ ] No hardcoded sensitive information
- [ ] Best practices followed throughout
- [ ] Code commented where necessary
- [ ] Documentation is clear and complete

---

## Submission Ready
- [ ] All deliverables complete
- [ ] Documentation reviewed for clarity
- [ ] All files committed to repository (if using version control)
- [ ] Final testing completed
- [ ] Ready to submit

---

**Progress Summary**

Total Items Completed: _____ / _____

**Notes & Blockers:**
_(Use this space to track issues, questions, or items that need attention)_
