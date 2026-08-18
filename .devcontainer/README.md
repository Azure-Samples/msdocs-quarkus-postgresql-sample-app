# .devcontainer directory

This `.devcontainer` directory contains the configuration for a [dev container](https://docs.github.com/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/introduction-to-dev-containers) and isn't used by the sample application itself.

The dev container configuration lets you open the repository in a [GitHub codespace](https://docs.github.com/codespaces/overview) or a dev container in Visual Studio Code. For your convenience, the dev container is configured with the following:

- Java 25
- Maven
- PostgreSQL in a separate container (see [docker-compose.yml](docker-compose.yml))
- [Azure CLI](https://learn.microsoft.com/cli/azure/) (so you can run `az` commands directly)
- [Azure Developer CLI](https://learn.microsoft.com/azure/developer/azure-developer-cli/overview) (so you can run `azd` commands directly).