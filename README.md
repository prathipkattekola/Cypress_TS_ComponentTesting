# Cypress_TS_ComponentTesting




**Step by Step Guide to Component Testing in Cypress**
**Prerequisites:**

Install NodeJS

Navigate to the NodeJS download page

Download the LTS version relevant to your operating system

Install the NodeJS

Install Visual Studio Code [optional but recommended]

Navigate to the Visual Studio Code download page,

https://code.visualstudio.com/download -  download, and install






**Understanding the Cypress Folder/File Structures**

**Components folder:** Contains Cypress component specs

**Fixtures folder:** Any data which can be used inside the specs can be placed here

**Support folder:** helper functions, utilities, any reusable code, and custom commands can be placed here.

**Support/component.js:** Great place to put the global configuration and reusable code

**Support/commands.js:** In this file, you can create custom commands or override existing commands

**Cypress.config.js:** This file contains runtime configurations such as devServer, framework, bundler, reporter, videos, screenshot options, etc.

**Package.json: **This file tracks all installed dependencies and allows you to create a custom commands shortcut






**Execute the Test to view the results**

Install the dependencies using the below command.

**npm install**

Open the Cypress with the below command

**npx cypress open –component**

Cypress Component Testing Tips and Tricks
•	Execute component Tests in headless mode. Cypress component testing can be executed in headless mode, using the Cypress CLI. The Cypress CLI executes the test faster. 

**npx cypress run --component**

•	Execute Cypress component tests, directly in the headed mode without manually selecting the test files. Generally, the headed tests are executed on the browser, by choosing the browser and selecting the tests on the test runner window. You can skip all these parts completely and directly execute the tests using the below command.

**npx cypress run --component --headed**

•	Open the test runner window directly by skipping the browser option. When you open the Cypress, every time you need to choose the test type as Component testing and then Browser as Chrome/Firefox/Edge, etc you can skip all these steps by specifying the open command options like below.

**npx cypress open --component --browser chrome**

•	Execute single component tests. When you have multiple tests you can execute the single spec using the –spec command line option.

**npx cypress run --component --spec cypress/component/DemoComponentTest.cy.jsx**

•	Use multiple configuration files in Cypress. You can have multiple configuration files in Cypress, while running the tests you can mention the configuration file name using the –config-file option.

**npx cypress run --component --config-file some.config.js**

•	Specify configuration command line. Generally, the configuration file is used to define the Cypress configuration, however, Cypress allows to specify the configuration in the command line using the –config option. 

**npx cypress run --component --config video=false**   

•	Test Reporter options. Cypress provides multiple reporter options such as Junit, XML, etc. You can specify the reporter using the –reporter option in Cypress

**npx cypress run --component --reporter junit**



