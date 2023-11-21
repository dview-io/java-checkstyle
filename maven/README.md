# Configuring your maven project with Code Style
## Setup
Download both [dview_google_checks.xml](dview_google_checks.xml) and [checkstyle-suppressions.xml](checkstyle-suppressions.xml) and place them at root folder of your maven project.
```
project
|
|--src
|--target
|--pom.xml
|--checkstyle-suppressions.xml
|--dview_google_checks.xml

```
## Update your pom.xml
Add the following plugin configuration to your `pom.xml`:
```xml
<build>
  <plugins>
  <!-- Other existing plugins    -->
    <plugin>
      <artifactId>maven-checkstyle-plugin</artifactId>
      <groupId>org.apache.maven.plugins</groupId>
      <version>3.3.0</version>
      <dependencies>
        <dependency>
          <artifactId>checkstyle</artifactId>
          <groupId>com.puppycrawl.tools</groupId>
          <version>10.12.3</version>
        </dependency>
      </dependencies>
      <executions>
        <execution>
          <configuration>
            <configLocation>dview_google_checks.xml</configLocation>
            <consoleOutput>true</consoleOutput>
            <failOnViolation>true</failOnViolation>
            <includeTestSourceDirectory>false</includeTestSourceDirectory>
            <violationSeverity>warning</violationSeverity>
            <suppressionsLocation>checkstyle-suppressions.xml</suppressionsLocation>
            <suppressionsFileExpression>checkstyle.suppressions.file</suppressionsFileExpression>
          </configuration>
          <goals>
            <goal>check</goal>
          </goals>
          <id>checkstyle</id>
          <phase>validate</phase>
        </execution>
      </executions>
    </plugin>
  </plugins>
</build>
```