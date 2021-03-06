This example demonstrates how to analyze a project with Maven reusing JUnit and JaCoCo reports.
There are two options:
* do not activate the JaCoCo JUnit listener => no information about unit tests covering each covered line
* activate the JaCoCo JUnit listener => information about unit tests covering each covered line (only available for Sonar 3.5+)

Prerequisites
=============
* [Sonar](http://www.sonarsource.org/downloads/) 3.4 or higher
* Maven 2.2.1 or higher

Usage for version 3.4+ (do not activate the JaCoCo JUnit listener)
==================================================================
* Build the project:

        mvn clean install

* Analyze the project with Sonar using Maven:

        mvn sonar:sonar

Usage for version 3.5+ (activate the JaCoCo JUnit listener)
===========================================================
* Build the project:

        mvn clean install

* Analyze the project with Sonar using Maven:

        mvn sonar:sonar -Pcoverage-per-test
