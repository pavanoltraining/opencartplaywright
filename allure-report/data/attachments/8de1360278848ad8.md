# Test info

- Name: User registration test
- Location: C:\Automation\opencartplaywright\tests\AccountRegistration.spec.ts:20:5

# Error details

```
Error: locator.textContent: Test timeout of 30000ms exceeded.
Call log:
  - waiting for locator('h1:has-text("Your Account Has Been Created!")')

    at RegistrationPage.getConfirmationMsg (C:\Automation\opencartplaywright\pages\RegistrationPage.ts:99:43)
    at C:\Automation\opencartplaywright\tests\AccountRegistration.spec.ts:47:47
```

# Page snapshot

```yaml
- navigation:
  - button "$ Currency ":
    - strong: $
    - text: Currency 
  - list:
    - listitem:
      - link "":
        - /url: http://localhost/opencart/upload/index.php?route=information/contact
      - text: "123456789"
    - listitem:
      - link " My Account":
        - /url: http://localhost/opencart/upload/index.php?route=account/account
    - listitem:
      - link " Wish List (0)":
        - /url: http://localhost/opencart/upload/index.php?route=account/wishlist
    - listitem:
      - link " Shopping Cart":
        - /url: http://localhost/opencart/upload/index.php?route=checkout/cart
    - listitem:
      - link " Checkout":
        - /url: http://localhost/opencart/upload/index.php?route=checkout/checkout
- banner:
  - link "Your Store":
    - /url: http://localhost/opencart/upload/index.php?route=common/home
    - img "Your Store"
  - textbox "Search"
  - button ""
  - button " 0 item(s) - $0.00"
- navigation:
  - list:
    - listitem:
      - link "Desktops":
        - /url: http://localhost/opencart/upload/index.php?route=product/category&path=20
    - listitem:
      - link "Laptops & Notebooks":
        - /url: http://localhost/opencart/upload/index.php?route=product/category&path=18
    - listitem:
      - link "Components":
        - /url: http://localhost/opencart/upload/index.php?route=product/category&path=25
    - listitem:
      - link "Tablets":
        - /url: http://localhost/opencart/upload/index.php?route=product/category&path=57
    - listitem:
      - link "Software":
        - /url: http://localhost/opencart/upload/index.php?route=product/category&path=17
    - listitem:
      - link "Phones & PDAs":
        - /url: http://localhost/opencart/upload/index.php?route=product/category&path=24
    - listitem:
      - link "Cameras":
        - /url: http://localhost/opencart/upload/index.php?route=product/category&path=33
    - listitem:
      - link "MP3 Players":
        - /url: http://localhost/opencart/upload/index.php?route=product/category&path=34
- list:
  - listitem:
    - link "":
      - /url: http://localhost/opencart/upload/index.php?route=common/home
  - listitem:
    - link "Account":
      - /url: http://localhost/opencart/upload/index.php?route=account/account
  - listitem:
    - link "Register":
      - /url: http://localhost/opencart/upload/index.php?route=account/register
- heading "Register Account" [level=1]
- paragraph:
  - text: If you already have an account with us, please login at the
  - link "login page":
    - /url: http://localhost/opencart/upload/index.php?route=account/login
  - text: .
- group "Your Personal Details":
  - text: Your Personal Details * First Name
  - textbox "* First Name"
  - text: First Name must be between 1 and 32 characters! * Last Name
  - textbox "* Last Name": PascaleVandervort
  - text: "* E-Mail"
  - textbox "* E-Mail": Louisa_Stamm@gmail.com
  - text: "* Telephone"
  - textbox "* Telephone": 477.445.1363 x198
- group "Your Password":
  - text: Your Password * Password
  - textbox "* Password": JMahVw4vOyTU6o4
  - text: "* Password Confirm"
  - textbox "* Password Confirm": JMahVw4vOyTU6o4
- group "Newsletter":
  - text: Newsletter Subscribe
  - radio "Yes"
  - text: "Yes"
  - radio "No" [checked]
  - text: "No"
- text: I have read and agree to the
- link "Privacy Policy":
  - /url: http://localhost/opencart/upload/index.php?route=information/information/agree&information_id=3
- checkbox [checked]
- button "Continue"
- complementary:
  - link "Login":
    - /url: http://localhost/opencart/upload/index.php?route=account/login
  - link "Register":
    - /url: http://localhost/opencart/upload/index.php?route=account/register
  - link "Forgotten Password":
    - /url: http://localhost/opencart/upload/index.php?route=account/forgotten
  - link "My Account":
    - /url: http://localhost/opencart/upload/index.php?route=account/account
  - link "Address Book":
    - /url: http://localhost/opencart/upload/index.php?route=account/address
  - link "Wish List":
    - /url: http://localhost/opencart/upload/index.php?route=account/wishlist
  - link "Order History":
    - /url: http://localhost/opencart/upload/index.php?route=account/order
  - link "Downloads":
    - /url: http://localhost/opencart/upload/index.php?route=account/download
  - link "Recurring payments":
    - /url: http://localhost/opencart/upload/index.php?route=account/recurring
  - link "Reward Points":
    - /url: http://localhost/opencart/upload/index.php?route=account/reward
  - link "Returns":
    - /url: http://localhost/opencart/upload/index.php?route=account/return
  - link "Transactions":
    - /url: http://localhost/opencart/upload/index.php?route=account/transaction
  - link "Newsletter":
    - /url: http://localhost/opencart/upload/index.php?route=account/newsletter
- contentinfo:
  - heading "Information" [level=5]
  - list:
    - listitem:
      - link "About Us":
        - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=4
    - listitem:
      - link "Delivery Information":
        - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=6
    - listitem:
      - link "Privacy Policy":
        - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=3
    - listitem:
      - link "Terms & Conditions":
        - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=5
  - heading "Customer Service" [level=5]
  - list:
    - listitem:
      - link "Contact Us":
        - /url: http://localhost/opencart/upload/index.php?route=information/contact
    - listitem:
      - link "Returns":
        - /url: http://localhost/opencart/upload/index.php?route=account/return/add
    - listitem:
      - link "Site Map":
        - /url: http://localhost/opencart/upload/index.php?route=information/sitemap
  - heading "Extras" [level=5]
  - list:
    - listitem:
      - link "Brands":
        - /url: http://localhost/opencart/upload/index.php?route=product/manufacturer
    - listitem:
      - link "Gift Certificates":
        - /url: http://localhost/opencart/upload/index.php?route=account/voucher
    - listitem:
      - link "Affiliate":
        - /url: http://localhost/opencart/upload/index.php?route=affiliate/login
    - listitem:
      - link "Specials":
        - /url: http://localhost/opencart/upload/index.php?route=product/special
  - heading "My Account" [level=5]
  - list:
    - listitem:
      - link "My Account":
        - /url: http://localhost/opencart/upload/index.php?route=account/account
    - listitem:
      - link "Order History":
        - /url: http://localhost/opencart/upload/index.php?route=account/order
    - listitem:
      - link "Wish List":
        - /url: http://localhost/opencart/upload/index.php?route=account/wishlist
    - listitem:
      - link "Newsletter":
        - /url: http://localhost/opencart/upload/index.php?route=account/newsletter
  - separator
  - paragraph:
    - text: Powered By
    - link "OpenCart":
      - /url: http://www.opencart.com
    - text: Your Store © 2025
```

# Test source

```ts
   1 | import { Page, Locator, expect } from '@playwright/test';
   2 |
   3 | export class RegistrationPage {
   4 |     private readonly page: Page;
   5 |     
   6 |     // Locators using CSS selectors
   7 |     private readonly txtFirstname: Locator;
   8 |     private readonly txtLastname: Locator;
   9 |     private readonly txtEmail: Locator;
   10 |     private readonly txtTelephone: Locator;
   11 |     private readonly txtPassword: Locator;
   12 |     private readonly txtConfirmPassword: Locator;
   13 |     private readonly chkdPolicy: Locator;
   14 |     private readonly btnContinue: Locator;
   15 |     private readonly msgConfirmation: Locator;
   16 |
   17 |     constructor(page: Page) {
   18 |         this.page = page;
   19 |         
   20 |         // Initialize locators with CSS selectors
   21 |         this.txtFirstname = page.locator('#input-firstname');
   22 |         this.txtLastname = page.locator('#input-lastname');
   23 |         this.txtEmail = page.locator('#input-email');
   24 |         this.txtTelephone = page.locator('#input-telephone');
   25 |         this.txtPassword = page.locator('#input-password');
   26 |         this.txtConfirmPassword = page.locator('#input-confirm');
   27 |         this.chkdPolicy = page.locator('input[name="agree"]');
   28 |         this.btnContinue = page.locator('input[value="Continue"]');
   29 |         this.msgConfirmation = page.locator('h1:has-text("Your Account Has Been Created!")');
   30 |     }
   31 |
   32 |     /**
   33 |      * Sets the first name in the registration form
   34 |      * @param fname - First name to enter
   35 |      */
   36 |     async setFirstName(fname: string): Promise<void> {
   37 |         await this.txtFirstname.fill(fname);
   38 |     }
   39 |
   40 |     /**
   41 |      * Sets the last name in the registration form
   42 |      * @param lname - Last name to enter
   43 |      */
   44 |     async setLastName(lname: string): Promise<void> {
   45 |         await this.txtLastname.fill(lname);
   46 |     }
   47 |
   48 |     /**
   49 |      * Sets the email in the registration form
   50 |      * @param email - Email to enter
   51 |      */
   52 |     async setEmail(email: string): Promise<void> {
   53 |         await this.txtEmail.fill(email);
   54 |     }
   55 |
   56 |     /**
   57 |      * Sets the telephone number in the registration form
   58 |      * @param tel - Telephone number to enter
   59 |      */
   60 |     async setTelephone(tel: string): Promise<void> {
   61 |         await this.txtTelephone.fill(tel);
   62 |     }
   63 |
   64 |     /**
   65 |      * Sets the password in the registration form
   66 |      * @param pwd - Password to enter
   67 |      */
   68 |     async setPassword(pwd: string): Promise<void> {
   69 |         await this.txtPassword.fill(pwd);
   70 |     }
   71 |
   72 |     /**
   73 |      * Sets the confirm password in the registration form
   74 |      * @param pwd - Password to confirm
   75 |      */
   76 |     async setConfirmPassword(pwd: string): Promise<void> {
   77 |         await this.txtConfirmPassword.fill(pwd);
   78 |     }
   79 |
   80 |     /**
   81 |      * Checks the privacy policy checkbox
   82 |      */
   83 |     async setPrivacyPolicy(): Promise<void> {
   84 |         await this.chkdPolicy.check();
   85 |     }
   86 |
   87 |     /**
   88 |      * Clicks the Continue button
   89 |      */
   90 |     async clickContinue(): Promise<void> {
   91 |         await this.btnContinue.click();
   92 |     }
   93 |
   94 |     /**
   95 |      * Gets the confirmation message text
   96 |      * @returns Promise<string> - Confirmation message text
   97 |      */
   98 |     async getConfirmationMsg(): Promise<string> {
>  99 |         return await this.msgConfirmation.textContent() ?? '';
      |                                           ^ Error: locator.textContent: Test timeout of 30000ms exceeded.
  100 |     }
  101 |
  102 |     /**
  103 |      * Complete registration workflow
  104 |      * @param userData - Object containing registration data
  105 |      */
  106 |     async completeRegistration(userData: {
  107 |         firstName: string;
  108 |         lastName: string;
  109 |         email: string;
  110 |         telephone: string;
  111 |         password: string;
  112 |     }): Promise<void> {
  113 |         await this.setFirstName(userData.firstName);
  114 |         await this.setLastName(userData.lastName);
  115 |         await this.setEmail(userData.email);
  116 |         await this.setTelephone(userData.telephone);
  117 |         await this.setPassword(userData.password);
  118 |         await this.setConfirmPassword(userData.password);
  119 |         await this.setPrivacyPolicy();
  120 |         await this.clickContinue();
  121 |         await expect(this.msgConfirmation).toBeVisible();
  122 |     }
  123 | }
  124 |
```