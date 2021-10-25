# nodejs-testing-and-code-quality

Node.js: Testing and Code Quality

Most software engineers would agree that clean code is easier to maintain than messy code, but what exactly does that look like, and how do go about cleaning up messy code? In this course, Jon Peck shows how to measure quality, implement testing, and measure code coverage in your Node.js apps, using a complete but buggy restaurant booking application to illustrate the concepts. Jon first reviews JavaScript fundamentals and testing and code quality concepts. He then explains how to use linters to find suspicious code; explores different testing frameworks and their components; and shows how to isolate your code for testing using test doubles, then verify with spies and mocks. Jon wraps up the course by showing how to generate reports on code health across your entire codebase. Along the way, he provides challenge and solution videos so you can test your knowledge of each section before moving on.

[Link to project example this course](https://github.com/laissonsilveira/nodejs-testing-and-code-quality/tree/main/nadia)

## Capítulo: 1. Testing and Code Quality Fundamentals

-----------------------------------------------
### What is code quality?
-----------------------------------------------

Quality consists of those product features that meet the needs of customers and thereby provide product satisfaction.

Quality consists of freedom from deficiencis

Code maintainable:
- Can you maintain the code?
- Can someone else maintain without help?
- Can someone else read and understand the desing and intent?

Useful code:
- Flexible and reusable

Improving maintainability:
- Consistent formatting, logical naming (help reading)
- Clear comments and function docs (describes intent)
- Modular components (reusable code)

Code quality means:
- Meeting functional requirements
- Maintainable
- Useful in multiple places

-----------------------------------------------
### Coding conventions and standards
-----------------------------------------------

Coding convention:
- Programmin style (code readability)
- Practices (how to build and architect)
- Methods (how to plan and implement)

-----------------------------------------------
### Unit, integration, and functional testing
-----------------------------------------------

Unit test [smallest testable part of an application]:
- Procedural (entire module or individual function)
- Object-oriented (interface, like class or individual method)

* Tests isolated unit via API
* Perfomaed in memory
* Safe to run repeatedly
* Fast execution

Isolate behavior of tested unit and test your custom code, without third-party code e core code

Integration testing
- Builds on unit tests
- Combines and tests resulting combinations
- One system or cross-systems
- Uses full or partial environment (databases and services)
- More complex and hard to maintain

Functional testing:
- Focus in on result, not code (user interface)
- Check a specific feature (user workflow)
- Typically automated or manual
- Slower than unit and integration

-----------------------------------------------
### Testing frameworks
-----------------------------------------------

Test automation:
- Separate software from application
- Controls test execution
- Avoids repetitive tasks

Testing framework:
- defined how assertions are defined
- controls and interacts with tested application
- executes tests
- reports results

Test phases in a framework:
1. setup
2. execution
3. validation
4. cleanup

- Mocha (mochajs.org)
- Jasmine (jasmine.github.io)
- Jest (jestjs.io)

-----------------------------------------------
### TDD and BDD test specifications
-----------------------------------------------

TDD (Test-Driven Development):
- Software development process
- Requirements turned into test cases
- Software improved until tests pass

-----------------------------------------------
### Assertions for correctness
-----------------------------------------------

Assertion Library Examples:
- Assert (native in Node.js)
- Chai (chaijs.com)
- should.js (shouldjs.github.io)
- Built-in (Jasmine [matchers] and Jest [expect methods])

## Capítulo: 2. Finding Errors with Linting

-----------------------------------------------
### Standardizing with EditorConfig
-----------------------------------------------


Create editorconfig [editorconfig.org]
- Standardization to improve code quality
- Readable file format is self-documenting
- Free, open-source industry standard
- Flexible and configurable
- Available in the most text editors


-----------------------------------------------
### Adding EditorConfig to a project and IDE
-----------------------------------------------

editorconfig.org/#download

-----------------------------------------------
### Comparing JavaScript linters
-----------------------------------------------

Linters:
- JSLint
- JSHint
- ESLint

ESLint:
- Most popular
- Most flexible
- Lints and corrects formatting
- Best documentation

-----------------------------------------------
### Extending an ESLint shareable config
-----------------------------------------------

Shareable configs to Consider:
- eslint-config-airbnb [Airbnb JS and React Style Guide]
- eslint-config-standard [JavaScript Standard Sytle]
- eslint-config-google [Google JavaScript Style Guide]

github.com/dustinspecker/awesome-eslint

## Capítulo: 3. Validate Correctness with Unit Testing

-----------------------------------------------
### Survey of Node.js testing frameworks
-----------------------------------------------

Node.js Testing Frameworks
- AVA
- Jasmine
- Jest
- Mocha
- tape

AVA - avajs.dev
- Minimalist
- Includes assertions and TypeScript definitions
- Fast

Jasmine - jasmine.github.io
- Very popular
- (a)Synchronous test execution
- No external dependencies
- Include assertions, test doubles, and more
- Adds to global namespace

Jest - jestjs.io
- Incredibly popular
- Fast with asynchronous testin
- React support
- Includes test doubles
- Add to global namaspace
- Interactive watch

Mocha - mochajs.org
- Very popular, oldest
- (as)Synchronous test execution
- Flexible (plugins)
- Does not include assertion or mocks
- Add to global namespace
- File watcher

tape - github.com/substack/tape
- Minimalist (similar to AVA)
- Synchronous
- No setup or teardown methods
- Doesn't add to global namespace
- Explicitly state when tests are complete

-----------------------------------------------
### What and where to unit test?
-----------------------------------------------

Test Organization
- Structure tests (specs) inside of suites
 * describe function for scoping
 * Supports nesting
 * In Jest, file is implicit suite

Example:
 * Describe (suite): Validator

## Capítulo: 4. Replacing and Inspecting Using Spies, Stubs, and Mocks

-----------------------------------------------
### Replacing code with test doubles
-----------------------------------------------

Further Reading on Test Doubles
* xunitpatterns.com/Test%20Double.html
* martinfowler.com/bliki/TestDouble.html

## Capítulo: 5. Reporting on Your Entire Codebase

-----------------------------------------------
### Why code coverage matters
-----------------------------------------------

Why does code coverage matther?
* Higher covarage reduces risk of bugs
* Highlights unsed of untested pieces of code
* Indicator of code quality
* Requirement in some industries

Type of coverage
* Statements - proportion of executed statements
* Branches - proportion of branches
* Functions - proportion of called defined funcions
* Lines - proportion of executed lines

Statement (developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements)

Each statement in a conditional
if (condition) {
  statement1(); //BRANCH 1
} else {
  statement2(); //BRANCH 2
  statement3();
}

-----------------------------------------------
### Measuring code coverage with Jest
-----------------------------------------------

VSCode extension do display coverage:
* Coverage Gutters


-----------------------------------------------
### Functional testing with Jest
-----------------------------------------------

Functional Testing Tools
* Selenium WebDriver - selenium.dev
  * Nightwatch.js - nightwatchjs.org
  * WebdriverIO - webdriver.io
* SuperAgent - visionmedia.github.io/superagent
  * SuperTest - github.com/visionmedia/supertest

-----------------------------------------------
### Form submissions with SuperTest
-----------------------------------------------

cheerio.js.org

-----------------------------------------------
### Coverage with continuous integration
-----------------------------------------------

Open-Source Continuous Integration
- Jenkins
- Buildbot
- Spinnaker

CI as a Service
* GitHub (actions) - github.com
* GitLab (CI/CD) - gitlab.com
* Bitbucket (pipelines) - bitbucket.org

* CircleCI - circleci.com
* Travis CI - travis-ci.com