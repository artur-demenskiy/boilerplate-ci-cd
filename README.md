# NestJS Boilerplate with CI/CD

A production-ready NestJS boilerplate with comprehensive CI/CD pipelines, automated code quality checks, and modern development tools.

## 🚀 Features

- **NestJS Framework**: Latest version with TypeScript support
- **Package Management**: pnpm for fast, efficient dependency management
- **CI/CD Pipeline**: GitHub Actions workflows for automated testing, building, and deployment
- **Code Quality**: ESLint, Prettier, and automated PR checks
- **Testing**: Jest for unit and e2e tests with coverage reporting
- **Security**: Automated security audits and dependency checks
- **Code Review**: CodeRabbit integration for automated code analysis
- **Staging Deployment**: Automated deployment to staging environment

## 📋 Prerequisites

- Node.js 20.x or higher
- pnpm 10.12.3 or higher
- Git

## 🛠️ Installation

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

## 📜 Available Scripts

- `pnpm start` - Start the application
- `pnpm start:dev` - Start in development mode with hot reload
- `pnpm start:debug` - Start in debug mode
- `pnpm start:prod` - Start in production mode
- `pnpm build` - Build the application
- `pnpm test` - Run unit tests
- `pnpm test:e2e` - Run end-to-end tests
- `pnpm test:cov` - Run tests with coverage
- `pnpm lint` - Run ESLint
- `pnpm format` - Format code with Prettier
- `pnpm format:check` - Check code formatting
- `pnpm depcheck` - Check for unused dependencies
- `pnpm madge` - Check for circular dependencies

## 🔄 CI/CD Pipeline

### Main CI/CD Workflow (`.github/workflows/ci-cd.yml`)

**Triggers**: Push to `main`/`development`, PR to `main`

**Jobs**:
1. **Lint**: Code linting and formatting checks
2. **Test**: Unit and e2e tests with coverage
3. **Build**: Application compilation and artifact upload
4. **Security**: Security audit and outdated package checks
5. **Deploy Staging**: Automated deployment to staging (development branch only)

### PR Checks (`.github/workflows/pr-checks.yml`)

**Triggers**: PR to `main`, push to `development`

**Jobs**:
1. **PR Analysis**: Bundle size, console.log, and TODO checks
2. **Code Quality**: TypeScript compilation, dependency analysis, linting, formatting, and tests

### Staging Deployment (`.github/workflows/staging-deploy.yml`)

**Triggers**: Push to `development`

**Features**: Automated testing, building, and deployment to staging environment

## 🏗️ Project Structure

```
nestjs-boilerplate/
├── .github/workflows/     # GitHub Actions workflows
├── src/                   # Application source code
│   ├── app.controller.ts  # Main controller
│   ├── app.service.ts     # Main service
│   ├── app.module.ts      # Root module
│   └── main.ts           # Application entry point
├── test/                  # Test files
├── .gitignore            # Git ignore patterns
├── .npmrc                # pnpm configuration
├── .coderabbit.yaml      # CodeRabbit configuration
├── package.json          # Project dependencies and scripts
└── README.md             # This file
```

## ⚙️ Configuration

### pnpm Configuration (`.npmrc`)

- Strict peer dependencies
- Hoisted node modules
- Side effects caching
- Security auditing enabled

### CodeRabbit Configuration (`.coderabbit.yaml`)

- Automated code review
- Security and quality checks
- TypeScript-specific analysis
- GitHub integration

## 🧪 Testing

The project includes comprehensive testing setup:

- **Unit Tests**: Jest with TypeScript support
- **E2E Tests**: End-to-end testing with supertest
- **Coverage**: Code coverage reporting with Codecov integration
- **Quality Checks**: Automated dependency and circular dependency analysis

## 🔒 Security

- Automated security audits with `pnpm audit`
- Dependency vulnerability scanning
- Outdated package detection
- Secure dependency installation

## 🚀 Deployment

### Staging Environment

- Automatic deployment on push to `development` branch
- Comprehensive testing before deployment
- Build artifact management

### Production Deployment

- Manual deployment process
- Environment-specific configurations
- Health checks and monitoring

## 🤝 Contributing

1. Create a feature branch from `development`
2. Make your changes
3. Run tests and quality checks: `pnpm test && pnpm lint && pnpm format:check`
4. Create a pull request to `development`
5. Ensure all CI checks pass
6. Request review from team members

## 📊 Code Quality Standards

- **Linting**: ESLint with TypeScript rules
- **Formatting**: Prettier for consistent code style
- **Type Safety**: Strict TypeScript configuration
- **Testing**: Minimum 80% code coverage
- **Dependencies**: Regular security audits and updates

## 🔧 Development Tools

- **ESLint**: Code quality and style enforcement
- **Prettier**: Code formatting
- **Jest**: Testing framework
- **TypeScript**: Type safety and modern JavaScript features
- **pnpm**: Fast package management

## 📝 Environment Variables

Create a `.env` file with the following variables:

```env
PORT=3000
NODE_ENV=development
# Add other environment-specific variables
```

## 🚨 Troubleshooting

### Common Issues

1. **Build Failures**: Ensure all dependencies are installed with `pnpm install`
2. **Test Failures**: Check test environment setup and database connections
3. **Linting Errors**: Run `pnpm lint --fix` to auto-fix issues
4. **Formatting Issues**: Run `pnpm format` to format code

### Getting Help

- Check the GitHub Actions logs for detailed error information
- Review the test output for specific failure details
- Ensure your Node.js and pnpm versions match the requirements

## 📄 License

This project is licensed under the UNLICENSED license.

## 🙏 Acknowledgments

- NestJS team for the excellent framework
- GitHub for CI/CD capabilities
- CodeRabbit for automated code review
- The open-source community for various tools and libraries
