## Running cypress project from command line interface

Firstly, open command line inside the cypress project

Run `npx cypress run` to execute all the test cases inside the integration / e2e folder
This command will run all the scripts, create screenshots and videos of the test execution.

For more info: run `npx cypress run --help` to see all other commands you can use

Examples: `npx cypress run --browser chrome` <= This will set the test browser to chrome instead of the default electron. We can use firefox,edge and brave too

`npx cypress run --spec locnOfSpec.js` 

`npx cypress run -b chrome -s locnOfSpec.js`, here we set the browser type to chrome, we provided a specific test / spec file to run otherwise it runs all the spec files inside the integration/e2e folder

## Setting configurations from command line

`npx cypress run --config watchForFileChanges=false, defaultCommandTimeout=5433, -b edge -s locOfSpec.js `
use , to add more config parameter
e.g npx cypress run --config watchForFileChanges=false, defaultCommandTimeout=2444 -b edge -s .\cypress\e2e\login_test_cases.cy.js
Here, our spec file is inside the e2e folder