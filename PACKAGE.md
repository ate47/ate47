[Back my profile...](https://github.com/ate47)

# Maven Packages <!-- omit in toc -->

**Table of contents**

- [Required repository](#required-repository)
	- [Maven code](#maven-code)
	- [Gradle code](#gradle-code)
- [Advanced Creative Tab 2](#advanced-creative-tab-2)
	- [Maven code](#maven-code-1)
	- [Gradle code](#gradle-code-1)

# Required repository

## Maven code


in your ~/.m2/settings.xml file.

```xml
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
                      http://maven.apache.org/xsd/settings-1.0.0.xsd">

  <activeProfiles>
    <activeProfile>github</activeProfile>
  </activeProfiles>

  <profiles>
    <profile>
      <id>github</id>
      <repositories>
        <repository>
          <id>github</id>
          <url>https://maven.pkg.github.com/ate47/ate47</url>
          <snapshots>
            <enabled>true</enabled>
          </snapshots>
        </repository>
      </repositories>
    </profile>
  </profiles>

  <servers>
    <server>
      <id>github</id>
      <username>USERNAME</username>
      <password>TOKEN</password>
    </server>
  </servers>
</settings>
```

Replace USERNAME and TOKEN with credentials from Github

in your pom.xml file.

```xml
<distributionManagement>
   <repository>
     <id>github</id>
     <name>Github ATE47</name>
     <url>https://maven.pkg.github.com/ate47/ate47</url>
   </repository>
</distributionManagement>
```

## Gradle code

```groovy
repositories {
    maven {
        url = "https://maven.pkg.github.com/ate47/ate47"
        credentials {
            username = System.getenv("GITHUB_USERNAME")
            password = System.getenv("GITHUB_TOKEN")
        }
    }
}
```

Set USERNAME and TOKEN in env variables with credentials from Github.

# Advanced Creative Tab 2

**[Open repository](https://github.com/ate47/AdvancedCreativeTab)**

## Maven code

```xml
<dependency>
  <groupId>fr.atesab</groupId>
  <artifactId>act</artifactId>
  <version>2.3.1-1.16</version>
</dependency>
```

## Gradle code

```groovy
dependencies {
    implementation 'fr.atesab:act:2.3.1-1.16'
}
```

