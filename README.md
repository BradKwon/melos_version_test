1. Versioning by the [semantic versioning scheme](https://semver.org/). 
    - Before v1.0.0, regardless of version type, it falls down to the one type lower.
        - Ex) major change in v0.0.1 causes v0.1.0, minor in v0.0.1 -> v0.0.2, patch in v0.0.1 -> v0.0.1+1
2. version tag name convention: <pakage_name>-v<major>.<minor>.<patch><+build>
3. Conventional Commits
    Currently the following commit types trigger a version bump:

    docs - A documentation change.
    feat - A new feature.
    fix - A bug fix.
    bug - A bug fix.
    perf - A change that improves performance.
    refactor - A change that neither fixes a bug nor adds a feature.
    revert - A change that reverts a previous commit.
    The first matching rule in the list below determines the version bump for a commit:

    A breaking change will trigger a major version bump.
    A feature will trigger a minor version bump.
    All other changes will trigger a patch version bump.

    For the breaking changes, you can simply use ! suffix. Ex) feat!:, fix!:, chore!:
4. Manual versioning: melos version <package_name> <major|minor|patch|build|X.Y.Z>