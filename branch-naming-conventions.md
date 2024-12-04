# Git Branch Naming Conventions - Complete Reference

## Basic Format

```text
type/description-in-kebab-case
```

## Standard Type Prefixes

| Prefix     | Usage                                        | Example                        |
|------------|----------------------------------------------|--------------------------------|
| `feature/` | New features or significant additions        | `feature/user-authentication`  |
| `fix/`     | Bug fixes and minor corrections              | `fix/login-validation`         |
| `hotfix/`  | Urgent production fixes                      | `hotfix/security-breach`       |
| `bugfix/`  | Alternative to fix/ (team preference)        | `bugfix/data-loss-prevention`  |
| `docs/`    | Documentation updates                        | `docs/api-documentation`       |
| `refactor/`| Code restructuring without feature changes   | `refactor/database-queries`    |
| `test/`    | Test addition or modification               | `test/user-registration`       |
| `chore/`   | Regular maintenance tasks                    | `chore/dependency-updates`     |

## Naming Rules

### ✅ DO
- Use lowercase letters: `feature/user-login`
- Use hyphens for spaces: `fix/broken-authentication`
- Include ticket numbers when applicable: `feature/JIRA-123-user-profile`
- Keep names concise but descriptive: `feature/oauth-implementation`
- Use nouns for features: `feature/image-upload`
- Use verbs for fixes: `fix/resolve-memory-leak`

### ❌ DON'T
- Use uppercase: ~~`Feature/UserAuth`~~
- Use underscores: ~~`feature/user_profile`~~
- Skip the type prefix: ~~`new-feature`~~
- Create excessively long names: ~~`feature/very-long-detailed-description-of-changes`~~
- Use special characters: ~~`feature/user@auth`~~
- Use numbers alone: ~~`feature/123`~~

## Personal Branches

For individual development work, prefix with initials or username:

```text
john/feature/login
jd/fix/navbar
```

## Tips for Good Branch Names

1. **Be Descriptive**
    - Names should clearly indicate what work is being done
    - Anyone on the team should understand the purpose from the name
    - Use meaningful keywords related to the feature or fix

2. **Maintain Consistency**
    - Follow established team conventions
    - Use the same prefix style throughout the project
    - Keep similar features named similarly

3. **Stay Concise**
    - Aim for 2-4 words in the description
    - Avoid unnecessary words or details
    - Balance brevity with clarity

4. **Ensure Readability**
    - Use common abbreviations only if they're well understood
    - Separate words with hyphens for clarity
    - Keep the overall structure simple

5. **Enable Traceability**
    - Include ticket/issue numbers when relevant
    - Make it easy to connect branches to their related tasks
    - Consider adding context in prefixes when working across multiple projects

## Examples of Complete Branch Names

### Good Examples

```text
feature/add-google-oauth
fix/resolve-memory-leak
docs/update-api-endpoints
refactor/optimize-queries
feature/JIRA-123-add-comments
hotfix/patch-security-vulnerability
test/integration-tests
chore/update-dependencies
```

### Bad Examples with Explanations

```text
Feature/UserAuth         # Wrong: Uses uppercase letters
fix_login_bug           # Wrong: Uses underscores instead of hyphens
new-feature            # Wrong: Missing type prefix
feature/working-on-stuff # Wrong: Too vague, not descriptive
feature/this-is-a-very-long-branch-name-that-keeps-going # Wrong: Excessively long
123-feature            # Wrong: Starts with a number, missing type
```

## Version Branches

For version management (if needed):

```text
release/v1.0.0
release/v2.1.0-beta
```

## Special Cases

### Long-Running Branches

Main branches that exist throughout the project lifecycle:

```text
main
develop
staging
production
```

### Environment-Specific Branches

Branches for different deployment environments:

```text
env/production
env/staging
env/qa
```

### Multiple Tickets

When working on multiple related tickets:

```text
feature/JIRA-123-456-user-system
```

## Additional Best Practices

1. **Branch Lifecycle**
    - Delete branches after merging
    - Keep the branch list clean and manageable
    - Regular cleanup of stale branches

2. **Branch Protection**
    - Protect important branches (main, develop)
    - Set up required reviews and checks
    - Enforce naming conventions through branch protection rules

3. **Documentation**
    - Document branch naming conventions in project README
    - Include examples specific to your project
    - Explain any project-specific variations

4. **Team Communication**
    - Use branch names in commit messages
    - Reference branches in pull requests
    - Include branch naming guidelines in onboarding docs

## Git Commands for Branch Management

```bash
# Create a new branch
git checkout -b feature/user-authentication

# List all branches
git branch

# Switch to a branch
git checkout feature/user-authentication

# Delete a branch locally
git branch -d feature/user-authentication

# Delete a branch remotely
git push origin --delete feature/user-authentication

# Push a new branch to remote
git push -u origin feature/user-authentication
```

---

Remember: Branch names should be meaningful to both humans and automated tools. They should clearly communicate the purpose of the branch while following consistent patterns that make them easy to work with in commands and scripts.