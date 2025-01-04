# Example Project: Running Notebooks Locally with PySpark in VS Code

This project demonstrates how to set up and run Jupyter Notebooks locally using the VS Code dev environment extension, including support for PySpark.

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Usage](#usage)
- [Cleaning Up](#cleaning-up)
- [Contributing](#contributing)
- [License](#license)

## Introduction
This example project is designed to help users set up a local development environment in Visual Studio Code (VS Code) to run Jupyter Notebooks with PySpark. It is intended for users who are new to PySpark and want to explore its capabilities in a familiar environment.

## Prerequisites
Before you begin, ensure you have the following installed:
- [Visual Studio Code](https://code.visualstudio.com/)
- [Docker Engine](https://docs.docker.com/get-docker/) (can be installed via [Rancher Desktop](https://rancherdesktop.io/) or [Docker Desktop](https://www.docker.com/products/docker-desktop/))

The necessary extension is the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) in VS Code.

## Setup
Follow these steps to set up the project:

1. **Clone the repository:**
    ```sh
    git clone git@github.com:pattaravut-mal/spark_vscode_environment.git
    cd spark_vscode_environment
    ```

2. **Open the project in VSCode:**
    ```sh
    code .
    ```

3. **Install VS Code extensions:**
    - Install the following extensions from the VS Code marketplace:
        - Dev Container

4. **Build and start the containers:**
    - Open the command palette (Ctrl+Shift+P) and select `Remote-Containers: Reopen in Container`.
    - This will build the Docker containers defined in the `docker-compose.yaml` file and open the project inside the container.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.