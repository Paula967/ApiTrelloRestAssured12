# Trello API Automation Project (RestAssured)

This project is an automated test suite for managing Trello boards, lists, cards, checklists, and check items using the **Trello API**. It leverages **RestAssured**, **TestNG**, and an XML configuration file to ensure flexible and ordered execution of test cases.

## 🚀 Features

- **Board Operations**:  
  - Create a new board.
  - Retrieve details of a board.
  - Update a board.
  - Delete a board.

- **List Operations**:  
  - Create a new list.
  - Retrieve details of a list.
  - Update a list.
  - Delete a list.

- **Card Operations**:  
  - Create a new card.
  - Retrieve details of a card.
  - Update a card.
  - Delete a card.

- **Checklist Operations**:  
  - Create a checklist on a card.
  - Retrieve details of a checklist.
  - Update a checklist.
  - Delete a checklist.

- **Check Item Operations**:  
  - Create a check item within a checklist.
  - Retrieve details of a check item.
  - Update a check item.
  - Delete a check item.

## 🛠️ Tools and Frameworks

- **RestAssured**: For API request and response handling.
- **TestNG**: For organizing and executing test cases.
- **XML Configuration**: For running tests in a specific order.
- **Maven**: For dependency management and build automation.
- **Allure Reports**: For detailed test reporting.

## 📂 Project Structure

src/main/java ├── api # Contains API request classes for boards, lists, cards, etc. ├── utils # Contains utility classes for authentication, configuration, etc. src/test/java ├── tests # Contains test classes for different entities (boards, lists, etc.) ├── resources # Contains TestNG XML configuration files. pom.xml # Maven configuration file

markdown
Copy code

## 🧑‍💻 Prerequisites

1. **Java Development Kit (JDK)** installed.
2. **Maven** installed for managing dependencies.
3. Trello API Key and Token:
   - [Generate your Trello API Key and Token](https://trello.com/app-key).

## ⚙️ Configuration

1. Add your Trello API Key and Token in a `config.properties` file:
   ```properties
   apiKey=your_api_key
   token=your_api_token
Update the BaseURI in the API request classes if needed.
🧪 Test Execution
1. Run Tests Using TestNG XML
To run tests in a specific order, the project uses an XML configuration file. An example configuration:

xml
Copy code
<suite name="Trello API Test Suite">
    <test name="Test Board and List Functionality">
        <classes>
            <class name="tests.BoardTests">
                <methods>
                    <include name="testCreateBoard" />
                    <include name="testGetBoard" />
                    <include name="testUpdateBoard" />
                    <include name="testDeleteBoard" />
                </methods>
            </class>
            <class name="tests.ListTests">
                <methods>
                    <include name="testCreateList" />
                    <include name="testGetList" />
                    <include name="testUpdateList" />
                    <include name="testDeleteList" />
                </methods>
            </class>
        </classes>
    </test>
</suite>
2. Run with Maven
Execute the tests using the Maven Surefire plugin:

bash
Copy code
mvn clean test
3. Generate Reports
Generate an Allure report after test execution:

bash
Copy code
allure serve target/allure-results
📋 Test Cases
Board Operations
Test Name	Description
testCreateBoard	Creates a new board.
testGetBoard	Retrieves board details.
testUpdateBoard	Updates an existing board.
testDeleteBoard	Deletes the board.
List Operations
Test Name	Description
testCreateList	Creates a new list.
testGetList	Retrieves list details.
testUpdateList	Updates an existing list.
testDeleteList	Deletes the list.
Card, Checklist, and Check Item
Follow the same structure for cards, checklists, and check items.

🏗️ Future Enhancements
Add data-driven testing for dynamic API inputs.
Integrate with CI/CD pipelines for automated runs.
Expand test coverage to include error scenarios.
📞 Contact
For questions or contributions, reach out at:
📧 paula.farid9@gmail.com
🌐 LinkedIn Profile :www.linkedin.com/in/paula-farid-534089225
