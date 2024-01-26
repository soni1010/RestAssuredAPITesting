## Spark & Pdf Extent Report generation for REST Assured API Testing

This [artifact](http://ghchirp.site/3791/) deals with the creation of Spark and Pdf Extent Report for REST Assured validation by using a Maven Plugin. The artifact uses the REST Assured Filter from the Allure Framework for generating the report data. This works with JUnit 4, JUnit 5 and TestNG testing frameworks. This avoids the mixing of Extent Report calls within the test code. All that is required in the code is an addition of a REST Assured filter. The remaining changes are all POM configuration changes.

For more details refer to this [article](http://ghchirp.site/3791/). Sample usages for [JUnit4](https://github.com/grasshopper7/rest-assured-report-junit4), [JUnit5](https://github.com/grasshopper7/rest-assured-report-junit5), [TestNG](https://github.com/grasshopper7/rest-assured-report-testng).

**Dependencies** - [Rest Assured](https://mvnrepository.com/artifact/io.rest-assured/rest-assured), [Extent Allure Annotations](https://mvnrepository.com/artifact/tech.grasshopper/extentreport-allure-annotation), Allure Rest Assured ([JUnit4](https://mvnrepository.com/artifact/io.qameta.allure/allure-junit4) or [JUnit5](https://mvnrepository.com/artifact/io.qameta.allure/allure-junit5) or [TestNG](https://mvnrepository.com/artifact/io.qameta.allure/allure-testng)) & Testing Framework (JUnit4 or JUnit5 or TestNG). POM for [JUnit4](https://github.com/grasshopper7/rest-assured-report-junit4/blob/ef35adc7b4fbf6405be99ecdeafb2ec3d289fc4e/pom.xml#L17), [JUnit5](https://github.com/grasshopper7/rest-assured-report-junit5/blob/2d22fe62a188f887412c8cc0e046b9fbcd7619f0/pom.xml#L17), [TestNG](https://github.com/grasshopper7/rest-assured-report-testng/blob/142f30dd6dab040f1b63a70470238915813c0378/pom.xml#L16).

**Maven Failsafe Plugin Configuration** - Plugin configurations for [JUnit4](https://github.com/grasshopper7/rest-assured-report-junit4/blob/ef35adc7b4fbf6405be99ecdeafb2ec3d289fc4e/pom.xml#L74), [JUnit5](https://github.com/grasshopper7/rest-assured-report-junit5/blob/2d22fe62a188f887412c8cc0e046b9fbcd7619f0/pom.xml#L67), [TestNG](https://github.com/grasshopper7/rest-assured-report-testng/blob/142f30dd6dab040f1b63a70470238915813c0378/pom.xml#L61).

**Report Plugin** -
```
<plugin>
  <groupId>tech.grasshopper</groupId>
  <artifactId>rest-assured-extent-report-plugin</artifactId>
  <version>2.1.2</version>
  <executions>
    <execution>
      <id>report</id>
      <phase>post-integration-test</phase>
      <goals>
        <goal>extentreport</goal>
      </goals>
    </execution>
  </executions>
</plugin>
```
Default configuration details and tips be modify them can be found in the [article](http://ghchirp.site/3791/). For more details refer to the relevant POM - [JUnit4](https://github.com/grasshopper7/rest-assured-report-junit4/blob/master/pom.xml), [JUnit5](https://github.com/grasshopper7/rest-assured-report-junit5/blob/master/pom.xml), [TestNG](https://github.com/grasshopper7/rest-assured-report-testng/blob/master/pom.xml).

***Pdf Report Images*** - 

*Dashboard*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/ra-db.png)

*Tests*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/ra-tests.png)

*Attributes*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/ra-attributes.png)

*Exception*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/ra-exception.png)

*Category*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/ra-category.png)

*Author*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/ra-author.png)

*Device*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/ra-device.png)

***Spark Report Images*** - 

*Dashboard*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/dashboard.png)

*Tests*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/tests.png)

*Exception*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/exception.png)

*Category*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/category.png)

*Author*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/author.png)

*Device*

![sample](https://raw.githubusercontent.com/grasshopper7/rest-assured-extent-report-plugin/master/images/device.png)
