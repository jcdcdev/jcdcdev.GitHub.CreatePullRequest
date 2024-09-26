# jcdcdev.GitHub.CreatePullRequest

This action checks for differences between source and target branches and creates a pull request if there are any differences.

If a pull request already exists, it will update the existing pull request with the latest changelog.

## Inputs

| Input           | Description                                                                   | Required |
| --------------- | ----------------------------------------------------------------------------- | -------- |
| `source-branch` | The source branch to compare against the target branch                        | `true`   |
| `target-branch` | The target branch to compare against the source branch                        | `true`   |
| `github-token`  | The GitHub token to use for authentication (use `{{ secrets.GITHUB_TOKEN }}`) | `true`   |
| `dry-run`       | Whether to perform a dry run or not - defaults to `false`                     | `false`  |

## Outputs

| Output      | Description                                  |
| ----------- | -------------------------------------------- |
| `pr-number` | The pull request number (if created/updated) |