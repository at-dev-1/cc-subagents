---
## allowed-tools: Bash(git status: *), Bash(git diff:* ), Bash(git add: *), Bash(git commit:* ), Read( *), List(* )
argument-hint: [optional-scope]
description: Analyze changes and create a professional git commit following best practices
model: claude-sonnet-4-20250514


# Git Commit Command


## Context


* Current git status: !`git status --short`
* Current branch: !`git branch --show-current`
* Staged changes: !`git diff --cached --stat`


## Instructions


You are tasked with creating a professional git commit message following industry best practices and conventions. Analyze the changed files carefully to understand what has been modified, then create an appropriate commit message.


### CRITICAL REQUIREMENTS


* **NEVER** include the words "Claude", "Anthropic", "AI", "assistant", "AI-generated", or any reference to AI assistance in commit messages
* Write commit messages as if they were written by a human developer
* Focus purely on the technical changes made


### Analysis Steps


1. **Examine all changed files:**
   * Use `git diff --cached` to review staged changes
   * Use `git diff` to review unstaged changes if any
   * Read the actual file content to understand the context
   * Identify the type of change (feature, fix, refactor, docs, style, test, chore, perf, build, ci)
1. **Determine the scope:**
   * For Angular projects: identify the affected module, component, service, or directive
   * For ASP.NET Core: identify the affected controller, service, repository, or entity
   * For general changes: identify the affected subsystem or area
1. **Understand the impact:**
   * What problem does this change solve?
   * What functionality does it add or modify?
   * Are there any breaking changes?


### Commit Message Format


Follow the Conventional Commits specification:


```
<type>(<scope>): <subject>

<body>

<footer>
```


#### Type (required)


*  **feat** : New feature or functionality
*  **fix** : Bug fix
*  **docs** : Documentation only changes
*  **style** : Code style changes (formatting, missing semicolons, etc.)
*  **refactor** : Code change that neither fixes a bug nor adds a feature
*  **perf** : Performance improvements
*  **test** : Adding or updating tests
*  **build** : Changes to build configuration or dependencies
*  **ci** : Changes to CI/CD configuration
*  **chore** : Other changes that don't modify src or test files
*  **revert** : Reverts a previous commit


#### Scope (optional but recommended)


For Angular:


* Use module names: `auth`, `dashboard`, `user`, `admin`
* Use technical areas: `routing`, `guards`, `interceptors`, `pipes`
* Use component names for component-specific changes


For ASP.NET Core:


* Use API areas: `auth`, `users`, `products`, `orders`
* Use technical layers: `controllers`, `services`, `repositories`, `middleware`
* Use feature names for feature-specific changes


#### Subject Rules


* Use imperative mood ("add" not "added" or "adds")
* Don't capitalize first letter
* No period at the end
* Maximum 50 characters
* Be specific and descriptive


#### Body Guidelines (for complex changes)


* Explain the motivation for the change
* Contrast with previous behavior
* Include any technical details that help understand the change
* Wrap at 72 characters per line
* Use bullet points for multiple items


#### Footer (when applicable)


* Breaking changes: Start with `BREAKING CHANGE:`
* Issue references: `Closes #123`, `Fixes #456`
* Related PRs: `Related to #789`


### Special Considerations for Your Stack


#### Angular with NGRX and Signals


* For NGRX changes, specify the store slice affected
* For Signal-based state management, mention signal updates
* Include any effects or selectors modified


#### Entity Framework Core


* For migration changes, always use `migration` as scope
* Mention affected entities in the body
* Include any database schema changes


#### Security and Best Practices


* If the commit addresses a security issue, mention it in the body (not the subject)
* For dependency updates, list the updated packages and versions
* For performance improvements, include metrics if available


### Examples


```
feat(auth): implement JWT refresh token mechanism

Add automatic token refresh functionality to prevent session expiration.
Implements silent refresh 5 minutes before token expiry.

- Add RefreshTokenService with token rotation
- Update AuthInterceptor to handle 401 responses
- Add refresh token storage in secure HTTP-only cookie
- Implement token blacklist for revoked tokens

Closes #234
```


```
fix(user-service): resolve null reference in profile update

Guard against null user preferences when updating profile data.
Previous implementation assumed preferences object always existed.

- Add null check before accessing user.preferences
- Initialize default preferences if not present
- Add unit tests for edge cases
```


```
refactor(products): migrate to signals for state management

Replace BehaviorSubject with Angular Signals for reactive state.
Improves performance and reduces boilerplate code.

- Convert ProductStateService to use signals
- Update components to use computed signals
- Remove manual subscription management
- Maintain backward compatibility with existing APIs
```


### Workflow


1. First, analyze all the changes thoroughly
1. Determine if changes should be in one commit or split into multiple logical commits
1. If multiple commits are needed, suggest staging strategy
1. Create the commit message(s) following the format above
1. Before finalizing, verify:
   * No AI/assistance references
   * Message accurately describes the changes
   * Format follows conventions
   * All changed files are accounted for


### Final Check


Before executing the commit:


* Review the message for any accidental AI references
* Ensure technical accuracy
* Verify the commit type matches the changes
* Confirm the scope is appropriate
* Check that the message would be helpful to other developers


Execute the commit using: `git commit -m "<your message>"`


If a longer body is needed, use: `git commit` to open the editor, or provide multi-line message.


$ARGUMENTS
---
comm
