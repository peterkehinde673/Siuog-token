# Contributing to Siuog Token

Thank you for your interest in contributing to Siuog Token! This document provides guidelines and instructions for contributing.

## Code of Conduct

We are committed to providing a welcoming and inspiring community for all. Please read and follow our [Code of Conduct](./CODE_OF_CONDUCT.md).

## How to Contribute

### Report Bugs

Submit a bug report by opening an issue. Please include:

1. **Title**: Clear, descriptive title
2. **Description**: What happened and what you expected
3. **Steps to Reproduce**: Exact steps to reproduce the issue
4. **Environment**: Node version, OS, network (testnet/mainnet)
5. **Screenshots/Logs**: Any relevant error messages or logs

### Suggest Features

Submit feature requests as GitHub issues with:

1. **Title**: Feature name
2. **Use Case**: Why this feature is needed
3. **Implementation Ideas**: Any thoughts on how to implement it
4. **Related Issues**: Links to related discussions

### Submit Code

#### Prerequisites

- Node.js 18+
- npm 9+
- Basic Git knowledge
- Understanding of TypeScript and Solidity

#### Development Setup

```bash
# Fork the repository on GitHub

# Clone your fork
git clone https://github.com/YOUR_USERNAME/Siuog-token.git
cd Siuog-token

# Add upstream remote
git remote add upstream https://github.com/peterkehinde673/Siuog-token.git

# Install dependencies
npm install

# Create feature branch
git checkout -b feature/your-feature-name
```

#### Development Workflow

1. **Create a feature branch** from `develop`:
   ```bash
   git checkout -b feature/descriptive-name
   ```

2. **Make your changes**:
   - Follow code style (see below)
   - Add tests for new functionality
   - Update documentation
   - Keep commits atomic and descriptive

3. **Run tests locally**:
   ```bash
   npm test
   npm run test:coverage
   ```

4. **Build**:
   ```bash
   npm run build
   ```

5. **Commit with conventional commits**:
   ```bash
   # Format: type(scope): description
   git commit -m "feat(sdk): add tip history filtering"
   ```

6. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

7. **Create a Pull Request** on GitHub

#### Commit Message Format

Use [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <subject>

<body>

<footer>
```

- **type**: feat, fix, docs, style, refactor, perf, test, chore
- **scope**: contracts, sdk, examples, docs
- **subject**: imperative, lowercase, no period, under 50 characters
- **body**: explain what and why (wrap at 72 characters)
- **footer**: reference issues (Fixes #123)

Examples:
```
feat(sdk): add tip history filtering
fix(contracts): resolve reentrancy vulnerability
docs(integration): add platform integration guide
```

### Code Style

#### TypeScript

- Use ESLint configuration provided
- Strict null checking enabled
- No `any` types without explanation
- Use meaningful variable names
- Max line length: 100 characters

```bash
npm run lint
npm run lint:fix
```

#### Solidity

- Follow Solidity style guide
- Use OpenZeppelin contracts where applicable
- Comprehensive NatSpec comments
- Unit tests for all functions

```bash
npm run lint:contracts
```

### Testing

- **Unit tests**: Test individual functions in isolation
- **Integration tests**: Test interactions between components
- **Coverage**: Aim for >80% coverage

```bash
# Run all tests
npm test

# Run specific test file
npm test -- tests/unit/token.test.ts

# With coverage
npm run test:coverage

# Watch mode
npm run test:watch
```

### Documentation

- Update README.md if functionality changes
- Add JSDoc comments for public APIs
- Document breaking changes in CHANGELOG.md
- Include examples for new features

### Pull Request Process

1. **Link to Issues**: Reference related issues (e.g., "Fixes #123")

2. **Description**: Clearly describe:
   - What the PR changes
   - Why these changes are needed
   - How to test the changes

3. **Checklist**:
   ```
   - [ ] Tests pass locally
   - [ ] Code follows style guidelines
   - [ ] Documentation updated
   - [ ] CHANGELOG.md updated
   - [ ] No breaking changes (or documented)
   ```

4. **Review**: Address reviewer feedback promptly

5. **Merge**: After approval, maintainers will merge

## Development Branches

- **main**: Production-ready code, tagged with versions
- **develop**: Integration branch for features
- **feature/**: Individual feature branches from develop
- **fix/**: Bugfix branches from develop

## Release Process

1. Update version in package.json
2. Update CHANGELOG.md with new version
3. Create release tag
4. Publish to npm

## Areas We're Looking For

- **Solidity Developers**: Contract optimization, new features
- **TypeScript Developers**: SDK expansion, type safety
- **DevOps Engineers**: Deployment automation, CI/CD
- **Documentation Writers**: Guides, tutorials, examples
- **Community Managers**: Integration partnerships, adoption

## Questions?

- **Documentation**: See [docs/](./docs/) folder
- **Discord**: [Kehinde Labs Community](https://discord.gg/kehindelaabs)
- **GitHub Discussions**: [Project Discussions](https://github.com/peterkehinde673/Siuog-token/discussions)

## Recognition

All contributors are recognized in:
- CONTRIBUTORS.md file
- GitHub contributors page
- Release notes (for significant contributions)

Thank you for helping build Siuog Token! 🚀
