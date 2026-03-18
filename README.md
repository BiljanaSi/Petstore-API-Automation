# Petstore-API-Automation

# 🐾 Petstore API: End-to-End Automation Suite

This project demonstrates a complete **automated testing lifecycle** for the Petstore API. It covers everything from resource creation and data integrity to business logic validation and final cleanup (teardown).

## 🚀 Key Testing Scenarios
* **Full CRUD Lifecycle:** POST (Create), GET (Read), PUT (Update), and DELETE (Remove).
* **Data Persistence:** Verified that data remains consistent across multiple API calls.
* **Request Chaining:** Dynamically extracted the `Pet ID` from the creation response and passed it through the entire test suite using Postman Environment Variables.
* **Business Logic Testing:** Verified that filtering by status (`sold`) correctly includes the updated pet in the search results.
* **Negative Testing:** Confirmed that deleted resources return a `404 Not Found` status code.

## 🛠️ Technical Implementation
* **Tool:** Postman
* **Scripting:** JavaScript (Postman Sandbox)
* **Variable Management:** Environment-based (baseUrl, petId).
* **Advanced Logic:** Used `.some()` and `.forEach()` JavaScript methods to validate arrays of data.

## 📊 Test Execution (The Matrix)
| Request | Method | Validation Goal |
| :--- | :---: | :--- |
| **Add New Pet** | `POST` | Create resource & capture dynamic ID |
| **Get Pet Details** | `GET` | Verify data integrity & schema |
| **Update Status** | `PUT` | Test business logic (Status change) |
| **Filter Search** | `GET` | Validate search/query parameters |
| **Delete Pet** | `DELETE` | Securely remove the resource |
| **Final Cleanup** | `GET` | Negative test: Confirm 404 (Success) |

## ✅ How to Run
1. Download the `Petstore_Collection.json` and `Petstore_Environment.json`.
2. Import them into Postman.
3. Select the **Petstore - Production** environment.
4. Open **Collection Runner** and click **Run Petstore Lifecycle**.

##  [Test Results] <img width="1770" height="1197" alt="Test Results" src="https://github.com/user-attachments/assets/3474fb50-e1f1-484f-9b6a-e438c7406310" />
