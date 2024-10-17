# runx-images

## Overview

This is a collection of [docker runx](https://github.com/eunomie/runx) compatible images.

Those images can be used without `runx`, like with `docker run` or `docker compose` for instance. In this case they are just mirrors of the official images.

Explore the documentation of each image to know more and learn how to use them with `docker runx IMAGE --help`.

List the available commands using `docker runx IMAGE --list` or get detailed information about an action using `docker runx IMAGE ACTION --help`.

Then simply run the image with `docker runx IMAGE [ACTION]`.

## Images

- [golangci-lint](./golangci-lint): A Docker image for [golangci-lint](https://golangci-lint.run/) with some defaults and caching enabled
    ```
    $ docker runx eunomie/golangci-lint --help
    ```
- [scout-cli](./scout-cli): A Docker image for [Docker Scout CLI](https://docs.docker.com/engine/reference/commandline/scout/) to showcase how to use it
    ```
    $ docker runx eunomie/scout-cli --help
    ```

Images are available on [Docker Hub](https://hub.docker.com/u/eunomie).
