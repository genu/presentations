## Overview
Introduction to angular testing

## Resources
- [simple-frontend-boilerplate](https://github.com/genu/simple-frontend-boilerplate/tree/angular-testing-presentation)
- [Presentation](http://slides.com/genuchelu/angular-testing)

## More information
  - [Official Guides](https://docs.angularjs.org/guide/unit-testing)
  - [Full-Spectrum Testing](http://www.yearofmoo.com/2013/01/full-spectrum-testing-with-angularjs-and-karma.html)

## Outline
- About Me
- Game plan
  - High level view of testing
  - Types of tests
  - Testing specific to angular applications
  - Tooling
- High level view of testing
  - Why is testing important?
  - Benefits of writing unit tests
    - Prevent breaking changes
      - Catch breaking changes before your users do
    - Helps manage code better
      - Code integration is simplified. Developers can focus on interaction between units and rather than the individual units. (E2E)
    - Planning and predictability
      - The codebase becomes much more predictable when tests are present.
    - Reduce overall development costs
      - Detect bugs at a stage of the development lifecycle where they can't be corrected at a lower cost.
- Types of tests
  - Unit Testing
    - Code-level
      - You interact with the code directly. (i.e. call methods directly on the service you're testing)
    - Sandboxed and isolated
      - You focus only on that particular unit that you're testing.
      - Typically this involves bootstrapping a component so that it can be tested.
    - Fast
      - Tests can run in part or in full
  - E2E testing
    - Web-level
      - You interact with the components as an actual user would
    - Requires its own server
      - A browser instance is used simulate user actions
- Testing in Angular
  - Karma (Unit-testing)
    - Makes no assumption about how you write your tests
    - All it does is launches the web browser of your choice, loads the files you specifies, and reports the results of your tests.
  - Protractor (End to end testing)
- Setting up Karma
  - `npm install -g karma-cli`
  - `karma init`
  - Pitfalls
    - `Error: [$injector:modulerr]`
      Cause by not including required dependencies in `karma.conf.js`
  - Simple test
- Mocking a service
- Testing a directive
- Exercise: Filter spec
- Advanced
  - Spies
    - Concept of Jasmine
    - Essentially, it enables you to spy on functions, and assert various things about the function (was it called? what parameters were sent to the function, how many times was it called?)
    - Super useful for testing complex functions
  - Mocks
    - Mocking services is a very powerful feature. See official documentation for advanced usage of $httpBackend
  - Debugging tests
    - Tests can be debugged using the chrome developer tools
  - Tooling
    - Automate your unit tests with hooks
      - When accept code into repo only when tests pass.
      - Run tests when running a build
