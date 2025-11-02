# AI Agent Instructions for Argo-Kustomize-Project

## Project Overview
This project focuses on Kubernetes resource management using Argo CD and Kustomize, with a specific emphasis on financial services deployment. The project is organized into microservices within the finance domain.

## Repository Structure
```
.
└── finance/
    ├── integration-api/     # Financial integration service
    └── payment-poc-api/     # Payment processing PoC service
```

## Key Technologies
- Argo CD: GitOps continuous delivery tool for Kubernetes
- Kustomize: Kubernetes native configuration management
- Kubernetes: Container orchestration platform

## Project Conventions
1. **Service Organization**
   - Financial services are grouped under the `finance/` directory
   - Each service has its own dedicated directory for Kubernetes manifests
   - Services follow a domain-driven directory structure

2. **Deployment Configuration**
   - Kustomize is used for managing environment-specific configurations
   - Base configurations should be placed in each service's base directory
   - Overlays should be used for environment-specific customizations

## Common Tasks
1. **Adding a New Service**
   - Create a new directory under the appropriate domain folder
   - Include base Kubernetes manifests and Kustomize configurations
   - Follow the existing pattern from integration-api or payment-poc-api

2. **Modifying Service Configuration**
   - Use Kustomize patches for environment-specific changes
   - Maintain backward compatibility when updating base configurations
   - Test changes using `kubectl kustomize` before committing

## Best Practices
1. Follow GitOps principles - all changes should be made through Git
2. Use semantic commit messages that clearly describe the changes
3. Document significant architectural decisions in service-level READMEs
4. Keep service configurations independent to maintain separation of concerns

## Need Help?
- Review the project README for basic setup instructions
- Check service-specific documentation for detailed configuration options
- Consult Argo CD and Kustomize documentation for best practices