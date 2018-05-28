# GantSign PMD Configuration

PMD configuration for Java code written by GantSign.

## Configuration

To use this PMD configuration add the following to your POM:

```xml
<project>
  ...
  <properties>
    <pmd.version>6.2.0</pmd.version>
  </properties>
  ...
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-pmd-plugin</artifactId>
        <version>3.9.0</version>
        <configuration>
          <rulesets>
            <ruleset>gantsign-pmd-config.xml</ruleset>
          </rulesets>
        </configuration>
        <executions>
          <execution>
            <goals>
              <goal>check</goal>
            </goals>
          </execution>
        </executions>
        <dependencies>
          <dependency>
            <groupId>net.sourceforge.pmd</groupId>
            <artifactId>pmd-core</artifactId>
            <version>${pmd.version}</version>
          </dependency>
          <dependency>
            <groupId>net.sourceforge.pmd</groupId>
            <artifactId>pmd-java</artifactId>
            <version>${pmd.version}</version>
          </dependency>
          <dependency>
            <groupId>net.sourceforge.pmd</groupId>
            <artifactId>pmd-javascript</artifactId>
            <version>${pmd.version}</version>
          </dependency>
          <dependency>
            <groupId>net.sourceforge.pmd</groupId>
            <artifactId>pmd-jsp</artifactId>
            <version>${pmd.version}</version>
          </dependency>
          <dependency>
            <groupId>com.github.gantsign.pmd</groupId>
            <artifactId>pmd-config</artifactId>
            <version>@enter.version.here@</version>
          </dependency>
        </dependencies>
      </plugin>
    </plugins>
  </build>
  ...
  <pluginRepositories>
    <pluginRepository>
      <snapshots>
        <enabled>false</enabled>
      </snapshots>
      <id>bintray-gantsign-maven</id>
      <name>bintray-gantsign-plugins</name>
      <url>https://dl.bintray.com/gantsign/maven</url>
    </pluginRepository>
  </pluginRepositories>
  ...
</project>
```

## License

This software is licensed under the terms in the file named "[LICENSE](LICENSE)"
in the root directory of this project.

## Author Information

John Freeman

GantSign Ltd.
Company No. 06109112 (registered in England)
