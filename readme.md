# Automation testing UI + API + DB with Cucumber Playwright (Javascript)

### Techstack:

- Developemnt language: Nodejs (Javascript)
- Framework: Playwright, Cucumber
- Database: MongoDB
- Reporter: Cucumber Reporter, Allure Reporter, Playwright trace
- CI/CD: Github Action

## Introduction

- The project combined both UI, API and DB automation testing for Milana Web Application

## Installation

- Use Node v20+ (should 20 in my suggestion)
- Install yarn
- Clone the project & run yarn install , yarn prepare

## Scripts

1. `yarn test-all-suites` (default of CI/CD) for run all tests with all emulation devices
2. `yarn clean-test-dev` for run all tests in Dev environment (UI + API + DB)
3. `yarn test-ui-dev:chrome` for run test UI with Playwright - Chrome
4. `yarn test-ui-dev:firefox` for run test UI with Playwright - Firefox
5. `yarn test-ui-dev:iPhone14` for run test UI with Playwright - IPhone14 Emulation
6. `yarn test-api-dev` for run test API using bundled Playwright API request
7. `yarn test-db-dev` for connect MongoDB and run DB testing (health check, query logic)

   ... and more in `package.json`

## Reporter

- After run local any tests, there will be 2 reporter generated: Cucumber and Allure

1. For Cucumber HTML report, just check the `test-results` folder
2. For Allure report, please run `yarn show-report` to display it

## CI/CD

- We are using Github Action CI CD

1. Test run automatically by the Github Runner
2. We can run workflow dynamically by specify the test command and run it from Github Action UI
3. After test finished, the Allure report will automatically real-time deploy using Github Page on:
   https://bsapac.github.io/PWA-automated-testing/
