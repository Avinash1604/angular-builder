# CommandTestDemo

As an example, will create a builder that executes a shell command. and was generated with [Angular CLI](https://github.com/angular/angular-cli) version 9.1.0-rc.0.

## How to integrate custom builder to project 

import the local custom builder depedencies to package.json 

```
    "@devkit/command-runner": "file:../command-builder",
```

Please go to command builder directory and run - npm run build and go to command-test-demo directory to install custom builder dependencies- npm i 

Please add the below custom builder command to angular.json file 

```
   "shell-command": {
          "builder": "@devkit/command-runner:command",
          "options": {
            "command": "ls",
            "args": [
              "src/"
            ]
          }
```
## Test builder 
 ```
 ng run command-test-demo:touch 
  or
 ng run command-test-demo:shell-command --command=df
  ```
 ## References 
 https://angular.io/guide/cli-builder#creating-a-builder
 https://blog.angular.io/introducing-cli-builders-d012d4489f1b
 https://www.npmjs.com/package/@angular-builders/custom-webpack

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.


## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
