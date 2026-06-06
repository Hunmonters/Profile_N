```markdown
# Profile_N Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the Profile_N TypeScript codebase. It covers file naming, import/export styles, commit message habits, and testing patterns. While no specific frameworks or automated workflows are detected, this guide will help you contribute code that matches the project's established style.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `accountSettings.test.ts`

### Imports
- Use **relative import paths** for modules within the project.
  - Example:
    ```typescript
    import { getUserProfile } from './userProfile';
    ```

### Exports
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // userProfile.ts
    export function getUserProfile(id: string) { ... }
    ```

### Commit Messages
- Commit messages are **freeform** (no enforced structure or prefixes).
- Average commit message length: ~43 characters.

## Workflows

### Adding a New Module
**Trigger:** When you need to add a new feature or module.
**Command:** `/add-module`

1. Create a new file using camelCase naming (e.g., `newFeature.ts`).
2. Write your TypeScript code using named exports.
3. Use relative imports to include other modules.
4. If applicable, create a corresponding test file named `newFeature.test.ts`.
5. Commit your changes with a clear, concise message.

### Writing Tests
**Trigger:** When you need to test a module or function.
**Command:** `/write-test`

1. Create a test file with the pattern `*.test.ts` (e.g., `userProfile.test.ts`).
2. Write your test cases using the project's preferred (but unspecified) testing framework.
3. Use relative imports to bring in the module under test.
4. Run your tests using the project's test runner (see Testing Patterns).

## Testing Patterns

- Test files follow the `*.test.ts` naming convention.
  - Example: `userProfile.test.ts`
- The specific testing framework is **unknown**; check existing test files for patterns.
- Import modules under test using relative paths.
  - Example:
    ```typescript
    import { getUserProfile } from './userProfile';

    // Example test (framework-agnostic)
    test('should fetch user profile', () => {
      // test implementation
    });
    ```

## Commands
| Command        | Purpose                                    |
|----------------|--------------------------------------------|
| /add-module    | Scaffold and add a new module or feature   |
| /write-test    | Create and implement a new test file       |
```
