# Jupyter Notebooks Rendered with Mercury on Azure Container Apps

An Azure Developer CLI (azd) template that renders runnable, interactive Jupyter Notebooks in the browser using [Mercury](https://github.com/mljar/mercury). This template uses Azure Container Apps to host the application on Azure. It includes:
- Application code (really just a sample Jupyter Notebook)
- Infrastructure as Code assets, written in Bicep, that provision Azure resources and specify how to deploy the code on Azure
- A GitHub Actions workflow that sets up a CI/CD pipeline to run against real Azure resources on every commit to your repo

## Prerequisites
- Azure Developer CLI
- Python 3.9+
- Docker

## Quickstart

The fastest way for you to get this application up and running on Azure is to use the `azd up` command. This single command will create and configure all necessary Azure resources - including access policies and roles for your account and service-to-service communication with Managed Identities.

1. Open a terminal, create a new empty folder, and change into it.
2. Create a new Python virtual environment.
3. Run the following command to initialize the project, provision Azure resources, and deploy the application code.

```
azd up --template savannahostrowski/python-mercury-notebooks-azd
```

## How to modify this template
In the `src/` directory, you'll find a sample notebook generated by Mercury. You can remove this file and replace it with your own Jupyter notebook(s).