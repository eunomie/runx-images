# Docker Scout

This image bundles the Docker Scout CLI.

Read more about the CLI at https://docs.docker.com/engine/reference/commandline/scout/.

## Usage

To run the CLI you need to be authenticated with Docker Hub.
To pass your credentials to Docker Scout CLI, pass the following environment variables:
- `DOCKER_SCOUT_HUB_USER`: Your Docker Hub user name.
- `DOCKER_SCOUT_HUB_PASSWORD`: Your Docker Hub Personal Access Token (PAT).

You can then run the CLI with the following command:

```console
$ docker run -it \
  -e DOCKER_SCOUT_HUB_USER=<your Docker Hub user name> \
  -e DOCKER_SCOUT_HUB_PASSWORD=<your Docker Hub PAT>  \
  docker/scout-cli <sub command>
```

Run the `docker/scout-cli` image with the `--help` flag (or with no sub command) to see the available sub commands.

```console
$ docker run -it docker/scout-cli --help
```

If you want to access local images, you need to mount the Docker socket:

```console
$ docker run -it \
  -e DOCKER_SCOUT_HUB_USER \
  -e DOCKER_SCOUT_HUB_PASSWORD \
  -u root \
  -v /var/run/docker.sock:/var/run/docker.sock \
  docker/scout-cli <sub command>
```

## Customization

If you want to always run the CLI for your organization namespace, create a `.docker/runx.yaml` file in your current folder with the following content:

```yaml
images:
  runx/scout-cli:
    all-actions:
      opts:
        org: <your organization>
```
