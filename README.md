Java class model API for Predictive Model Markup Language (PMML).

# Features #

* Full support for PMML 3.0, 3.1, 3.2, 4.0 and 4.1 schemas:
  * Class hierarchy.
  * Schema version annotations.
* Fluent API:
  * Value constructors.
* SAX Locator information
* [Visitor pattern] (http://en.wikipedia.org/wiki/Visitor_pattern):
  * Validation agents.
  * Optimization and transformation agents.

# Installation #

JPMML library JAR files (together with accompanying Java source and Javadocs JAR files) are released via [Maven Central Repository] (http://repo1.maven.org/maven2/org/jpmml/). Please join the [JPMML mailing list] (https://groups.google.com/forum/#!forum/jpmml) for release announcements.

The current version is **1.0.22** (17 February, 2014).

```xml
<!-- Class model classes -->
<dependency>
	<groupId>org.jpmml</groupId>
	<artifactId>pmml-model</artifactId>
	<version>${jpmml.version}</version>
</dependency>
<!-- Class model annotations -->
<dependency>
	<groupId>org.jpmml</groupId>
	<artifactId>pmml-schema</artifactId>
	<version>${jpmml.version}</version>
</dependency>
```

# Usage #

The class model consists of two types of classes. There is a small number of manually crafted classes that are used for structuring the class hierarchy. They are permanently stored in the Java sources directory `/pmml-model/src/main/java`. Additionally, there is a much greater number of automatically generated classes that represent actual PMML elements. They can be found in the generated Java sources directory `/pmml-model/target/generated-sources/xjc` after a successful build operation.

All class model classes descend from class `org.dmg.pmml.PMMLObject`. Additional class hierarchy levels, if any, represent common behaviour and/or features. For example, all model classes descend from class `org.dmg.pmml.Model`.

There is not much documentation accompanying class model classes. The application developer should consult with the [PMML specification] (http://www.dmg.org/v4-1/GeneralStructure.html) about individual PMML elements and attributes.

# Contact and Support #

Please use the e-mail displayed at [GitHub profile page] (https://github.com/jpmml)