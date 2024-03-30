# Versioning

A quick and dirty solution to handling update checking.

## What's going on here?

Basically, this is a quick and dirty hack that allows anybody on the team to update the latest version without having to commit to the backend. When a commit is made in this repository, a webhook automatically is triggered that makes it re-fetch the versions file.

Please **do not** update this unless you are the one releasing a new versions.
This versioning mechanism affects users across all versions of Peacock, and we don't want to accidentally give users the wrong version.

## Fields

The following fields are used for the following reasons (within a specific version):

- `active`: Boolean that determines if the channel is actively being updated.
- `version`: Integer that describes the revision identifier. Note: this field is no longer being used beyond v6.6.0 and 7.0.0-alpha.7 because of it's lack of an ability to represent complex data like pre-releases accurately.
- `versionString`: String that describes the latest version (using semver, no `v` at the beginning).

## Release channels

- Stable: the current stable build.
- Nightly: the current alpha or beta build.
