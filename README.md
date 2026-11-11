# sre-github-lab
“Requirements documentation for a BUG TRACE LIVE.” 

# BUG TRACE LIVE 
 
# BugTrace Live
## Real-Time Error Detection & Developer Notification System

# BugTrace Live
## Real-Time Error Detection & Developer Notification System

## Overview

BugTrace Live is a proposed real-time error monitoring and notification system designed for software houses. It collects error reports from deployed applications, records important error details, identifies the affected application and responsible development team, and sends notifications to the relevant developers.

Software houses often manage multiple applications, such as online ordering systems, backend APIs, and student portals. When an error occurs in a deployed application, developers may not become aware of it immediately. They may depend on client complaints or manually checking server logs.

BugTrace Live aims to reduce this delay by providing a centralized platform where errors from multiple applications can be monitored, classified, tracked, and reported. It helps development teams become aware of failures earlier and investigate them more efficiently.

**Project Type:** Documentation and proposed system  
**Document Version:** 1.0  
**Course:** Software Requirement Engineering  
**Instructor:** Dr. Muddassira Arshad Sheraz  
**Submission Date:** October 5

## Scope

### In Scope

- Real-time error detection: Receive error reports from deployed applications as they occur.
- Application and service identification: Identify the application, project, service, environment, and version associated with each error.
- Centralized error logging: Store error messages, timestamps, error types, and technical details in one place.
- Error classification and severity levels: Categorize errors and assign Critical, High, Medium, or Low severity levels.
- Team notifications: Notify the responsible development team about detected errors.
- Incident status tracking: Track errors through New, Acknowledged, Under Investigation, and Resolved statuses.
- Error history and search: Search and filter previous errors by application, date, type, severity, and status.
- Monitoring dashboard and reporting: Display current errors, recent activity, and basic error statistics.

### Out of Scope

- Fixing errors or automatically suggesting code changes.
- Replacing developers, QA engineers, or system administrators.
- Running software tests or detecting bugs before deployment.
- Developing, hosting, or deploying client applications.
- Full infrastructure monitoring, including CPU and memory usage.
- Managing the complete software development lifecycle.
- Sending direct notifications to clients or end users.

## Stakeholders

- **Developers:** Direct users who investigate and fix production errors. They need timely alerts, technical error details, stack traces, and previous error history.
- **Team Leads:** Direct users responsible for development teams. They need to prioritize errors, view open incidents, and track who is handling each issue.
- **System / DevOps Administrators:** Direct users who manage servers, deployments, application registration, teams, and notification configurations. They need application and environment details and system availability.
- **QA Engineers:** Secondary users who verify fixes and investigate errors that escape testing. They need access to error records, history, and search facilities.
- **Project Managers:** Secondary users who manage project delivery and client communication. They need project-level error summaries, reports, and incident status.
- **Software House Management:** Indirect beneficiaries interested in client satisfaction, company reputation, and team performance. They need summary reports across projects.
- **Clients / Customers:** Indirect beneficiaries who own the applications. They benefit from faster error handling and fewer service interruptions.
- **End Users:** Indirect beneficiaries who use client applications and benefit from fewer and shorter interruptions.

## Functional Requirements

- **FR-01:** The system shall receive error reports from monitored applications when errors occur.
- **FR-02:** The system shall associate each error with its application, client project, service or module, environment, and application version.
- **FR-03:** The system shall store error records centrally, including the error timestamp, type, message, and technical details.
- **FR-04:** The system shall classify errors into categories such as database, network, authentication, and application logic, and group repeated occurrences of the same error.
- **FR-05:** The system shall assign severity levels to errors, including Critical, High, Medium, and Low, according to defined rules.
- **FR-06:** The system shall notify the responsible development team through configured notification channels when an error is detected.
- **FR-07:** The system shall allow authorized users to update an error's status to New, Acknowledged, Under Investigation, or Resolved and record who changed it and when.
- **FR-08:** The system shall allow users to search and filter error history by application, date, type, severity, and status.
- **FR-09:** The system shall provide a centralized monitoring dashboard displaying open errors, recent activity, and the condition of monitored applications.
- **FR-10:** The system shall generate basic reports showing error counts per application and severity, along with average acknowledgement and resolution times.

## Nonfunctional Requirements

- **NFR-01 (Performance):** At least 95% of errors shall appear in BugTrace Live within 10 seconds of occurring in the test environment.
- **NFR-02 (Notification Performance):** Critical error notifications shall be sent within 1 minute in at least 90% of test cases, and all tested notifications shall reach the correct responsible team.
- **NFR-03 (Usability of Error Records):** At least 8 out of 10 sample error records shall contain sufficient information for team members to begin investigating without opening server logs. Each record shall include the time, application, environment, error type, severity, and technical details.
- **NFR-04 (Classification Accuracy):** At least 90% of approximately 20 prepared test errors shall receive the expected severity level, and all prepared Critical errors shall be classified as Critical.
- **NFR-05 (Search Performance):** Searching approximately 1,000 test error records by application, date range, type, severity, and status shall return correct results within 3 seconds.
- **NFR-06 (Multi-Application Support):** The system shall monitor at least 3 sample applications simultaneously and display their errors together on the centralized dashboard.

## Acceptance Criteria

- **FR-01:** Given a connected application, when a sample error occurs, BugTrace Live receives and records its error report.
- **FR-02:** Given an error report from a registered application, the system displays the correct application, project, service or module, environment, and version.
- **FR-03:** Given an incoming error report, the system saves its timestamp, type, message, and technical details in the centralized error records.
- **FR-04:** Given multiple errors of the same type, the system classifies them correctly and groups repeated occurrences into a single entry with an occurrence count.
- **FR-05:** Given a set of prepared test errors, the system assigns Critical, High, Medium, or Low severity according to the configured rules. All prepared Critical errors must be classified as Critical.
- **FR-06:** Given an error from a monitored application, the system sends a notification to the development team associated with that application through its configured channel.
- **FR-07:** Given an error with status New, an authorized user can change its status through Acknowledged and Under Investigation to Resolved. The system records the user and time of each status change.
- **FR-08:** Given stored error records, a user can search and filter them by application, date range, type, severity, and status and receive matching results.
- **FR-09:** Given at least three connected sample applications, the dashboard displays their current open errors and recent activity, with the ability to filter errors by application.
- **FR-10:** Given stored error records from multiple applications, the system generates reports showing error counts by application and severity and average acknowledgement and resolution times.

## Assumptions and Open Questions

### Assumptions

- **A-01:** Each monitored application will be properly integrated with BugTrace Live and capable of sending error reports.
- **A-02:** Software house administrators will register applications and assign their responsible development teams.
- **A-03:** Developers and team leads will have access to the configured notification channels.
- **A-04:** Sample applications and simulated errors will be available for testing this university project.

### Open Questions

- **Q-01:** Which notification channels should be supported, such as email or messaging platforms?
- **Q-02:** Who will have permission to modify severity classification rules?
- **Q-03:** Should developers receive notifications for every error or only errors above a selected severity level?
- **Q-04:** How long should BugTrace Live retain historical error records?

## Project Status and Viewing

BugTrace Live is a proposed Software Requirement Engineering project. Its purpose is to monitor, record, classify, and notify responsible development teams about errors in deployed applications.

The project is limited to sample applications and simulated errors for university testing. It does not automatically fix errors, run software tests, or deploy applications.

The project documentation can be viewed by opening README.md in Notepad or by visiting the GitHub repository and selecting the `doc/feature` branch.

## Team Members / Authors

1. Ayesha Saleem - 524
2. Zara Ibrahim - 547
3. Azeen - 535

**Course:** Software Requirement Engineering  
**Instructor:** Dr. Muddassira Arshad Sheraz  
**Department:** Software Engineering  
**Document Version:** 1.0  
**Submission Date:** October 5

## Contributing

All team members should work on separate documentation branches when making changes to the project documentation.

The contribution process includes:

1. Clone the GitHub repository to the local computer.
2. Create or switch to a separate documentation branch.
3. Edit and review the README.md file.
4. Inspect changes using Git diff.ss
5. Stage the required changes using Git add.
6. Commit changes with meaningful commit messages.
7. Push the documentation branch to GitHub.
8. Open a Pull Request for review before merging changes into the main branch.

All changes should be reviewed to maintain accurate, clear, and consistent project requirements.