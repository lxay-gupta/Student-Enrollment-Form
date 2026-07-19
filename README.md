# Student Enrollment Form

A web-based Student Enrollment Form built using **HTML, CSS, JavaScript, jQuery**, and **JsonPowerDB (JPDB)** as the backend database. This project demonstrates save, update, retrieve reset operations using JPDB's RESTful API.

---

## Description

The **Student Enrollment Form** is a front-end web application that allows users to manage student records in a database. It provides a clean, user-friendly interface to:

- **Save** new student records
- **Retrieve** existing student records by Roll-No
- **Update** existing student details
- **Reset** the form to its initial state

The application uses **JsonPowerDB** as its backend database, storing data in the `STUDENT-TABLE` relation of the `SCHOOL_DB` database. The **Roll-No** field serves as the primary key, ensuring each student record is unique.

### Input Fields

| Field Name         | Description                  |
|--------------------|------------------------------|
| Roll-No            | Unique identifier (Primary Key) |
| Full-Name          | Student's full name          |
| Class              | Class/Grade of the student   |
| Birth-Date         | Date of birth                |
| Address            | Residential address          |
| Enrollment-Date    | Date of enrollment           |

---

## Benefits of using JsonPowerDB

1. **Serverless & Real-Time** – No server setup required; database is instantly available.
2. **JSON-Native Database** – Data is stored as JSON, making it perfect for web applications.
3. **Fastest NoSQL Database** – Offers lightning-fast query response times.
4. **Built-in RESTful API** – No need to write backend code; direct API calls from the browser.
5. **Schema-Free with Flexibility** – Easy to add or modify fields without migrations.
6. **Fast Key-Based Retrieval** – Quick data lookup using GET_BY_KEY command with indexed fields.
7. **Supports Multiple Commands** – PUT, GET, GET_BY_KEY, UPDATE, DELETE, and more.
8. **Cross-Platform** – Works seamlessly with HTML, JavaScript, and other web technologies.
9. **Low Latency** – Real-time data updates with minimal delay.
10. **Cost-Effective** – Free tier available for learning and small-scale projects.

---

## Release History

| Version | Date       | Description                                              |
|---------|------------|----------------------------------------------------------|
| v1.0.0  | 2026-07-19 | Initial release of the Student Enrollment Form with Save, Update, and Reset functionality using JsonPowerDB |
| v1.1.0  | 2026-07-19 | Added comprehensive README.md documentation with project details, usage instructions, and examples |

---

## Scope of Functionalities

### Core Features
- ✅ **Form Validation** – Ensures no field is left empty before saving.
- ✅ **Primary Key Check** – Detects whether a Roll-No already exists.
- ✅ **Dynamic UI** – Enables/disables fields and buttons based on context.
- ✅ **Save New Records** – Inserts a new student into the database.
- ✅ **Retrieve Records** – Fetches and displays existing student data.
- ✅ **Update Records** – Modifies existing student information.
- ✅ **Reset Form** – Clears all fields and returns to initial state.

### User Workflow
1. On page load → Empty form with only Roll-No enabled.
2. User enters Roll-No and presses Enter.
3. If Roll-No is **new** → Enables Save & Reset; moves cursor to Full-Name.
4. If Roll-No **exists** → Populates form; enables Update & Reset; disables Roll-No.
5. User completes/edits the form and clicks Save or Update.
6. On success → Form resets automatically.

---

##  Examples of Use

### Example 1: Adding a New Student
1. Enter Roll-No: `101` → Press Enter
2. Form shows: *"New Roll-No. Please fill in the remaining details."*
3. Fill in:
   - Full-Name: `John Doe`
   - Class: `10th`
   - Birth-Date: `2008-05-15`
   - Address: `123 Main Street`
   - Enrollment-Date: `2024-06-01`
4. Click **Save** → Record stored successfully.

### Example 2: Updating an Existing Student
1. Enter Roll-No: `101` → Press Enter
2. Form auto-populates with John Doe's details
3. Change Class to `11th`
4. Click **Update** → Record updated successfully.

### Example 3: Resetting the Form
1. Click **Reset** at any time
2. Form clears and returns to initial state
3. Cursor moves back to Roll-No field

---

## Instructions to Run

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge)
- A JsonPowerDB account and token
- A local web server (e.g., VS Code Live Server)

### Steps
1. **Clone the repository:**
   ```bash
   git clone https://github.com/lxay-gupta/Student-Enrollment-Form.git
   cd student-enrollment-form

2. Configure your JPDB credentials:

   Create a file named config.js:
   const JPDB_CONFIG = {
    baseUrl: "http://api.login2explore.com:5577",
    token: "YOUR_JPDB_TOKEN_HERE",
    dbName: "SCHOOL_DB",
    relName: "STUDENT-TABLE"
     };

3. Run the application:
   Open index.html using VS Code Live Server, OR
   Open index.html directly in your browser

4. Start using the form:
   Enter a Roll-No and press Enter
   Fill in the details and click Save




