# 04-themenausarbeitung-container-image-jib


This tutorial will teach you how to make a Java image with a quarkus project using JIB.

## Generate a project with following command

This project contains a simple REST service qith QUTE.

mvn io.quarkus.platform:quarkus-maven-plugin:2.7.0.Final:create \
    -DprojectGroupId=at.htl \
    -DprojectArtifactId=persons \
    -Dextensions="quarkus-resteasy-qute" \
    -Dextensions="quarkus-container-image-jib"

