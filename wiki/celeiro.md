---
layout: wiki
title: Celeiro
comments: false
toc: true
editurl: wiki/celeiro.md
---

# Resources
* [http://www.jaxio.com/documentation/celerio/index.html](http://www.jaxio.com/documentation/celerio/index.html)
* [http://www.springfuse.com/documentation/pdf/springfuse.pdf](http://www.springfuse.com/documentation/pdf/springfuse.pdf)

# Custom pack

## Howto change location of well known files:

Some predefined generated file types have fixed paths like java. In order to change them edit `celerio-maven-plugin.xml` and add in `configuration` section:

```xml
<celerio >
    <configuration>
        <conventions>
            <wellKnownFolders>
                <wellKnownFolder wellKnownFolder="JAVA" folder="./middleware/src/main/java"
                                 generatedFolder="./middleware/src/main/generated-java"/>
            </wellKnownFolders>
        </conventions>
    </configuration>
</celerio>
```

## Howto override header comment

Edit `celerio-maven-plugin.xml` and add in `configuration` section:

```xml
<celerio>
    <configuration>
        <headerComment>
            <lines>
                <line>created by: Piotr Kosmowski</line>
            </lines>
        </headerComment>
    </configuration>
</celerio>
```

