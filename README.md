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

**Automated cases:**
This cases where automated according to their importance tu run a happy path

Test cases for Monefy
1-	Validate you can add income
Steps:
Access the app monefy, hit ‘Income’, type a number ‘1500’, add a note, then hit choose category, hit ‘Deposits’. 
Expected results:
The income will be added to the list of incomes and the chart will show it

2 – Validate you can add expense
Steps:
Access the app monefy, hit ‘Expense, type a number ‘500’, add a note, then hit choose category, hit ‘Deposits’. 
Expected results:
The expense will be added to the list of incomes and the chart will show it
3 – validate you can add an expense by directly hitting the icon
Steps:
On the main screen, choose the hit the Car figure, you will be prompted to digit quantity and notes, insert 2000 and a note, hit ‘Add car’ icon
4- try to add an empty income
Steps:
On the main screen hit income and then just hit choose category
Expected results:
Screen with quantity should blink red and it does not allow you to add the empty income
5- Confirm that the balance is right
Steps:
On the main screen hit ‘Balance’ button, will get a list of everything you have added where:
 Incomes – Expenses = Balance
Expected results:
On this screen we confirm Incomes – Expenses = Balance if incomes > expenses the button will be green, but if Incomes < expenses the button will be red, and the balance will be negative
6- Confirm search button is working fine
Steps:
On the main screen hit the search button, type one of the criteria you have added EG: Eating out
Expected results:
You should get the expense on screen with the date you registered it 



