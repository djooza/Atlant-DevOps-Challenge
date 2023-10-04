# Commit Message Format Enforcement Hook

## Overview

This repository includes a Git hook script named `commit-msg` that enforces a specific commit message format. The hook ensures that commit messages adhere to a predefined format, promoting consistency in commit messages across the project.

## Commit Message Format

The enforced commit message format consists of two parts, `<type>` and `<description>`.

- `<type>`: This is a keyword indicating the purpose of the commit. It can be one of the following:
  - `feature`: For new features or enhancements.
  - `fix`: For bug fixes.
  - `refactor`: For code refactoring.
  - `wip` (work in progress): For incomplete work that is not yet ready for merging.

- `<description>`: A brief, concise description of the changes introduced by the commit. It should not exceed 50 characters in length.

## How the Hook Works

The `commit-msg` hook script checks each commit message to ensure it matches the specified format. Here's what the hook does:

1. It verifies that the commit message is not empty.
2. It uses a regular expression pattern to check if the commit message matches the required format.

If the commit message does not meet the specified format, the hook will prevent the commit and display an error message.

## Usage

To use this hook in your Git repository, follow these steps:

1. Clone this repository or copy the `commit-msg` hook script to your local repository's `.git/hooks` directory.

2. Make the script executable by running:

   ```
   chmod +x .git/hooks/commit-msg
   ```

3. The hook will now enforce the commit message format for every commit you make in your local repository.