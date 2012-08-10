This is an fork of the [github-maven-example](http://kevinsawicki.github.com/github-maven-example)
project that uses the [GitHub Maven Plugins](https://github.com/github/maven-plugins).

This forked version supported multimodule maven build for eclipse plugins with features and update site hosted at github.

See the [POM file](https://github.com/funthomas424242/github-maven-example/blob/master/example/pom.xml)
for how the downloads plugin and site plugin are configured.

# Getting started

* Fork this project
* Update the `pom.xml` file `<url>` element to be the address of your fork
* Optionally update `<scm>` and `<developers>` section as well to have the information for your fork
* Add the following to your Maven `settings.xml` file (update with your GitHub login name and password):

```xml
<profiles>
  <profile>
    <id>github</id>
    <properties>
      <github.global.userName>user</github.global.userName>
      <github.global.password>password</github.global.password>
    </properties>
  </profile>  
</profiles>

<activeProfiles>
  <activeProfile>github</activeProfile>
</activeProfiles>
```

# Using the downloads plugin

```
$ cd github-maven-example/example
$ mvn clean install
```

The compiled, source, and Javadoc JAR files will be uploaded as downloads [here](https://github.com/funthomas424242/github-maven-example/downloads).

# Using the site plugin

```
$ cd github-maven-example/example
$ mvn site
```

The generated site will be committed to the [gh-pages branch](https://github.com/funthomas424242/github-maven-example/tree/gh-pages) and visible [here](http://funthomas424242.github.com/github-maven-example/).
