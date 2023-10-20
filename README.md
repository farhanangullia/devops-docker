# devops-docker

## Docker container releases for monorepo

- This repository contains a Git submodule (ecommerce-app) which contains 4 independent microservice that serves REST APIs. 3 of these services are Python based and 1 is Go based. Each of these services has their respective Dockerfile in their directory.
- A GitHub workflow is configured to **build** and **push** these 4 container images to GHCR (GitHub Container Registry)
  - Builds support multi platform: amd64 and arm64
  - Images are published to GitHub Packages
- The workflow triggers on demand OR if there are changes to files in any of these directories:
  - ecommerce-app/cart-service
  - ecommerce-app/order-service
  - ecommerce-app/catalog-service
  - ecommerce-app/shipping-service

### Workflow template 
https://github.com/farhanangullia/devops-docker/blob/main/.github/workflows/docker.yml

#### Images

##### Cart Service
https://github.com/farhanangullia/devops-docker/pkgs/container/devops-docker%2Fcart-service

##### Order Service
https://github.com/farhanangullia/devops-docker/pkgs/container/devops-docker%2Forder-service

##### Catalog Service
https://github.com/farhanangullia/devops-docker/pkgs/container/devops-docker%2Fcatalog-service

##### Shipping Service
https://github.com/farhanangullia/devops-docker/pkgs/container/devops-docker%2Fshipping-service
