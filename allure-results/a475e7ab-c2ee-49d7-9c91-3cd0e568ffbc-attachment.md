# Test info

- Name: Login Test with CSV Data: Invalid login @datadriven
- Location: C:\Automation\opencartplaywright\tests\LoginDataDriven.spec.ts:55:8

# Error details

```
Error: page.goto: net::ERR_ABORTED; maybe frame was detached?
Call log:
  - navigating to "https://naveenautomationlabs.com/opencart", waiting until "load"

    at C:\Automation\opencartplaywright\tests\LoginDataDriven.spec.ts:58:20
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
  20 |         await page.goto(config.appUrl);    // getting appURL from test.config.ts file
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
  38 |             //expect(errorMessage).toBe('Warning: No match for E-Mail Address and/or Password.');
  39 |             expect(errorMessage).toContain('Warning: No match');
  40 |         }
  41 |     })
  42 |
  43 | }
  44 |
  45 |
  46 |
  47 | //Load CSV test data logindata.json
  48 |
  49 | const csvPath = "testdata/logindata.csv";
  50 | const csvTestData = DataProvider.getTestDataFromCsv(csvPath);
  51 |
  52 |
  53 | for(const data of csvTestData)
  54 | {
  55 |    test(`Login Test with CSV Data: ${data.testName} @datadriven`, async({page})=>{
  56 |
  57 |         const config = new TestConfig(); // create instance
> 58 |         await page.goto(config.appUrl);    // getting appURL from test.config.ts file
     |                    ^ Error: page.goto: net::ERR_ABORTED; maybe frame was detached?
  59 |
  60 |         const homePage = new HomePage(page);
  61 |         await homePage.clickMyAccount();
  62 |         await homePage.clickLogin();
  63 |
  64 |         const loginPage = new LoginPage(page);
  65 |         await loginPage.login(data.email, data.password);
  66 |
  67 |         if(data.expected.toLowerCase()==='success')
  68 |         {
  69 |             const myAccountPage=new MyAccountPage(page);
  70 |             const isLoggedIn=await myAccountPage.isMyAccountPageExists();
  71 |             expect(isLoggedIn).toBeTruthy();
  72 |
  73 |         }
  74 |         else{
  75 |             const errorMessage=await loginPage.getloginErrorMessage();
  76 |             expect(errorMessage).toBe('Warning: No match for E-Mail Address and/or Password.');
  77 |         }
  78 |     })
  79 |
  80 | }
```