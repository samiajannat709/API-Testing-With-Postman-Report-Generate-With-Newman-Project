# 🧪 API Testing Project — Restful Booker
An end-to-end API testing project using **Postma** and **Newman** on the **Restful Booker**

## 🔗 Base URL
https://restful-booker.herokuapp.com

## 🛠️ Tools & Technologies

| Postman | Newman | JavaScript |
|----------|--------|-------------|

## 📁 Project Structure

```text
Report_generate_with_newman/
|
├── images/
|   ├── collection.png        # Postman collection Screenshot
|   └── report.png            # Newman repost Screenshot
|
├── API_Testing.postman_collection.json     # Postman collection
├── API_Testing.postman_environment.json    # Environment variables
├── newman/
|   └── API_Testing_Report.html             # Newman HTML Report
└── README.md
```
## 📋 Collection Overview

| Mehod | Request Name | Description |
|-------|--------------|-------------|
| GET | GetBookingIds | Retrieve all bookings |
| POST | CreateBooking | Create a new booking |
| GET | GetBookingID | Retrieven booking details |
| POST | CreateToken | Generate authentication token |
| GET | GetBooking | Verify booking Generate authentication token |
| PUT | UpdateBooking | Update booking details |
| GET | GetBooking | Verify Update booking details |
| PATCH | PartialUpdateBooking | Partially update booking |
| DELETE | DeleteBooking | Delete booking |
| GET | GetBooking | Verify booking deletion|

## 🌍 Environment Variables

| Variable | Description |
|----------|-------------|
| basic_url | Base URL of the API |
| id | Dynamic booking ID |
| token | Dynamic authentication token |
| fname | First name |
| lname | Last name |
| tp | Total price |
| dp | Deposit paid |
| adneed | Additionaln needs |
| ci | Check-in date |
| co | Check-out date |

## 📸 Screenshots

### Postman Collection

![Postman Collection](images/collection.png)

### Newman Report

![Newman Report](images/report.png)

## 📊 Newman Test Report Summary

| Metric | Value |
|--------|-------|
| Total Iterations | 1 |
| Total Requests | 8 |
| Total Assertions | 60 |
| Failed Tests | 0 *(Update if different)* |
| Skipped Tests | 0 |
| Total Run Duration | *(Update from your report)* |
| Average Response Time | *(Update from your report)* |

## 🧠 Challenges Faced

- Managing dynamic variables across multiple requests.
- Validating response data using JavaScript assertions.
- Automating the execution of the complete API collection with Newman.
- Generating detailed HTML reports for test analysis.

## ▶️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/<repository-name>.git
cd <repository-name>
```

### 2. Install Newman

```bash
npm install -g newman
npm install -g newman-reporter-htmlextra
```

### 3. Run the Collection

```bash
newman run API_Testing.postman_collection.json ^
-e API_Testing.postman_environment.json ^
-r htmlextra ^
--reporter-htmlextra-export newman_report.html
```
> **Note:** If you're using macOS or Linux, replace `^` with `\`.

### 4. View the Report

Open **newman_report.html** in your browser to view the detailed test execution report.

## 👤 Author

**Jannatul Ferdous Samia**  
SQA Learner

## 📌 Note

This project was created for learning, practice, and portfolio purposes. It demonstrates API testing automation using **Postman** and **Newman**, including CRUD operations, automated assertions, environment variables, and HTML report generation.
