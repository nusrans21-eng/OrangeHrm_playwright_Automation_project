# OrangeHRM Playwright + TypeScript Test Automation Framework

A web test automation framework built using **Playwright**, **TypeScript**, and the **Page Object Model (POM)** design pattern for the OrangeHRM demo application.

## Features & Architecture

- **Page Object Model (POM):** Separates test logic from page actions and locators.
- **Centralized Test Data:** Test data and expected values are maintained in dedicated test data files.
- **Reusable Page Classes:** Login, Dashboard, Admin User Management, and My Info page classes.
- **Organized Test Suites:** Test scenarios are grouped by module and functional area.
- **HTML Reporting:** Playwright HTML reports for test execution results.
- **Execution Evidence:** Screenshots, videos, and traces configured for test execution.
- **Sequential Execution:** Configured to run with one worker and zero retries.

## Project Structure

```text
playwright_project_02/
├── testData/
│   ├── testData.ts
│   ├── dashboardTestData.ts
│   ├── myInfoTestData.ts
│   ├── sample-avatar.png
│   ├── sample-doc.txt
│   └── invalid-file.xyz
├── pages/
│   ├── loginPage.ts
│   ├── dashboardPage.ts
│   ├── adminUserPage.ts
│   └── myInfoPage.ts
├── tests/
│   ├── login.spec.ts
│   ├── dashboard.spec.ts
│   ├── adminUser.spec.ts
│   └── myInfo.spec.ts
├── playwright.config.ts
├── package.json
├── package-lock.json
├── tsconfig.json
├── .gitignore
└── README.md
```

## Technologies Used

- Playwright
- TypeScript
- Node.js
- npm
- Page Object Model (POM)

## Prerequisites

- Node.js (v18 or higher recommended)
- npm (v9 or higher recommended)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/nusrans21-eng/OrangeHrm_playwright_Automation_project.git
   ```

2. Navigate to the project folder:

   ```bash
   cd OrangeHrm_playwright_Automation_project
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Install the Chromium browser:

   ```bash
   npx playwright install chromium
   ```

   On Windows PowerShell, use `npm.cmd` and `npx.cmd` if script execution is restricted.

## Test Coverage

The framework contains **84 test cases across four modules**.

| Module | Test file | Test cases |
|---|---|---:|
| Login | `login.spec.ts` | 3 |
| Dashboard | `dashboard.spec.ts` | 25 |
| Admin User Management | `adminUser.spec.ts` | 30 |
| My Info | `myInfo.spec.ts` | 26 |
| **Total** | | **84** |

### 1. Login Module

- Valid login
- Invalid login
- Empty username and password validation

### 2. Dashboard Module

- Dashboard page and widgets
- Quick Launch navigation
- Side menu functionality
- Top bar and user menu
- General navigation and responsive layout

### 3. Admin User Management Module

- Add users and validate form fields
- Edit and delete users
- User list, sorting, and pagination
- Search and filter functionality

### 4. My Info Module

- Personal details
- Contact details
- Emergency contacts and dependents
- Immigration records
- Job, salary, and reporting details
- Qualifications
- Attachments and profile photo
- Memberships
- Change password
- General navigation and validation

## Running Tests

### Run all tests

```bash
npx playwright test
```

### Run individual modules

**Login:**

```bash
npm run test:valid
npm run test:invalid
npm run test:empty
```

**Dashboard:**

```bash
npm run test:dashboard
```

**Admin User Management:**

```bash
npm run test:admin
```

Run individual Admin areas:

```bash
npm run test:admin:add
npm run test:admin:editdelete
npm run test:admin:list
npm run test:admin:search
```

**My Info:**

```bash
npm run test:myinfo
```

Run selected My Info areas:

```bash
npm run test:myinfo:personal
npm run test:myinfo:contact
npm run test:myinfo:password
```

On Windows PowerShell, use `npm.cmd` and `npx.cmd` instead of `npm` and `npx` when necessary.

## HTML Reports

After test execution, open the default Playwright report:

```bash
npx playwright show-report
```

Reports for individual modules:

```bash
npm run report:valid
npm run report:invalid
npm run report:empty
npm run report:admin
npm run report:myinfo
```

## Coding Standards

1. **Page Object Model:** Page classes contain locators and reusable page actions.
2. **Centralized Test Data:** Test data and expected values are maintained separately.
3. **Reusable Methods:** Common actions are encapsulated in page classes.
4. **Organized Test Cases:** Test cases are grouped using `test.describe()`.
5. **Assertions:** Playwright's `expect` is used to verify application behavior and results.

## Test Execution Result

The latest completed full test execution resulted in:

**84 passed**

This project demonstrates functional UI automation, validation testing, navigation testing, data-driven scenarios, and reusable automation framework design using Playwright and TypeScript.
