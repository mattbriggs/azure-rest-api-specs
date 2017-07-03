# Web
    
> see https://aka.ms/autorest

This is the AutoRest configuration file for Web.


The App service RP comprises of services where each service has its own tag.
Hence, each sub-service has its own swagger spec. 

All of them are tied together using this configuration and are packaged together into one compute client library.
This makes it easier for customers to download one (nuget/npm/pip/maven/gem) compute client library package rather than installing individual packages for each sub service.


---
## Getting Started 
To build the SDK for Web, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration for generating APIs


---
#### Basic Information 
These are the global settings for the Web API.

``` yaml
# common 
title: Web
description: Web App Client
openapi-type: arm
tag: package-2016-09

```


# Tag: package-2016-09

These settings apply only when `--tag=package-2016-09` is specified on the command line.

``` yaml $(tag) == 'package-2016-09'
input-file:
- Microsoft.CertificateRegistration/2015-08-01/AppServiceCertificateOrders.json
- Microsoft.DomainRegistration/2015-04-01/Domains.json
- Microsoft.DomainRegistration/2015-04-01/TopLevelDomains.json
- Microsoft.Web/2016-03-01/Certificates.json
- Microsoft.Web/2016-03-01/DeletedWebApps.json
- Microsoft.Web/2016-03-01/Provider.json
- Microsoft.Web/2016-03-01/Recommendations.json
- Microsoft.Web/2016-03-01/ResourceProvider.json
- Microsoft.Web/2016-08-01/WebApps.json
- Microsoft.Web/2016-09-01/AppServiceEnvironments.json
- Microsoft.Web/2016-09-01/AppServicePlans.json

```
 
# Tag: package-2015-08-preview

These settings apply only when `--tag=package-2015-08-preview` is specified on the command line.

``` yaml $(tag) == 'package-2015-08-preview'
input-file:
- Microsoft.Web/2015-08-01/service.json
- Microsoft.Web/2015-08-01-preview/logicAppsManagementClient.json

```


---
#### Language-specific settings: CSharp

These settings apply only when `--csharp` is specified on the command line.

``` yaml $(csharp)
csharp:
  # override the default output folder
  output-folder: $(output-folder)/csharp
```
