# browserbase-cypress-runner

<p align="center">
  <img width="460" height="300" src="https://raw.githubusercontent.com/Browserbase/browserbase-cypress-runner/master/bb_heart_cypress.png">
</p>

A wrapper for cypress that allows you to run cypress tests in paralell on the Browserbase platform.

Check us out at https://browserbase.io

## Usage
Simply install browserbase-cypress-runner using npm 

```
npm i browserbase-cypress-runner
```

and then copy the example config file with your configuration, and then run

```
npx browserbase-cypress-runner
```

You can also override the config file by passing command line arguments

```
npx browserbase-cypress-runner --paralell 10 --spec integration/example
```

## Config 
In the base of this repo there is an example config file that is required in order to run Cypress tests.

```json
{
    "org": "11111111-2222-3333-4444-5555555555",      // Org is used to specify the Browserbse Organization ID you want to run the tests using 
    "path": "example-site/",                          // path is the relative path to the folder containing cypress.json
    "paralell": 10,                                   // paralell is the number of paralell tests to run
    "additional-dependencies": ["faker", "moment"],   // additional-dependencies allows you to instlal other npm packages before the test starts
    "specs": "integration"                            // specs is the folder containing the spec files you want to run
}
```