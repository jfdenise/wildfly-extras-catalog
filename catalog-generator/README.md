# WildFly catalog generator

## Build the project

`mvn clean install`

## Generate a catalog for a WildFly version

NOTE: By default the repository `wildfly-extras`, project `wildfly-catalog` and branch `main` are used. To generate locally the catalog, you can use your own fork and branch.

* `mvn exec:java -Dwildfly-version=<WildFly Version> [-Dgit_fork=<your fork>] [-Dgit_project_name=<your project name>] [-Dgit_branch=<your branch>`

* You then need to commit and push the generated json file `../docs/<wildfly version>/wildfly-catalog.json` in your forked branch. 

* You can then access the catalog by browsing the local file `../docs/<wildfly version>/index.html`

## Validate only

`mvn exec:java -Dwildfly-version=<WildFly Version> -DvalidateOnly=true`

