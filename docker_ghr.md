Once you have produced a Dockerfile for the model, you can add the following to a GitHub action file (`.github/workflows/docker_ghcr.yaml`).

You'll need to amend the final run command to point the appropriate environment name.

Once you have created that action, you can delete this file.

```
name: "Publish Docker image"
# Name of this action (else will name after the commits)
run-name: Publish Docker image on GitHub container registry (ghcr.io)

# Source: https://dev.to/github/publishing-a-docker-image-to-githubs-container-repository-4n50

on:
  push:
    branches: main
  workflow_dispatch:

jobs:
  Publish-docker-image:
    name: Publish docker image
    runs-on: ubuntu-latest

    permissions:
      contents: read
      packages: write

    steps:
      - name: Checkout
        uses: actions/checkout@v3

      - name: Login to GitHub Container Registry
        uses: docker/login-action@v1
        with:
          registry: ghcr.io
          username: ${{ github.actor }}
          password: ${{ secrets.GITHUB_TOKEN }}

      - name: Build the Docker image
        run: |
          docker build . --file reproduction/docker/Dockerfile --tag ghcr.io/pythonhealthdatascience/covid19:latest
          docker push ghcr.io/pythonhealthdatascience/covid19:latest
```