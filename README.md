## Installation

### Maven
To use cucumber-jvm-clojure in your project, add the following dependency to your `pom.xml`:
```xml
<dependency>
    <groupId>io.cucumber</groupId>
    <artifactId>cucumber-jruby</artifactId>
    <version>{{% version "jruby" %}}</version>
    <scope>test</scope>
</dependency>
```

## Using JRuby

Run the features:

```
jruby bin/cucumber-jvm --glue src/test/resources src/test/resources
```

### Customizing JRuby

You can define `GEM_PATH` to tell JRuby where to load gems from.

These values can be defined in any of the three places:

* In an Environment variable
* In a System property (for example `-DGEM_PATH=src/test/gems`
* In a `cucumber.properties` properties file on your `CLASSPATH`.

Sample `cucumber.properties` file:

```
GEM_PATH=${basedir}/src/test/gems
```
