# coredns-builds

[coredns](https://github.com/coredns/coredns) Builds specific to [Kuma](https://github.com/kumahq/kuma).

## Making dependabot work 

To be able to rely on dependabot we have a `go mod` in the root with the 2 dependencies we have. Because `go mod tidy` will remove
unused dependencies we have an `internal` package that imports these 2 dependencies.

## Building

You can build the entire package with `make tar` everything will then be in `build/out`. 
In practice this is all done in a github action.

## Releasing a new version

If the version in `main` changes, a build and release of the binaries for that version is triggered.
You can also manually trigger the workflow for a specific version.
