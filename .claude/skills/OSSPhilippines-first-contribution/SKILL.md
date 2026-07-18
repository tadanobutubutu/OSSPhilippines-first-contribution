```markdown
# OSSPhilippines-first-contribution Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns, coding conventions, and contribution workflows used in the `OSSPhilippines-first-contribution` TypeScript repository. You'll learn how to structure code, follow commit and file naming conventions, and contribute effectively—especially when updating contributor profiles.

## Coding Conventions

### File Naming
- Use **camelCase** for filenames.
  - Example: `contributorProfile.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { getContributor } from './contributorUtils';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // contributorUtils.ts
    export function getContributor(id: string) { ... }
    ```

### Commit Messages
- Use prefixes like `fix` or `update` to indicate the type of change.
- Keep commit messages concise (average ~49 characters).
  - Example:
    ```
    fix: correct photo URL in contributor profile
    update: add new contributor profile for Jane Doe
    ```

## Workflows

### Update Contributor Profile
**Trigger:** When someone needs to add or correct information for a contributor (such as file extension or photo URLs).
**Command:** `/update-contributor`

1. Locate the relevant JSON file in the `contributors/` directory (e.g., `contributors/janedoe.json`).
2. Edit the file to update or fix the contributor's information.
   - Example change:
     ```json
     {
       "name": "Jane Doe",
       "photoUrl": "https://example.com/janedoe.jpg"
     }
     ```
3. Commit your changes with a descriptive message, such as:
   ```
   update: fix photo URL for Jane Doe
   ```
4. Open a pull request if required by the repository.

## Testing Patterns

- **Test files** follow the `*.test.*` naming convention (e.g., `contributorUtils.test.ts`).
- **Testing framework** is not specified; check existing test files for patterns.
- Place test files alongside or near the code they test.

  Example test file:
  ```typescript
  // contributorUtils.test.ts
  import { getContributor } from './contributorUtils';

  test('should return contributor by ID', () => {
    expect(getContributor('janedoe').name).toBe('Jane Doe');
  });
  ```

## Commands

| Command              | Purpose                                                        |
|----------------------|----------------------------------------------------------------|
| /update-contributor  | Update or fix contributor profile information in contributors/  |

```