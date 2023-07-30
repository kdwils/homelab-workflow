# homelab-workflow

# About

This repository contains the github actions workflows that I use for my own projects.


# Workflows

### build-push-sign
This workflow builds a docker image for whatever supplied platforms, pushes it to github's container registry, and signs the artifact with sigstore's cosign.

Inputs

| Input       | Description | Required    | Defaults    |
| ----------- | ----------- | ----------- | ----------- |
| image      | Image Name       | true | - |
| registry   | Image Registry        | true | - |
| environment   | Image Registry        | false | Homelab |
| platforms   | Platforms to build images for | false | linux/amd64,linux/arm64 |

### go-releaser

This workflow generates a new release for go projects using goreleaser. Generally this workflow would be called whenever a new tag is pushed to a repository.

### go

a simple workflow to build go binaries and test code 