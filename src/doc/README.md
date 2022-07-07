<!-- ${doc.msg.generated} -->
<!--
  After editing the source file or changing pom.xml, run at project root:
  mvn resources:copy-resources@readme
-->

# fmi-avi-messageconverter-bom

The [Bill of Materials (BOM)](https://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html#Bill_of_Materials_BOM_POMs)
for the _fmi-avi-messageconverter_ library artifacts providing compatible versions:

* [fmi-avi-messageconverter](https://github.com/fmidev/fmi-avi-messageconverter)
  ([v${fmi-avi-messageconverter.version}](https://github.com/fmidev/fmi-avi-messageconverter/releases/tag/fmi-avi-messageconverter-${fmi-avi-messageconverter.version}))
* [fmi-avi-messageconverter-iwxxm](https://github.com/fmidev/fmi-avi-messageconverter-iwxxm)
  ([v${fmi-avi-messageconverter-iwxxm.version}](https://github.com/fmidev/fmi-avi-messageconverter-iwxxm/releases/tag/fmi-avi-messageconverter-iwxxm-${fmi-avi-messageconverter-iwxxm.version}))
* [fmi-avi-messageconverter-tac](https://github.com/fmidev/fmi-avi-messageconverter-tac)
  ([v${fmi-avi-messageconverter-tac.version}](https://github.com/fmidev/fmi-avi-messageconverter-tac/releases/tag/fmi-avi-messageconverter-tac-${fmi-avi-messageconverter-tac.version}))

## Using the BOM

These projects is available as maven dependencies in the FMI OS maven repository. To access them, add this repository to
your project pom, or in your settings:

```xml
<repositories>
  <repository>
    <id>fmi-os-mvn-release-repo</id>
    <url>https://raw.githubusercontent.com/fmidev/fmi-os-mvn-repo/master</url>
    <snapshots>
      <enabled>false</enabled>
    </snapshots>
    <releases>
      <enabled>true</enabled>
      <updatePolicy>daily</updatePolicy>
    </releases>
  </repository>
</repositories>
```

Import this bom in the `<dependencyManagement>` section of your pom.xml:

```xml
<dependencyManagement>
  <dependencies>
    <dependency>
      <groupId>fi.fmi.avi.converter</groupId>
      <artifactId>fmi-avi-messageconverter-bom</artifactId>
      <version>${project.version}</version>
      <type>pom</type>
      <scope>import</scope>
    </dependency>
  </dependencies>
</dependencyManagement>
```

Then add your dependencies without a `<version>`:

```xml
<dependencies>
  <dependency>
    <groupId>fi.fmi.avi.converter</groupId>
    <artifactId>fmi-avi-messageconverter</artifactId>
  </dependency>
  <!-- ... -->
</dependencies>
```

## BOM versioning scheme

This BOM uses semantic versioning (`major.minor.patch`).

1. The `major` version is incremented on a major version update of any of provided artifacts.
2. Otherwise the `minor` version is incremented on a minor version update of any of provided artifacts.
3. Otherwise the `patch` version is incremented on a patch version update of any of provided artifacts.
