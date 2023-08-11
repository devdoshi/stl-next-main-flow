# Release Flow

## Repo Setup
- You will need to enable Github Actions to create pull requests in this repo's settings in `/settings/actions``
- You will need to use squash and merge strategy when merging pull requests
- You will need to find-and-replace "my-package" with the name of your actual package throughout this repo. 

## Flow
Here we make PRs to next, with a running release-please release-pr job when commits are made to next.  

When commits are made to main, we rebase next onto main. This may fail if commits are made / PRs are merged to next at the same time. 

`release.yml` and `draft-release.yml` use concurrency: 'release' to ensure both sets of actions run sequentially to make it easier to reason about the sequence of events. 

`pr.yml` checks for valid PR branches. A PR must be from any branch to next, or release-please--branches--next--components--my-package to main


