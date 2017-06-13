# Sample Java webapp with Maven configuration to deploy to Azure App Service

The code in this repo is a very simple JSP web application with some additional Maven configuration that's ready to deploy into Azure App Service. To build the application from the command line and run it locally:

```
cd app-service-maven
mvn package
mvn tomcat7:run-war
```

## Deploy to Azure App Service

Create a web app plan and web app in Azure App Serivce and configure the web app to use Tomcat and Java 8.

Replace the placeholder values in the az-settings.xml file with the username, password, and FTP hostname in your App Service publishing profile. Then deploy to Azure App Service through Maven:

```
mvn install -s az-settings.xml
```

# Contributing

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
