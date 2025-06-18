# Asynk

Asynk is a modular SaaS platform inspired by GoHighLevel. It provides a Next.js front-end with a set of microservices to handle CRM, automation workflows and documentation.

This repository contains the core Next.js application and configuration for local development and deployment.

## Features
- Website and funnel builder
- CRM with multi-tenant support
- Automation workflows powered by n8n
- Stripe billing integration
- Documentation site powered by Docusaurus

## Local Development
Requirements:
- Node.js 20
- Docker

Install dependencies and copy the example environment file:

```bash
npm install
cp .env.example .env.local
```

Start the stack using Docker Compose:

```bash
docker compose up
```

The Next.js app will be available on `http://localhost:3000` and n8n on `http://localhost:5678`.

## Configuration
Create a `.env.local` file using the provided `.env.example` and set the values for your environment such as Stripe keys and domain name.

## Deployment
A GitHub Actions workflow is included to deploy the `main` branch to Vercel. Configure the `VERCEL_TOKEN`, `VERCEL_ORG_ID`, and `VERCEL_PROJECT_ID` secrets in your repository settings.

## Contributing
Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License
Licensed under the [MIT License](LICENSE).
