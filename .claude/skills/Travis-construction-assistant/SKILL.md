```markdown
# Travis-construction-assistant Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `Travis-construction-assistant` TypeScript codebase. You'll learn how to structure files, write and organize code, follow commit message conventions, and implement and run tests. This guide ensures consistency and maintainability across the project.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example:  
    ```
    construction-helper.ts
    project-manager.test.ts
    ```

### Import Style
- Use **relative imports** for referencing other files.
  - Example:
    ```typescript
    import { calculateEstimate } from './estimate-utils';
    ```

### Export Style
- Use **named exports** exclusively.
  - Example:
    ```typescript
    // estimate-utils.ts
    export function calculateEstimate() { ... }
    ```

### Commit Messages
- Follow the **Conventional Commits** format.
- Use the `feat` prefix for new features.
- Keep commit messages concise (average ~48 characters).
  - Example:
    ```
    feat: add material cost calculation module
    ```

## Workflows

### Feature Development
**Trigger:** When adding a new feature  
**Command:** `/feature-development`

1. Create a new TypeScript file using kebab-case.
2. Implement the feature using named exports.
3. Import dependencies using relative paths.
4. Write a corresponding test file (`*.test.ts`).
5. Commit changes using the `feat:` prefix and a concise message.

### Testing
**Trigger:** When validating code changes  
**Command:** `/run-tests`

1. Ensure all test files follow the `*.test.ts` pattern.
2. Run the test suite using the project's test runner (framework unknown; check project scripts).
3. Review and fix any failing tests before committing.

### Code Review Preparation
**Trigger:** Before submitting a pull request  
**Command:** `/prepare-code-review`

1. Check all file names for kebab-case.
2. Ensure all imports are relative and exports are named.
3. Review commit messages for conventional format.
4. Confirm all tests pass.

## Testing Patterns

- Test files are named with the `*.test.ts` pattern.
- Place test files alongside or near the modules they test.
- Testing framework is unspecified; check project documentation or scripts for details.
- Example test file:
  ```typescript
  // estimate-utils.test.ts
  import { calculateEstimate } from './estimate-utils';

  describe('calculateEstimate', () => {
    it('should return correct total', () => {
      expect(calculateEstimate(5, 10)).toBe(50);
    });
  });
  ```

## Commands
| Command                | Purpose                                      |
|------------------------|----------------------------------------------|
| /feature-development   | Start a new feature using project conventions|
| /run-tests             | Run all test files in the codebase           |
| /prepare-code-review   | Prepare code for review and ensure standards |
```
