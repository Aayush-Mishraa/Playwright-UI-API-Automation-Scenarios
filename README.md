# Playwright Automation

A hands-on Playwright workspace that grows from basic UI checks to advanced UI + API scenarios. I use it as a learning sandbox and a quick place to validate ideas before moving them into real projects.

## Quick start

1) Install dependencies

```
npm install
npx playwright install
```

2) Run a few tests

```
# run everything under tests
npx playwright test

# run a folder
npx playwright test tests/testAllSenarios
npx playwright test tests/testlogics

# run api tests only
npx playwright test tests/testAllSenarios/apis
```

3) Open the report

```
# after a run
npx playwright show-report
```

## Configs

- playwright.config.js
  - Headed Chromium, screenshots only on failure, traces retained on failure.
- playwright.config2.ts
  - Multi-browser projects with standard Playwright defaults.

You can switch configs like this:

```
npx playwright test --config playwright.config2.ts
```

## Folder map

- tests/testAllSenarios
  - Main learning track: basic to advanced UI + API topics.
- tests/testAllSenarios/apis
  - API-only suites.
- tests/testlogics
  - Focused automation patterns and demo flows.
- tests/utils
  - Reusable helpers.
- auth
  - Storage state and session data.
- playwright-report, test-results
  - Playwright HTML report and raw artifacts.

## Scenario index (basic to advanced)

### tests/testAllSenarios

- app.spec.ts - basic app flow and smoke checks.
- assertions.spec.ts - expect and assertion patterns.
- backandforward.spec.ts - browser navigation history.
- browsercontext.spec.ts - multiple contexts and isolation.
- calendar.spec.ts - date picker interactions.
- customFixture.spec.ts - custom fixture setup and usage.
- datadriveFaker.spec.ts - faker-driven input data.
- datadrivenExcel.spec.ts - data driven tests with Excel.
- dataprovider.spec.ts - data provider basics.
- dataproviderCSV.spec.ts - CSV based data provider.
- dataproviderjson.spec.ts - JSON based data provider.
- describe.spec.ts - describe blocks and grouping.
- google.core.spec.ts - core search flow with Google.
- google.spec.ts - UI search checks on Google.
- hooks.spec.ts - before/after hooks.
- hooksinsidedecribe.spec.ts - hooks inside describe blocks.
- InBuiltFixture.spec.ts - built-in Playwright fixtures.
- launchurl.spec.ts - launch and basic navigation.
- loginpage.spec.ts - login page flow.
- mytest.spec.ts - mixed sample tests.
- myutil.spec.ts - helper usage in tests.
- productinfo.spec.ts - product page validations.
- regfix.spec.ts - regex locator or fix-up examples.
- register.spec.ts - registration flow.
- retry.spec.ts - retry behavior.
- search.spec.ts - search flow validations.
- serialrun.spec.ts - serial execution patterns.
- sessiontest.spec.ts - session handling.
- storage-session.spec.ts - storage state reuse.
- webtablepagination.spec.ts - table pagination logic.

### tests/testAllSenarios/apis

- basicauth.spec.ts - basic auth coverage.
- gorest.spec.ts - GoRest API basics.
- gorest_crud.spec.ts - GoRest CRUD flow.
- gorest_e2e.spec.ts - GoRest end-to-end.
- network_monitoring.spec.ts - network monitoring in API tests.
- product_jsonpath.spec.ts - JSONPath validation.
- schema_validation.spec.ts - schema validation checks.
- spotify_oauth2.spec.ts - OAuth2 token flow.

### tests/testlogics

- APITest.spec.ts - API test fundamentals.
- BrowserContext.spec.ts - context and isolation demos.
- CalenderUISenario.spec.js - calendar UI scenario.
- ChildParentWindow.spec.js - window and tab handling.
- ClientAPP.spec.js - client app flow checks.
- DownloadAndUploadSenario.spec.js - upload and download flows.
- E2EAPITest.spec.ts - API end-to-end test.
- EndToEndTest_UsingGetBy.spec.js - E2E flow using getBy locators.
- EndToEnd_WebAutomationPractice.spec.js - E2E practice flow.
- gorest_e2e.spec.ts - GoRest end-to-end API.
- LocateElement_Using_GetBy.spec.js - locator strategies with getBy.
- NetworkTest.spec.js - network intercept or listen basics.
- NetworkTest2.spec.js - network scenario two.
- NetworkTest3.spec.js - network scenario three.
- product_jsonpath.spec.ts - JSONPath validations.
- RadioButton_CheckBoxesUI.spec.js - radio and checkbox controls.
- ScreenshotAndVisualComperation.spec.js - visual comparison.
- UIBasictest.spec.js - basic UI actions.
- WebAPIOopsPart1.spec.js - API design with OOP style.
- WebAPIPart1.spec.js - API basics and patterns.

## Helpers

- tests/utils/APIutils.js - API helper functions.
- tests/utils/ElementUtil.ts - element and locator helpers.

## Notes

- package.json includes a sample script that runs one spec in headed mode. Use the CLI examples above for full control.
- If you are reusing session state, keep auth/session.json updated.
