# MC-Service
CodeDevils Minecraft as a service with David Welborn.

_**To simplify Minecraft bedrock edition administration**_

## About the Project
Minecraft as a Service is going to be a system that simplifies provisioning and managing minecraft bedrock edition servers. Minecraft admins will be able to login to a dashboard to spin up and shutdown worlds, see world health, review and restore from backups as needed, queue updates, and otherwise maintain the server from a single pane of glass.

## Built With
We are architecting this system with **cross-cloud and on-prem support**, **DevOps**, and **micro-service architecture** as first-class citizens. Releases will be as simple as following process in our pipeline with pull requests, automated testing, and continuous deployment. This service will leverage technologies like **Terraform for Infrastructure-as-Code** and **Kubernetes** for container orchestration.

## Objectives
- Simplified Minecraft administration user experience
- Real-time metrics and meta data about running worlds
- System is extensible for other server-client games
- Deployment is deterministic and cloud-agnostic
