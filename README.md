# Release Flow

## Repo Setup
- You will need to enable Github Actions to create pull requests in this repo's settings in `/settings/actions``
- You will need to use squash and merge strategy when merging pull requests

## Flow
Here we make PRs to next, with a running release-please release-pr job when commits are made to next.  

When commits are made to main, we rebase next onto main. This may fail if commits are made / PRs are merged to next at the same time. 