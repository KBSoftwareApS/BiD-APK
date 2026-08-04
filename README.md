# APK Distribution

This repository contains the APK files distributed through BiD. The APKs are separated by environment and release stage.

## Environments

| Environment | Folder | Source | Purpose |
| --- | --- | --- | --- |
| Dev | `dev` | KBS `develop` branch | Contains the latest development builds for internal testing. These builds may include work that is still in progress. |
| Demo | `demo` | KBS `main` branch | Contains builds from the main development line for demonstrations and testing against the demo environment. |
| Master | `master` | Tagged release version | Contains release versions deployed to each client's acceptance-test environment. A version in `master` is available for client validation but is not necessarily approved for production. |
| Production | `prod` | Client-approved stable version | Contains only the stable release candidate approved by the client for production use. The current production version is **V5.9.0**. |

The application uses its `appsettings.json` configuration to select the APK from the folder associated with the target environment.

## Release pipeline rules

The release pipelines must enforce the following rules:

1. Builds from the KBS `develop` branch are published only to `dev`.
2. Builds from the KBS `main` branch are published only to `demo`.
3. Only tagged release versions are published to `master` for client acceptance
   testing.
4. Publishing to `prod` requires explicit client approval of the stable release
   candidate.
5. A version must not be promoted automatically from `master` to `prod` merely
   because it has been tagged or deployed for acceptance testing.
