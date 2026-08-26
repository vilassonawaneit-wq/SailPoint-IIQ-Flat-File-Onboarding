# SailPoint IdentityIQ – Flat File Application Onboarding

## Practical 02: CSV-Based HR Source

This hands-on practical demonstrates how to onboard a CSV-based HR source into **SailPoint IdentityIQ (IIQ)** using a **Delimited File Application**.

## Scenario

The organization does not have a directly connected HR system. Instead, the HR team provides employee data through a CSV file named `employees.csv`.

The objective is to configure the CSV file as an application in IdentityIQ and aggregate the employee account data into IIQ.

## Sample CSV

```csv
employeeId,firstName,lastName,email,department,manager,hireDate,status
E1001,Rahul,Sharma,rahul.sharma@acme.com,Finance,E1000,2024-01-15,Active
E1002,Priya,Patil,priya.patil@acme.com,HR,E1000,2024-02-01,Active
```

## Implementation Steps

1. Create the `employees.csv` file.
2. Log in to SailPoint IdentityIQ.
3. Navigate to **Applications → Application Definition → Add New Application**.
4. Select **Delimited File** as the Application Type.
5. Configure the application name, for example: `HR Master Source`.
6. Provide the CSV file path accessible to the IIQ server.
7. Configure the Account Schema using:
   - employeeId
   - firstName
   - lastName
   - email
   - department
   - manager
   - hireDate
   - status
8. Configure the delimiter as comma and enable header row.
9. Save the application.
10. Run an **Account Aggregation Task**.
11. Verify the aggregated account data in IdentityIQ.

## Expected Result

The employee records from the CSV file are aggregated into SailPoint IdentityIQ.

For this example:

- E1001 – Rahul Sharma
- E1002 – Priya Patil

The visibility and correlation of the accounts with identities depends on the configured IdentityIQ correlation and identity-processing settings.

## Key Concepts Learned

- Delimited File Application
- CSV-based source onboarding
- Account Schema configuration
- Account Aggregation
- Identity Warehouse
- Account and Identity correlation concepts
- Task Scheduler

## Repository Structure

```text
SailPoint-IIQ-Flat-File-Onboarding/
│
├── README.md
├── employees.csv
└── screenshots/
    └── README.md
```

## Screenshots

Add your IdentityIQ practical screenshots inside the `screenshots` folder.

Suggested names:

- `01-application-definition.png`
- `02-delimited-file-configuration.png`
- `03-account-schema.png`
- `04-aggregation-task.png`
- `05-identity-warehouse.png`

## Disclaimer

This repository is created for educational and hands-on learning purposes.

All employee names, IDs, email addresses, and other information used in this practical are sample/dummy data only.
