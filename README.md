# Java Cucumber Selenium Framework

## Purpose

Illustrate how to implement classic BDD features:

- Variables in steps - [link](https://github.com/andreasneuber/java-cucumber-selenium-framework/blob/master/src/test/resources/features/ConvertCelsius.feature)
- Horizontal data tables - [link](https://github.com/andreasneuber/java-cucumber-selenium-framework/blob/master/src/test/resources/features/Login.feature)
- Vertical data tables - [link](https://github.com/andreasneuber/java-cucumber-selenium-framework/blob/master/src/test/resources/features/ProvideYourDetails.feature)
- Scenarios with Examples - [link](https://github.com/andreasneuber/java-cucumber-selenium-framework/blob/master/src/test/resources/features/Creditcard.feature)
- Backgrounds - [link](https://github.com/andreasneuber/java-cucumber-selenium-framework/blob/master/src/test/resources/features/AdminPrivileges.feature)
- Setup hook
- Teardown hook
- Tags
- Reports
- Screenshots
- Parallel execution
- Page objects

## IDE used here in this docu

IntelliJ IDEA Community Edition

## Application under test

The tests here were written to
fit [https://github.com/andreasneuber/automatic-test-sample-site](https://github.com/andreasneuber/automatic-test-sample-site)

README in this project explains how to start the sample site.

## Setup

Setup Maven, otherwise `mvn` commands below cannot be executed.
See [https://maven.apache.org/install.html](https://maven.apache.org/install.html)

## How to execute the tests

**Way 1:**
Run this command in your terminal (Mac/Linux/UNIX) or CMD (Windows):

```
mvn test
```

or

```
mvn clean verify
```

or with providing options (which also override what is set in the TestRunner file)

```
mvn test -D"cucumber.filter.tags=@Login"
```

After this you will see 2 new folders - target and test-output.
Directory test-output contains Spark test report.

**Way 2:**
Through IntelliJ UI. Right-click on project name, then choose "Run > (NG) All Tests"


## Update Maven packages

`mvn clean install -U`

## Principles for accomplishing good design

1) No driver invocation in step definitions
2) No instantiation of page objects and generic utils in step definitions (so no code like `xyz = new Class()` )
3) Follow official Java naming conventions - https://www.thoughtco.com/using-java-naming-conventions-2034199

