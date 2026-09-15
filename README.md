# 🚀 WebdriverIO Web UI Automation Framework (JavaScript + Mocha + Allure)

A scalable **Web UI Test Automation Framework** built using **WebdriverIO**, **JavaScript**, **Mocha**, and the **Page Object Model (POM)** design pattern.

## 📌 Tech Stack

| Category | Technology |
|---|---|
| Automation Framework | WebdriverIO |
| Programming Language | JavaScript (ES6+) |
| Test Framework | Mocha |
| Browser Automation | Chrome |
| Design Pattern | Page Object Model (POM) |
| Reporting | Allure / HTML reporting |
| Package Manager | npm |

## ✨ Framework Features

- WebdriverIO Test Runner
- Mocha test framework
- Page Object Model architecture
- Chrome browser automation
- Async/Await implementation
- Reusable page objects
- Centralized WebdriverIO configuration
- Extensible reporting
- Support for parallel execution

## 📁 Project Structure

```text
webdriverio-web-ui-automation-main/
│
├── pageobjects/
│   ├── page.js
│   ├── login.page.js
│   └── secure.page.js
│
├── specs/
│   └── example.e2e.js
│
├── wdio.conf.js
├── package.json
├── package-lock.json
├── .gitignore
└── README.md
```

## 🧱 Framework Architecture

```text
                Test Spec
                    │
                    ▼
             Page Object
                    │
                    ▼
              Base Page
                    │
                    ▼
             WebdriverIO
                    │
                    ▼
             Chrome Browser
```

## ⚙️ Installation

### Clone the repository

```bash
git clone <repository-url>
cd webdriverio-web-ui-automation-main
```

### Install dependencies

```bash
npm install
```

Ensure Google Chrome is installed on the execution machine.

## ▶️ Running Tests

Run the complete suite:

```bash
npx wdio run wdio.conf.js
```

Run a specific test:

```bash
npx wdio run wdio.conf.js --spec ./specs/example.e2e.js
```

If an npm test script is configured:

```bash
npm test
```

## 🧪 Sample Test Scenario

The sample framework demonstrates login automation against **The Internet** application.

### Scenario

1. Open the login page.
2. Enter a valid username.
3. Enter a valid password.
4. Click Login.
5. Verify successful login.

Application:

```text
https://the-internet.herokuapp.com/login
```

Sample credentials:

```text
Username: tomsmith
Password: SuperSecretPassword!
```

## 📄 Page Object Model

The framework separates test logic from page-specific locators and actions.

Example:

```javascript
await LoginPage.login(
    "tomsmith",
    "SuperSecretPassword!"
);
```

This approach improves:

- Maintainability
- Reusability
- Readability
- Scalability
- Locator management

## 📊 Reporting

### Allure

If Allure is configured in the project, generate and open the report with:

```bash
allure generate allure-results --clean
allure open
```

Reports can provide:

- Test execution status
- Test duration
- Failure details
- Stack traces
- Browser information
- Execution history

## ⚙️ WebdriverIO Configuration

Typical configuration includes:

```javascript
capabilities: [{
    browserName: "chrome",
    acceptInsecureCerts: true
}]
```

The framework can be extended to support additional browsers and environments.

## 🌐 Browser Support

Current setup:

- ✅ Chrome

Can be extended to:

- Firefox
- Microsoft Edge
- Safari
- Cloud browsers such as BrowserStack or Sauce Labs

## 🔄 CI/CD Integration

The framework can be integrated with:

- GitHub Actions
- Jenkins
- Azure DevOps
- GitLab CI/CD

A typical CI pipeline can perform:

```text
Checkout
   ↓
Install Node.js
   ↓
npm ci
   ↓
Run WebdriverIO Tests
   ↓
Generate Reports
   ↓
Publish Test Results
```

## 🚀 Future Enhancements

- Cross-browser testing
- Data-driven testing
- Environment-specific configuration
- API + UI automation
- Docker execution
- BrowserStack integration
- GitHub Actions CI/CD
- Jenkins pipeline
- Slack/Teams notifications
- Enhanced Allure reporting
- Test tagging and selective execution

## 💡 Automation Best Practices

This project follows commonly used automation practices:

- Page Object Model
- Reusable page methods
- Centralized configuration
- Async/Await
- Separation of test and page logic
- Maintainable locators
- Automated reporting
- CI/CD readiness

## 👨‍💻 Author

**Vinod Kumar**

**Lead SDET | QA Automation Architect | Staff Software Engineer**

### Core Expertise

- Playwright
- Selenium
- WebdriverIO
- Cypress
- BrowserStack
- API Automation
- CI/CD
- JavaScript / TypeScript
- Azure DevOps
- GitHub Actions

---

⭐ If you find this project useful, consider starring the repository and connecting with me on LinkedIn.
