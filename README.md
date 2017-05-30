[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Build Status][travis-badge]][travis-badge-url]

![](./images/logo-paleblue-candara_357px.png)

Patra Web
==========================
* Creates a [Webjar](http://www.webjars.org/) containing the static content of [patra](https://indrabasak.github.io/patra/). 
Webjars is a convention for packaging client-side web libraries as JAR dependencies.
* The content is served from the the following url: `http://<host>:<port>/patra-ui.html`

Patra visualizes [Dropwizard Metrics](http://metrics.dropwizard.io/) in a user friendly way.

# Maven

The current version is `1.0.0`, which is compatible with [Patra 1.0.0](https://indrabasak.github.io/patra/). To use
the Patra Webjar, add the following dependency to your `pom.xml`.

```xml
<dependency>
    <groupId>com.github.indrabasak</groupId>
    <artifactId>patra-web</artifactId>
    <version>1.0.0</version>
</dependency>
```

# Build
* Check out the [project](https://github.com/indrabasak/patra-web).
* Execute the following Maven command from the parent directory:
```
mvn clean install
```
Once the build completes successfully, you should have `patra-web-1.0.0.jar` in the `target` folder.

The patra version is specified in the `pom.xml` where `patra.version` is the git tag on 
the [patra repo](https://github.com/indrabasak/patra).

# Usage
Spring Boot picks up the content of a webjars if the jar is detected in the classpath. Please see the 
[webjar documentation](http://www.webjars.org/documentation#springmvc) to find out more on how to configure a webjar 
with a Spring application.

The content of the `patra-web` webjar can be accessed from the following url: `http://<app host>:<app port>/patra-ui.html`

Please note that url for fetching the metric is `http://<app host>:<app port>/metrics/metrics`. If the metrics url is
different, change it in the `pom.xml` by modifying the _Renaming the metrics url_ step.

# License

The __Patra Web__ code is shared under the terms of [Apache License v2.0](https://opensource.org/licenses/Apache-2.0).

[travis-badge]: https://travis-ci.org/indrabasak/patra-web.svg?branch=master
[travis-badge-url]: https://travis-ci.org/indrabasak/patra-web
