# Test info

- Name: Login Test with JSON Data: Invalid login @datadriven
- Location: C:\Automation\opencartplaywright\tests\LoginDataDriven.spec.ts:17:8

# Error details

```
Error: page.goto: Test timeout of 30000ms exceeded.
Call log:
  - navigating to "https://tutorialsninja.com/demo/", waiting until "load"

    at C:\Automation\opencartplaywright\tests\LoginDataDriven.spec.ts:20:20
```

# Test source

```ts
   1 | import { test, expect } from '@playwright/test';
   2 | import { LoginPage } from '../pages/LoginPage';
   3 | import { MyAccountPage } from '../pages/MyAccountPage';
   4 | import { DataProvider } from '../utils/dataProvider';
   5 | import { TestConfig } from '../test.config';
   6 | import { HomePage } from '../pages/HomePage';
   7 |
   8 |
   9 | //Load JSON test data logindata.json
  10 |
  11 | const jsonPath="testdata/logindata.json";
  12 | const jsonTestData=DataProvider.getTestDataFromJson(jsonPath);
  13 |
  14 |
  15 | for(const data of jsonTestData)
  16 | {
  17 |    test(`Login Test with JSON Data: ${data.testName} @datadriven`, async({page})=>{
  18 |
  19 |         const config = new TestConfig(); // create instance
> 20 |         await page.goto(config.appUrl);    // getting appURL from test.config.ts file
     |                    ^ Error: page.goto: Test timeout of 30000ms exceeded.
  21 |
  22 |         const homePage = new HomePage(page);
  23 |         await homePage.clickMyAccount();
  24 |         await homePage.clickLogin();
  25 |
  26 |         const loginPage = new LoginPage(page);
  27 |         await loginPage.login(data.email, data.password);
  28 |
  29 |         if(data.expected.toLowerCase()==='success')
  30 |         {
  31 |             const myAccountPage=new MyAccountPage(page);
  32 |             const isLoggedIn=await myAccountPage.isMyAccountPageExists();
  33 |             expect(isLoggedIn).toBeTruthy();
  34 |
  35 |         }
  36 |         else{
  37 |             const errorMessage=await loginPage.getloginErrorMessage();
  38 |             expect(errorMessage).toBe('Warning: No match for E-Mail Address and/or Password.');
  39 |         }
  40 |     })
  41 |
  42 | }
  43 |
  44 |
  45 |
  46 | //Load CSV test data logindata.json
  47 |
  48 | const csvPath = "testdata/logindata.csv";
  49 | const csvTestData = DataProvider.getTestDataFromCsv(csvPath);
  50 |
  51 |
  52 | for(const data of csvTestData)
  53 | {
  54 |    test(`Login Test with CSV Data: ${data.testName} @datadriven`, async({page})=>{
  55 |
  56 |         const config = new TestConfig(); // create instance
  57 |         await page.goto(config.appUrl);    // getting appURL from test.config.ts file
  58 |
  59 |         const homePage = new HomePage(page);
  60 |         await homePage.clickMyAccount();
  61 |         await homePage.clickLogin();
  62 |
  63 |         const loginPage = new LoginPage(page);
  64 |         await loginPage.login(data.email, data.password);
  65 |
  66 |         if(data.expected.toLowerCase()==='success')
  67 |         {
  68 |             const myAccountPage=new MyAccountPage(page);
  69 |             const isLoggedIn=await myAccountPage.isMyAccountPageExists();
  70 |             expect(isLoggedIn).toBeTruthy();
  71 |
  72 |         }
  73 |         else{
  74 |             const errorMessage=await loginPage.getloginErrorMessage();
  75 |             expect(errorMessage).toBe('Warning: No match for E-Mail Address and/or Password.');
  76 |         }
  77 |     })
  78 |
  79 | }
```