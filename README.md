# NestJS Boilerplate with CI/CD & Docker

A production-ready NestJS boilerplate with comprehensive CI/CD pipelines, Docker containerization, and automated code quality checks.

## 🚀 Features

- **NestJS Framework**: Latest version with TypeScript support
- **Docker Containerization**: Multi-stage Docker builds with production optimization
- **CI/CD Pipeline**: GitHub Actions workflows with Docker build and deployment
- **Package Management**: pnpm for fast, efficient dependency management
- **Code Quality**: ESLint, Prettier, and automated PR checks
- **Testing**: Jest for unit and e2e tests with coverage reporting
- **Security**: Automated security audits and dependency checks
- **Code Review**: CodeRabbit integration for automated code analysis
- **Multi-Environment**: Staging and production deployment pipelines

## 📋 Prerequisites

- Node.js 20.x or higher
- pnpm 10.12.3 or higher
- Docker and Docker Compose
- Git

## 🐳 Docker Quick Start

### Build and Run
```bash
# Build Docker image
pnpm docker:build

# Run container
pnpm docker:run

# Or use docker-compose for development
pnpm docker:dev
```

### Development with Docker Compose
```bash
# Start all services (development mode)
pnpm docker:dev

# Start with rebuild
pnpm docker:dev:build

# Start production container
pnpm docker:prod

# Stop all services
pnpm docker:stop

# Clean up Docker
pnpm docker:clean
```

### Docker Compose Services
- **app**: Development server with hot reload
- **app-prod**: Production build
- **redis**: Cache and session storage
- **nginx**: Reverse proxy and load balancer

## 🚀 Quick Start

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd nestjs-boilerplate
   ```

2. **Install dependencies**
   ```bash
   pnpm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Run the application**
   ```bash
   # Development
   pnpm start:dev
   
   # Or with Docker
   pnpm docker:dev
   ```

## 📜 Available Scripts

### Development
- `pnpm start:dev` - Start development server with hot reload
- `pnpm start:debug` - Start with debug mode
- `pnpm start:prod` - Start production server

### Code Quality
- `pnpm lint` - Run ESLint with auto-fix
- `pnpm format` - Format code with Prettier
- `pnpm format:check` - Check code formatting

### Testing
- `pnpm test` - Run unit tests
- `pnpm test:watch` - Run tests in watch mode
- `pnpm test:e2e` - Run end-to-end tests
- `pnpm test:cov` - Run tests with coverage

### Building
- `pnpm build` - Build the application
- `pnpm docker:build` - Build Docker image

### Docker
- `pnpm docker:dev` - Start development environment
- `pnpm docker:prod` - Start production environment
- `pnpm docker:stop` - Stop all services

## 🔄 CI/CD Pipeline

### Workflow Stages
1. **Lint & Test** - Code quality, formatting, and testing
2. **Docker Build** - Build and test Docker image
3. **Security Scan** - Audit dependencies and security
4. **Deploy Staging** - Deploy to staging environment
5. **Deploy Production** - Deploy to production environment

### Triggers
- **Pull Request**: Runs lint, test, Docker build, and security scan
- **Push to Development**: Deploys to staging environment
- **Push to Main**: Deploys to production environment

### Docker Integration
- Multi-stage Docker builds for optimization
- Image testing and validation
- Registry integration (GitHub Container Registry)
- Health checks and monitoring

## 🏗️ Project Structure

```
nestjs-boilerplate/
├── .github/workflows/     # CI/CD pipelines
├── src/                   # Application source code
├── test/                  # Test files
├── Dockerfile             # Multi-stage Docker build
├── docker-compose.yml     # Local development setup
├── nginx.conf            # Nginx configuration
├── .dockerignore         # Docker build exclusions
└── package.json          # Dependencies and scripts
```

## 🔧 Configuration

### Environment Variables
- `NODE_ENV` - Environment (development/production)
- `PORT` - Application port (default: 3000)

### Docker Configuration
- Multi-stage builds for development and production
- Alpine Linux base images for minimal size
- Non-root user for security
- Health checks for monitoring

### Nginx Configuration
- Reverse proxy setup
- Load balancing support
- Health check endpoint routing

## 🚀 Deployment

### Staging Environment
- Automatic deployment on push to `development` branch
- Docker image building and testing
- Health check validation

### Production Environment
- Automatic deployment on push to `main` branch
- Tagged Docker images with commit SHA
- Production-optimized builds

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the UNLICENSED license.

## 🆘 Support

For support and questions:
- Check the [Issues](../../issues) page
- Review the CI/CD pipeline logs
- Check Docker container logs: `docker-compose logs app`
