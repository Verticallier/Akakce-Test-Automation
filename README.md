# 🛒 Akakçe Test Automation 

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)
![JUnit 5](https://img.shields.io/badge/JUnit5-25A162?style=for-the-badge&logo=junit5&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJIDEA-000000?style=for-the-badge&logo=intellij-idea&logoColor=white)

> A comprehensive, automated testing framework designed to verify the core functionalities of the [Akakçe](https://www.akakce.com) e-commerce platform. Built with **Java**, **Selenium WebDriver**, and **JUnit 5**.

---

## 📋 Table of Contents
- [About The Project](#-about-the-project)
- [Key Features](#-key-features)
- [Built With](#-built-with)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Configuration](#configuration)
- [Usage & Running Tests](#-usage--running-tests)
- [Test Scenarios](#-test-scenarios)
- [Disclaimer](#-disclaimer)
- [Contact](#-contact)

---

## 📖 About The Project

This project aims to automate End-to-End (E2E) testing scenarios for Akakçe.com. It simulates real user behaviors to ensure the reliability and stability of critical application features such as authentication, product search algorithms, filtering mechanisms, and price comparison logic.

The suite follows the **Page Object Model (POM)** design pattern principles (via `BOT` class) to ensure code maintainability and reusability.

---

## 🌟 Key Features

* **Robust Authentication Testing:** Verifies login security, error handling for invalid credentials, and rate-limiting protection.
* **Advanced Search Validation:** Tests typo tolerance, case insensitivity, partial matches, and special character handling.
* **Dynamic Filtering:** Validates product listing accuracy based on price ranges, brand selections, and technical specifications.
* **Watchlist Management:** Automates "Follow/Unfollow" actions, including multi-follow capabilities and duplicate checking.
* **Price Comparison Engine:** Ensures accurate sorting of prices, currency formatting, and redirection to vendor sites.

---

## 🛠 Built With

* **Language:** [Java JDK 23](https://www.oracle.com/java/technologies/downloads/)
* **Web Browser Automation:** [Selenium WebDriver](https://www.selenium.dev/)
* **Testing Framework:** [JUnit 5 (Jupiter)](https://junit.org/junit5/)
* **IDE:** IntelliJ IDEA

---

## 📂 Project Structure

```text
Akakce-Test-Automation/
├── .idea/                  # IntelliJ IDEA project settings
├── out/                    # Compiled class files
├── src/
│   └── akakcebot/
│       └── BOT.java        # Core bot logic & helper methods (POM)
├── Test/
│   └── akakcebot/
│       ├── LoginTest.java              # Authentication tests
│       ├── SearchTest.java             # Search functionality tests
│       ├── FilterTest.java             # Filtering logic tests
│       ├── FollowUnfollowTest.java     # Watchlist management tests
│       └── PriceCompRedirectTest.java  # Price comparison & redirection tests
├── .gitignore              # Git ignore file
├── Akakce-Test-Automation.iml
└── README.md               # Project documentation
```
**🚀 Getting Started**
Follow these steps to set up the project locally.

Prerequisites
Java Development Kit (JDK): Version 17 or higher recommended.

IDE: IntelliJ IDEA (preferred) or Eclipse.

Git: To clone the repository.

Installation
Clone the repository:

Bash
git clone [https://github.com/Verticallier/Akakce-Test-automation.git](https://github.com/Verticallier/Akakce-Test-automation.git)
Open the project: Open your IDE and select the cloned folder (Akakce-Test-Automation) as the project root.

Resolve Dependencies: Ensure that the Selenium and JUnit libraries are correctly added to your project's classpath/module settings.

Configuration
⚠️ Important: To run tests requiring user authentication (Login, Follow, etc.), you must provide valid credentials.

Open Test/akakcebot/LoginTest.java.

Locate the following constants:

Java
private static final String TEST_MAIL = "";     // TODO: Enter your email
private static final String TEST_PASSWORD = ""; // TODO: Enter your password
Fill in your test account credentials.

Repeat this step for FollowUnfollowTest.java and PriceCompRedirectTest.java if necessary.

Note: Never commit your real passwords to GitHub. The .gitignore file is configured to protect sensitive files, but always double-check your code.



**▶ Usage & Running Tests**
You can run the tests using your IDE's test runner.

Run All Tests: Right-click on the Test/akakcebot package and select "Run 'Tests in 'akakcebot''".

Run Specific Class: Open a test file (e.g., SearchTest.java) and click the Play icon next to the class name.



**🧪 Test Scenarios**

1.✅  Authentication (LoginTest)
- Login with valid credentials.
- Login with incorrect password & empty fields (Error message validation).
- "Remember Me" cookie persistence.
- Rate limiting check (Repeated failed attempts).
- Password input masking check.

2.✅   Search Engine (SearchTest)
- Valid product search.
- Empty & Special character query handling.
- Case insensitivity & Partial match verification.
- Typo Tolerance: Verifies if "ipohne" brings results for "iphone".
- Dropdown suggestions check.

3.✅   Filtering (FilterTest)
- Filter by Price Range + Brand + Features.
- Verify filtered results match the selected criteria.
- "No results found" verification for invalid ranges.

4.✅   Watchlist (FollowUnfollowTest)
- Follow a product & verify in profile.
- Prevent duplicate follows (Warning check).
- Multi-Follow: Follow multiple items in a loop.
- Unfollow single item & "Unfollow All" functionality.
- Follow persistence across sessions (Logout/Login).

5.✅ Price Comparison (PriceCompRedirectTest)

- Verify price list visibility (Guest vs. Logged-in).
- Sorting: Ensure prices are sorted ascending.
- Redirect: Test "Go to Seller" button opens a new tab.
- Currency format validation (TL/$/€).
- Free Shipping label check.

⚠️ Disclaimer
This project is for educational and testing purposes only. It is not affiliated with, endorsed by, or connected to Akakce.com. Automated scraping or botting may violate the terms of service of the target website. Use responsibly.

