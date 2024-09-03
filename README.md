# Commit Standardization Guide This repository is a guide to help developers standardize their commit messages using the Conventional Commits concept.

## Why Standardize Commits?
- Understand the change history.
- Automate versioning and changelogs.
- Collaborate with other developers more effectively.

## Why Standardize Commits?
- Introduction: Why standardizing commits is important.
- Configuration: How to configure tools like Husky and Commitlint.
- Examples: Practical examples of standardized commits.
- Advanced: Automation and hooks to ensure the quality of commit messages.

## Configuration

1. Install the required packages:

```bash
npm install husky @commitlint/config-conventional @commitlint/cli --save-dev
```

2. Configure Husky:

```bash
npx husky install
```

3. Create a Commitlint configuration file called .commitlintrc.json:

```bash
{
"extends": ["@commitlint/config-conventional"]
}
```

4. Add a Husky hook to ensure commit messages are in the correct format:

```bash
npx husky add .husky/commit-msg 'npx --no-install commitlint --edit "$1"'
```

## Commit types

| Type | Description | Commit Example |
|------------|----------------------------------------------------------------|--------------------------------------------------|
| `feat` | Adding new functionality | `feat: implement user profile page` |
| `fix` | Bug fix | `fix: resolve login page crash issue` |
| `docs` | Documentation change | `docs: update README with setup instructions` |
| `style` | Change that does not affect the code (only formatting) | `style: format code according to linting rules` |
| `refactor` | Refactoring the code without adding functionality | `refactor: improve performance of user data processing` |
| `test` | Adding or modifying tests | `test: add unit tests for login functionality` |
| `chore` | General updates and maintenance | `chore: update dependencies` |
| `perf` | Performance-improving code changes | `perf: optimize image loading time` |
| `ci` | Continuous integration (CI) configuration changes | `ci: add GitHub Actions for automated testing` |
| `build` | Changes affecting the build system or external dependencies | `build: upgrade Node.js to version 14` |
| `revert` | Reverting a previous commit | `revert: undo commit 1234abcd` |
| `hotfix` | Urgent bug fix in production | `hotfix: fix critical bug in payment processing` |
| `security` | Security fixes | `security: patch vulnerability in user login` |
| `env` | Changes to the environment or environment variables | `env: update environment variables for staging` |
| `config` | Changes to configuration files or tools | `config: update eslint configuration` |
