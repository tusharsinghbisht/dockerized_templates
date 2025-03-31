# TypeScript Node.js Docker Template

A production-ready Node.js application template with TypeScript support, containerized with Docker.

## Folder Structure

```
typescript_node/
├── src/                      # Application source code
│   └── server.ts             # Application entry point
├── .dockerignore             # Files excluded from Docker build
├── .gitignore                # Git ignored files
├── docker-compose.dev.yml    # Docker Compose configuration for development environment
├── docker-compose.prod.yml   # Docker Compose configuration for production environment
├── Dockerfile                # Docker build configuration
├── nodemon.json              
├── package-lock.json         
├── package.json              
├── tsconfig.json             
└── README.md                 
```

## Getting Started

### Clone the template
Clone the repo and navigate to typescript_node folder

   ```bash
   # Clone the repo
   git clone https://github.com/tusharsinghbisht/dockerized_templates.git
   
   # Navigate to the typescript_node template directory
   cd dockerized_templates/typescript_node
   ```

### Development
Start the development environment:
```bash
make dev-up
```

To stop the development environment:
```bash
make dev-down
```

### Production
Build and start the production environment:
```bash
make prod-build
make prod-up
```

To view logs:
```bash
make prod-logs
```

To stop the production environment:
```bash
make prod-down
```

## Customization

### Adding Dependencies

1. Add packages to your `package.json` file
2. Rebuild the development container:
   ```bash
   make dev-down
   make dev-up
   ```
   
   Or for production:
   ```bash
   make prod-down
   make prod-build
   make prod-up
   ```

### Modifying TypeScript Configuration

Edit the `tsconfig.json` file to customize TypeScript settings according to your project requirements.
