![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)![Build Status](https://travis-ci.com/ZackBorton/Basic.Template.API.svg?branch=master)

# Ensure you have docker installed then
* In the API directory you should build the container ```docker build --no-cache .```
* Then to run the app running on port 5005 run this command ```docker compose up```

# TODO
* Install AWS cli and install AWS cert bundles 
* Add localstack logic

# Basic.Template.API
Basic bootstrapped project for creating a new dotnet app using the dotnet new command

### Clone the project locally
```git clone https://github.com/ZackBorton/Basic.Template.API.git```

### Ensure you have the correct version of dotnet installed
Should be 3.0.1 or higher if its not install the latest stable version

``` dotnet --version```

### HTTPS
This app requires running https locally using a self signed cert. You can do so by running the following command
```dotnet dev-certs https --trust```

### If this is a local project use the directory containing the .template.config folder to install the project
```dotnet new -i FullPathToConfig```

Example 
```dotnet new -i "PathToYourProject/Basic.Template.API/Basic.Template.API/content/"```

### You should now be able to view the new template by running
```dotnet new```

* Templates: API with swagger
* Short Name: Basic.API.Template

### Finally create a new project using the dotnet new syntax
```dotnet new Basic.API.Template```

To note you can specifiy a new name for the project being created

```dotnet new Basic.API.Template --name NewAppName```

### Uninstalling
You need to supply the full path to the content directory specified during install step listed above

### Issues uninstalling
If you have issues uninstalling try running the below command

```dotnet new --debug:reinit```

### Project 
Includes swagger enabled by default @ http://RootURL/swagger/v1/swagger.json

Includes assembly scanning for dependency injection via autofac

Includes enforced HSTS security

Includes API versions example

Includes renovate to auto bump project dependencies
