# castingnetworks/.github

This repository houses [starter workflow templates](https://docs.github.com/en/actions/using-workflows/creating-starter-workflows-for-your-organization) for the castingnetworks organization.

## Templates

!!! note
    
    The following 4 workflows are intended to be used as a package. Technically the build workflow could be used in isolation but the release, force-prerelease, and delete-release workflows should be added together.

### castingnetworks-build

The workflows are designed to be used in nodejs projects that use nx for the build and have an optional terraform directory.
This workflow file covers the standard build and test and is the same template that is used for the release.

### castingnetworks-force-prerelease

This workflow is part of the standard Release Process and is used to ensure all newly created releases are marked as a prerelease.

This workflow enables us to trust the state of releases in GitHub and know that any release labeled as 'latest' is what is currently deployed to production.
The most recent release labeled 'prerelease' is what is currently deployed to staging.
The expectation is that a prerelease will be deployed to staging and needs to be promoted to production.

### castingnetworks-delete-release (rollback)

This workflow is part of the standard Release Process and is used to perform a Rollback in the event that there is a problem with a release that was promoted to production.

### castingnetworks-release

The workflows are designed to be used in nodejs projects that use nx for the build and have an optional terraform directory.
This workflow file covers the standard release and is the same template that is used for the build.
