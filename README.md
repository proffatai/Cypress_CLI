## Running cypress project from command line interface

Firstly, open command line inside the cypress project

Run `npx cypress run` to execute all the test cases inside the integration / e2e folder
This command will run all the scripts, create screenshots and videos of the test execution.

For more info: run `npx cypress run --help` to see all other commands you can use

Examples: `npx cypress run --browser chrome` <= This will set the test browser to chrome instead of the default electron. We can use firefox,edge and brave too

`npx cypress run --spec locnOfSpec.js`  
NB: location of the spec file is easy and should start from the cypress folder. E.g, say we have our spec file in the root of the integration folder, we can say: npx cypress run --spec cypress/integration/specName.js
Do not include the path in a double quote, write it directly

`npx cypress run -b chrome -s locnOfSpec.js --e2e`, here we set the browser type to chrome, we provided a specific test / spec file to run and also stated we wanted to perform e2e, otherwise it runs all the spec files inside the integration/e2e folder

## Setting configurations from command line

`npx cypress run --config watchForFileChanges=false, defaultCommandTimeout=5433, -b edge -s locOfSpec.js `
use , to add more config parameter
e.g npx cypress run --config watchForFileChanges=false, defaultCommandTimeout=2444 -b edge -s .\cypress\e2e\login_test_cases.cy.js
Here, our spec file is inside the e2e folder

## To verify that cypress was installed properly
`npx cypress verify`

## Analyzing package.json file

When we run the command `npm init -y`, the package.json file is created to help us handle and manage all node packages we use in our project.

Below shows a sample
{
  "name": "cypress_cli",  // name of the project, max acceptabele characters=214, must not start with . or _ and cant contain uppercase letter
  "version": "1.0.0",
  "description": "Firstly, open command line inside the cypress project", // we can provide more description about the project here
  "main": "index.js", we specify the main js file
  "scripts": { // script section where we can create custom commands
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/proffatai/Cypress_CLI.git"
  },
  "keywords": [], // Array of strings and it is provided so people can easily locate our project online
  "author": "", // the name of the author
  "license": "ISC",
   "dependencies": { // this holds all the dependencies / packages we used in this project. THis allows others to just run npm install and all the dependencies with the exact version used in the project gets installed
    "cypress": "^10.4.0"
  },
  "bugs": {
    "url": "https://github.com/proffatai/Cypress_CLI/issues"
  },
  "homepage": "https://github.com/proffatai/Cypress_CLI#readme"
}
