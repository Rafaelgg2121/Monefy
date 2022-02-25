Cucumber BDD framework with Appium:

Money Mobile App

1. setup IntelliJ for cucumber

2. setup Maven 

3. Create new Maven project

4. Add Cucumber JVM and Cucumber-JUnit dependencies

https://cucumber.io/docs/installation/java/
https://cucumber.io/docs/cucumber/api/#junit

5. Add other dependencies: Appium, JSON, Log4J2
===============================================

6. Create Runner file: src/test/java/com/qa/runners/MyRunnerTest
========================
[glue, features]

7. Create feature files:
=========================== 
src/test/resources/Login.feature and Products.feature
Gherkin basics - https://cucumber.io/docs/gherkin/reference/

8. Create step defination files: 
================================
src/test/java/com/qa/stepdef: Login and Products
https://cucumber.io/docs/gherkin/step-organization/

9. Copy apps to src/test/resources/app
=====================================

10. Copy config.properties and log4j2.xml
=========================================

11. Copy TestUtils class to src/main/java/com/qa/utils
======================================================

12. Create hooks under src/test/java/stepdef
=============================================

13. Create GlobalParams under src/main/java/com/qa/utils
========================================================
platformName, udid, deviceName, systemPort,chromeDriverPort, wdaLocalPort, webkitDebugProxyPort

14. Initialize global params and add Thread Context for Log4j2 in Before hook
========================

15: Create ServerManager
===========================**

16. Start server in Before hook and stop service in After hook
=============================================================

17. Create PropertyManager
===========================

18. Create CapabilitiesManager
=============================

19. Create DriverManager
===========================

20. Initialize driver in Before hook and Quit in After hook (and set to null)
====================================

21. Add Base Page and Page Objects
===================================

22. Update step defination files with actual code
================================================

23. Execute Runner and "mvn test" with parameters
================================================
