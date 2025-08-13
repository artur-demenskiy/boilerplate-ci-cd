<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg" alt="Donate us"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

# NestJS Boilerplate with CI/CD Pipeline

A production-ready NestJS boilerplate with comprehensive CI/CD pipeline, automated testing, and code quality checks.

## Features

- 🚀 **NestJS 11** - Latest version with TypeScript 5.7+
- 🔧 **Complete CI/CD Pipeline** - GitHub Actions workflows
- 📦 **pnpm** - Fast, disk space efficient package manager
- 🧪 **Automated Testing** - Jest with coverage reporting
- 📝 **Code Quality** - ESLint, Prettier, and automated checks
- 🔍 **CodeRabbit Integration** - Automated code review
- 🚀 **Staging Deployment** - Automated staging environment deployment
- 🔒 **Security Audits** - Automated dependency vulnerability scanning

## Quick Start

### Prerequisites

- Node.js 20+
- pnpm 10.12.3+

### Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd nestjs-boilerplate

# Install dependencies
pnpm install

# Start development server
pnpm run start:dev
```

### Available Scripts

```bash
# Development
pnpm run start:dev          # Start in watch mode
pnpm run start:debug        # Start in debug mode

# Building
pnpm run build              # Build the application
pnpm run start:prod         # Start production build

# Testing
pnpm run test               # Run unit tests
pnpm run test:watch         # Run tests in watch mode
pnpm run test:cov           # Run tests with coverage
pnpm run test:e2e           # Run end-to-end tests

# Code Quality
pnpm run lint               # Run ESLint
pnpm run format             # Format code with Prettier
pnpm run format:check       # Check code formatting
```

## CI/CD Pipeline

### Workflows

1. **CI/CD Pipeline** (`.github/workflows/ci-cd.yml`)
   - Linting and formatting checks
   - Unit and e2e tests
   - Build verification
   - Security audits
   - Staging deployment

2. **PR Checks** (`.github/workflows/pr-checks.yml`)
   - Code quality analysis
   - Bundle size checks
   - TypeScript compilation
   - Dependency analysis
   - Circular dependency detection

3. **Staging Deployment** (`.github/workflows/staging-deploy.yml`)
   - Automated staging deployment
   - Deployment notifications

### Automated Checks

- ✅ **ESLint** - Code quality and style
- ✅ **Prettier** - Code formatting
- ✅ **Jest** - Unit and integration tests
- ✅ **TypeScript** - Type checking
- ✅ **Security Audit** - Dependency vulnerabilities
- ✅ **Bundle Analysis** - Size and dependency checks
- ✅ **Code Coverage** - Test coverage reporting

## Project Structure

```
nestjs-boilerplate/
├── .github/workflows/     # GitHub Actions workflows
├── src/                   # Application source code
├── test/                  # Test files
├── .coderabbit.yaml      # CodeRabbit configuration
├── .npmrc                # pnpm configuration
├── .gitignore            # Git ignore patterns
└── package.json          # Project dependencies
```

## Configuration

### pnpm Configuration (`.npmrc`)

- Strict peer dependency resolution
- Hoisted node modules
- Side-effects caching
- Exact version saving

### CodeRabbit Configuration (`.coderabbit.yaml`)

- Automated code review
- Security vulnerability detection
- Code quality analysis
- Performance optimization suggestions

## Contributing

1. Create a feature branch from `staging`
2. Make your changes
3. Run tests: `pnpm run test`
4. Check code quality: `pnpm run lint`
5. Format code: `pnpm run format`
6. Submit a pull request

## Deployment

### Staging

Automatically deployed on push to `staging` branch.

### Production

Deploy from `main` branch after successful staging deployment.

## Support

For issues and questions:
- Create an issue in the repository
- Check the CI/CD pipeline logs
- Review the automated code review feedback

## License

This project is licensed under the MIT License.
