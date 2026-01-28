# 🛒 Akakçe Test Automation Suite

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
