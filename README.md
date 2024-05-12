# flutter_gha

A new Flutter project to test gha capabilities

## Capabilities:

### OS specific builds:

- Build Android [.github/android.yaml](.github/android.yaml)
- Build iOS [.github/ios.yaml](.github/ios.yaml)

Both the workflows take version number and release notes as input and upload artifacts.

### PR Builds:

- Build PR [.github/pr.yaml](.github/pr.yaml)

Calls both Android and iOS workflows to build the project and upload artifacts.

#### Test Build:

- Build Test [.github/test_release.yaml](.github/test_release.yaml)

Downloads the artifacts from the latest release and publishes them to Firebase App Distribution.

#### Release Build:

- Build Release [.github/test_release.yaml](.github/test_release.yaml)

Builds the project and then downloads the artifacts from the latest release and publishes them to
Play store and App store

### Nightly Builds:

- Build Nightly [.github/nightly.yaml](.github/nightly.yaml)

Builds the project and then downloads the artifacts to test them on Maestro cloud.

## Notes:
- Uses macos-latest runner for iOS builds only to reduce costs. Everything else is on ubuntu-latest.

### TODO
- [ ] Push iOS build to App distribution
- [ ] Signing Android builds
- [ ] Signing iOS builds
- [ ] Publish to Play Store
- [ ] Publish to App Store
- [ ] Test iOS on Maestro cloud

