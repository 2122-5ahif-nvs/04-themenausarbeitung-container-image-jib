# 04-themenausarbeitung-container-image-jib


This tutorial will teach you how to make a Java image with a quarkus project using JIB.

## Generate a project with following command

This project contains a simple REST service qith QUTE.

````
mvn io.quarkus.platform:quarkus-maven-plugin:2.7.0.Final:create -DprojectGroupId=at.htl -DprojectArtifactId=persons -Dextensions="resteasy-qute" -Dextensions="container-image-jib"
````

Go into the project
````
cd persons
````


Add to application.properties

```
quarkus.container-image.username=<username>
quarkus.container-image.password=<password>

quarkus.container-image.registry=<where you want to have your image e.g: docker.io>
quarkus.container-image.group=<name of group> 
quarkus.container-image.name=<name>
quarkus.container-image.push=true
```

then you have to login so execute following command

````
docker login <where you want to have your image e.g: docker.io>
````

then execute following command to build image

````
mvn clean package
````

After this Tutorial you should have an image created. Now you can use it.


