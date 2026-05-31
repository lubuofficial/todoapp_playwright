# TodoMVC Automation Testing (Playwright)

This repository contains an automated testing script for the [React TodoMVC](https://demo.playwright.dev/todomvc/) website using Playwright. 

## ⚙️ How to Set Up and Run

**Prerequisites:**
* Node.js installed on your machine.

**Installation Steps:**
1. Clone this repository to your local machine.
2. Open a terminal and navigate into the project directory.
3. Install the required dependencies by running:
   npm install
4. Install the required Playwright browsers by running:
   npx playwright install

**Execution:**
To run the automated tests in the terminal, execute:
npx playwright test


---

## 🧪 Test Cases Designed (ออกแบบ Test Cases)

The automation script (`tests/todo-app.spec.js`) is designed as a continuous End-to-End (E2E) user flow. It verifies the following core functionalities:

* **Create Todos:** Verify that a user can type text into the input field and press 'Enter' to add multiple items to the list (e.g., "Buy Groceries", "Rest", "Go to gym", "Cooking").
* **Complete Todos:** Verify that users can mark specific items as completed by clicking the toggle checkbox.
* **Filter Active Todos:** Verify that clicking the "Active" link successfully hides completed items and only displays remaining tasks (verifying "Rest" and "Go to gym" are visible).
* **Clear Completed Todos:** Verify that navigating to the "Completed" tab and clicking the "Clear completed" button removes all finished tasks from the application entirely.
* **View All Todos:** Verify that the user can return to the "All" tab to see the updated, accurate list of remaining tasks.

---

## 🏗️ Project Structure (โครงสร้างที่เหมาะสมและยั่งยืน)

This project utilizes Playwright's standard structure, which provides a scalable and sustainable foundation for UI automation:

* **`tests/todo-app.spec.js`**: Contains the automated test script. Centralizing the user flow here allows for easy execution and straightforward debugging. As the project grows, more `.spec.js` files can be added to this folder without cluttering the root directory.
* **`playwright.config.js`**: The central configuration file. This allows global settings (like browsers, timeouts, and test execution rules) to be managed in one place rather than hardcoded into individual tests, ensuring long-term maintainability.
* **`package.json` & `package-lock.json`**: Manages all project dependencies. This ensures that anyone evaluating or working on the project can clone the repository and reproduce the exact same environment effortlessly.
