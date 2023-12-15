# Pipeline Documentation
![image](https://github.com/CSE-210-Team-6/shuttlecraft/assets/66744312/73cd4862-6699-42e5-890a-2c8ca7ce0e3a)

This documents the various pipelines and checks that occur when a pull request (PR) is raised against this GitHub repository.

## Build Pipeline
Builds the project against Node.js 18.x and 16.x

- build (18.x) - Runs build process on Node 18.x
- build (16.x) - Runs build on Node 16.x
## Test Pipeline
Runs unit and integration tests on Node 18.x and 16.x

- tests (18.x) - Runs tests on Node 18.x
- tests (16.x) - Runs tests on Node 16.x
## Code Quality Checks
- Code style validations - Validates code adheres to configured style guidelines
- DeepScan - Static Code Checker
- eslint - Lints codebase using ESLint and outputs reviewdog report
- prettier - Formats codebase using Prettier and outputs reviewdog report
## Test Coverage Checks
- codecov/patch - Compares test coverage between the current and parent commits
- codecov/project - Reports total test coverage compared to parent commit

PR can be merged after all checks pass.
