# Update Submodule and Create Pull Request

This GitHub Action workflow checks for fresh commits to a specified submodule and creates a pull request if there are any updates. It's schduled to run everyday at midnight.

## Overview

The workflow performs the following steps:

1. **Check for fresh commits to submodule**: Compares the local commit of the submodule with the remote commit on the main branch.
2. **Update submodule**: If there are new commits, updates the submodule to the latest commit.
3. **Create Pull Request**: Creates a pull request with the updated submodule.

## Prerequisites

- A Personal Access Token (PAT) with appropriate permissions (`repo`, `workflow`, and `write:discussion`) must be added to the repository secrets as `PAT_CREATE_PR`.

## Configuration

The workflow can be configured using the following environment variables:

- `SUBMODULE_NAME`: Path to the submodule you want to update (e.g., `"content"`).
- `GITHUB_TOKEN`: Token used for authentication, set to the secret `PAT_CREATE_PR`.
- `PULL_REQUEST_TITLE`: Title for the pull request.
- `PULL_REQUEST_BODY`: Body text for the pull request.

## Usage

1. **Add the Workflow**: Copy the workflow YAML file to your repository under `.github/workflows`.
2. **Configure the Environment Variables**: Update the `env` section in the YAML file with the appropriate values for your repository and submodule.
3. **Run the Workflow**: Trigger the workflow manually from the "Actions" tab in your GitHub repository.

## License

Please refer to the repository's license to understand how you can use or distribute this code.

[1]: https://github.com/peter-evans/create-pull-request
