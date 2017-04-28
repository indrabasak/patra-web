[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Build Status][travis-badge]][travis-badge-url]


Patra Web
==========================
* Creates a [Webjar](http://www.webjars.org/) containing the [patra](https://github.com/indrabasak/patra) static content. 
Webjars is a convention for packaging client-side web libraries as JAR dependencies.
* The content is served from the the following url: `http://<host>:<port>/patra-ui.html`

Patra allows you to visualize [Dropwizard Metrics](http://metrics.dropwizard.io/) in a user friendly way.

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
[webjar documentation] (http://www.webjars.org/documentation#springmvc) to find out more on how to configure a webjar 
with a Spring application.

The content of the `patra-web` webjar can be accessed from the following url: http:<host>:<port>/patra-ui.html

# License

The __Patra Web__ code is shared under the terms of [Apache License v2.0](https://opensource.org/licenses/Apache-2.0).

[travis-badge]: https://travis-ci.org/indrabasak/patra-web.svg?branch=master
[travis-badge-url]: https://travis-ci.org/indrabasak/patra-web
