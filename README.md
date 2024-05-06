---
page_type: sample
languages:
- azdeveloper
- java
- bicep
products:
- azure
- azure-app-service
- azure-database-postgresql
- azure-virtual-network
urlFragment: msdocs-quarkus-postgresql-sample-app
name: "Quarkus sample: Hibernate ORM with Panache and RESTEasy"
description: This is a Quarkus web app using and the Azure Database for PostgreSQL flexible server.
---

# Quarkus sample: Hibernate ORM with Panache and RESTEasy

This is a sample application that you can use to follow along with the tutorial [Build a Quarkus web app with Azure App Service on Linux and PostgreSQL](https://learn.microsoft.com/azure/app-service/tutorial-java-quarkus-postgresql-app).

This sample is taken from [Quarkus demo: Hibernate ORM with Panache and RESTEasy](https://github.com/quarkusio/quarkus-quickstarts/tree/main/hibernate-orm-panache-quickstart). For detailed information about how the sample application is created, check out the [Quarkus guide](https://quarkus.io/guides/hibernate-orm-panache).

## Run the sample

1. Fork this repository to your account. For instructions, see [Fork a repo](https://docs.github.com/get-started/quickstart/fork-a-repo).

1. From the repository root of your fork, select **Code** > **Codespaces** > **+**.

1. In the codespace terminal, run the following command:

    ```shell
    mvn quarkus:dev
    ```

1. When you see the message `Your application running on port 8080 is available.`, click **Open in Browser**.

> [!NOTE]
> Be sure to conserve your [monthly allowance](https://docs.github.com/en/billing/managing-billing-for-github-codespaces/about-billing-for-github-codespaces) by deleting the codespace when you're done. To delete, visit [https://github.com/codespaces](https://github.com/codespaces) and select **...** > **Delete** next to the codespace.

### Quick deploy

This project is designed to work well with the [Azure Developer CLI](https://learn.microsoft.com/azure/developer/azure-developer-cli/overview), which makes it easier to develop apps locally, deploy them to Azure, and monitor them. 

🎥 Watch a deployment of the code in [this screencast](https://www.youtube.com/watch?v=JDlZ4TgPKYc).

Steps for deployment:

1. Sign up for a [free Azure account](https://azure.microsoft.com/free/)
2. Install the [Azure Dev CLI](https://learn.microsoft.com/azure/developer/azure-developer-cli/install-azd). (If you opened this repository in a Dev Container, it's already installed for you.)
3. Log in to Azure.

    ```shell
    azd auth login
    ```

4. Provision and deploy all the resources:

    ```shell
    azd up
    ```

    It will prompt you to create a deployment environment name, pick a subscription, and provide a location (like `westeurope`). Then it will provision the resources in your account and deploy the latest code. If you get an error with deployment, changing the location (like to "centralus") can help, as there may be availability constraints for some of the resources.

5. When `azd` has finished deploying, you'll see an endpoint URI in the command output. Visit that URI, and you should see the CRUD app! 🎉 If you see an error, open the Azure Portal from the URL in the command output, navigate to the App Service, select Logstream, and check the logs for any errors.

6. When you've made any changes to the app code, you can just run:

    ```shell
    azd deploy
    ```

## Run locally

Take a look at the [preconfigured dev container](.devcontainer/README.md) to see what you need for a dev environment.

## Resources

- [Azure App Service](https://azure.microsoft.com/products/app-service)
- [Quarkus guides][https://quarkus.io/guides/]
- [Quarkus samples](https://github.com/quarkusio/quarkus-quickstarts)
- [GitHub Codespaces overview](https://docs.github.com/en/codespaces/overview)
- [Introduction to dev containers](https://docs.github.com/en/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/introduction-to-dev-containers)
