# Git Operations Guide

## Introduction

Git serves as a version control system that facilitates collaborative software development. It allows for the tracking of changes, branching, and merging among other features. For an enhanced experience, Visual Studio Code (VS Code) is recommended due to its robust Git integration. The GitLens extension can further augment Git capabilities within VS Code.

## Feature Implementation Process

### Step 1: Communication

Before initiating work on a new feature, it is advised to communicate the intended feature to the team to avoid duplication of effort.

### Step 2: Branch Creation

1. **Update Local Repository**: Ensure the local repository is synchronized with the `main` or `dev` branch.
    ```bash
    git checkout main
    git pull
    ```

2. **Branch Creation**: A new branch specific to the feature should be created.
    ```bash
    git checkout -b feature/feature-name
    ```

### Step 3: Commit and Push Changes

1. **Stage Changes**: All changes should be staged.
    ```bash
    git add .
    ```

2. **Commit Changes**: Commit messages should adhere to standard language conventions (explained below).
    ```bash
    git commit -m "feat: implement feature"
    ```

3. **Push to Remote Repository**: The commits should be pushed to the remote repository.
    ```bash
    git push origin feature/feature-name
    ```

### Step 4: Pull Request Creation

1. Navigate to the web interface of the repository (e.g., GitHub, GitLab).
2. A new Pull Request should be created from the feature branch to the `main` or `dev` branch.
3. The option to "Squash commits" should be selected when merging.

#### Commit Message Convention for Squashed Commits

When squashing commits, a summary commit message should be provided. The following conventions are advised:

- `feat:` for new features
- `fix:` for bug fixes
- `chore:` for routine tasks
- `docs:` for documentation changes
- `style:` for code style changes
- `refactor:` for non-feature, non-bug code changes
- `test:` for test-related changes

### Step 5: Bug Fixes

For bug fixes, a separate branch should be created, following the same steps as for feature implementation.

## Additional Considerations

- **Conflict Resolution**: Conflicts should be resolved locally prior to pushing changes.
- **Code Review**: A review of the Pull Request is advised before merging.
- **Testing**: Adequate testing of the feature or bug fix is recommended before Pull Request creation.

This guide aims to provide a structured approach to Git operations within the project.