# qrl-docker

[![CircleCI](https://circleci.com/gh/theQRL/qrl-docker.svg?style=svg)](https://circleci.com/gh/theQRL/qrl-docker)

This repo contains images used by QRL build processes.

Each branch contains configuration specific for each platform. The Dockerfile can also be used as a reference of our recommended installation steps.

## Example usage

(requires Docker to be installed)

1. Pull docker image of QRL node in Ubuntu 22.04 container:

    ```bash
    docker pull qrledger/qrl-docker:jammy
    ```

2. Run a detached container, may need this arg [--platform linux/{amd64,arm64}]:

    ```bash
    docker run -d --name=qrl-node qrledger/qrl-docker:jammy
    ```

3. Start the node:

    ```bash
    docker start qrl-node
    ```

4. See the console logs:

    ```bash
    docker logs qrl-node
    ```

5. Generate an encrypted wallet (-i and -t flags to interact with terminal)

    ```bash
    docker exec -i -t qrl-node qrl wallet_gen --encrypt
    ```

## Docker desktop

![CLI](https://i.imgur.com/ukaYP6s.gif)

[![Docker Desktop](https://i.imgur.com/FibGaaG.png)](https://vimeo.com/387298687)

### Windows user?

Use PowerShell run as an Administrator before running the Docker CLI commands.
