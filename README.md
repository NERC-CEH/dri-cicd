# dri-cicd
Repo for CI/CD workflow files used in DRI

## About

This repo contains several GitHub actions workflows that are reused in other projects to maintain CI/CD pipelines in one central repository.

## Private repos

Some repositories depend on private repos.  To enable access to them
from the CI environment, follow the below steps:

1. In the [settings][] for the `dri-private-repos` GitHub app,
   generate a new private key and make a note of it.

2. Add the private key as a repository secret called `PRIVATE_KEY` by
   going to
   https://github.com/NERC-CEH/$repo/settings/secrets/actions.

3. Switch to the "Variables" tab and add the `APP_ID` with value
   1737249.

4. Make sure to call the workflows with the `private_repos` argument
   set to `true`.

[settings]: https://github.com/organizations/NERC-CEH/settings/apps/dri-private-repos
