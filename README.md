# Student Attendance Management System (SAMS)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Storage](https://img.shields.io/badge/Storage-LocalStorage-2563EB?style=flat-square)
![Version](https://img.shields.io/badge/Version-1.0-2563EB?style=flat-square)

<p align="center">
  <img src="media/bwu-logo.jpg" width="110" alt="Brainware University logo">
</p>

<p align="center"><strong>Brainware University — BCA Academic Web Development Project</strong><br>Developed by Soumik Roy</p>

![Brainware University campus](media/campus-hero.png)

> **Academic demonstration only:** This is an independent student project inspired by the Brainware University Information System (BUIS). It is not an official university portal and is not connected to university servers. All student records, staff profiles and login credentials are fictional. Never enter actual university credentials or confidential information.

## Table of Contents

- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Key Features](#key-features)
- [User Roles and Permissions](#user-roles-and-permissions)
- [Demo Login Credentials](#demo-login-credentials)
- [Batch and Student Configuration](#batch-and-student-configuration)
- [Academic Curriculum](#academic-curriculum)
- [Attendance Workflow](#attendance-workflow)
- [Reports and Calculations](#reports-and-calculations)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Demonstration Walkthrough](#demonstration-walkthrough)
- [Data Storage and Architecture](#data-storage-and-architecture)
- [GitHub Pages Deployment](#github-pages-deployment)
- [Testing and Limitations](#testing-and-limitations)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [Developer](#developer)
- [Acknowledgements and Usage Notice](#acknowledgements-and-usage-notice)

## Project Overview

The **Student Attendance Management System (SAMS)** is a browser-based academic management application designed to demonstrate how a university can organise student records, manage attendance, assign faculty members and generate academic reports through a centralised interface.

The application recreates the traditional blue-and-white institutional design of the Brainware University Information System, using supplied campus photographs, a university logo, a portal selection screen, a collapsible sidebar and compact academic forms.

Unlike a static UI mock-up, SAMS provides interactive attendance marking, record management and persistent browser storage. It is built entirely with **HTML5, CSS3 and Vanilla JavaScript**, without a backend, database server, framework, build process or package installation.

| Project Information | Details |
| --- | --- |
| Project name | Student Attendance Management System (SAMS) |
| Institution | Brainware University |
| School | School of Computational & Applied Sciences |
| Department | Department of Computational Sciences |
| Programme | Bachelor of Computer Applications (Honours) |
| Developer | Soumik Roy |
| Project type | Academic web development project |
| Application language | English |
| Version | 1.0 |

## Objectives

- Demonstrate the digitisation of classroom attendance records.
- Provide administrator, faculty and student interfaces using one shared local data store.
- Organise students according to admission year, section, semester and group.
- Reduce manual attendance calculations and demonstrate duplicate prevention.
- Generate subject-wise, student-wise and batch-wise attendance summaries.
- Apply frontend development concepts such as DOM manipulation, event handling, form validation, responsive design and browser storage.
- Keep the project simple to install, understand, modify and present in an academic environment.

## Key Features

### Authentication and navigation

- Three demonstration login categories: Administrator, Staff and Student.
- Demo account quick-fill buttons, refreshable CAPTCHA, password visibility and Remember Me.
- Role-specific navigation and logout functionality.
- Portal selection with **Academics**, **Students** and **Exam** modules. No Mentor module.
- University-inspired header, dashboard cards, breadcrumbs and sidebar.

### Attendance management

- Batch, semester, course, module, class type, group, class number and date selection.
- Dependent course and class-type controls based on academic configuration.
- Batch-wise and group-wise student rosters with fictional names and unique IDs.
- Individual present/absent checkboxes, bulk marking and student search.
- Live attendance counts and percentages, remarks and confirmation before saving.
- Attendance editing and deletion, duplicate/overlap checks and activity logging.

### Academic administration

- Student, staff, batch and course management.
- Faculty assignment management with scope-based demonstration access.
- Search, filters, pagination and sorting in management tables.
- Lecture plan entry, modification and completion reporting.
- Simple text-based academic resources and feedback modules.
- Configurable demonstration attendance threshold and administrator data reset.

### Reporting

- Student-wise, course-wise, batch-wise, group-wise, semester-wise and monthly summaries.
- Date-wise attendance history and low-attendance lists.
- Personal student attendance and subject-level summaries.
- CSV export and printable reports, including browser Save as PDF.

## User Roles and Permissions

The roles share the same data in one browser. Permissions are simulated in JavaScript for educational purposes; they are not secure server-side authorisation.

| Operation | Administrator | Staff / Professor | Student |
| --- | --- | --- | --- |
| View attendance | All records | Assigned scope | Own records |
| Mark attendance | Yes | Assigned classes | No |
| Modify/delete attendance | Yes | Permitted assigned records | No |
| View student directory | All | Assigned students | Own profile |
| Manage student, staff and course data | Yes | No | No |
| Manage faculty assignments | Yes | View own assignments | No |
| Manage lecture plans | Yes | Assigned classes | No |
| Download attendance reports | All | Assigned scope | Own records |
| View activity logs / reset local data | Yes | No | No |

## Demo Login Credentials

Use the following fictional accounts. Select the matching **User Category**, enter the credentials and type the CAPTCHA displayed on screen.

| Role | User ID | Password |
| --- | --- | --- |
| ADMINISTRATOR | `admin_demo` | `Admin@123` |
| STAFF | `john_doe` | `Staff@123` |
| STUDENT | `BCA2025B001` | `Student@123` |

The staff demonstration account belongs to **John Doe**, assigned to BCA 2025 SEC B, Semester III, Artificial Intelligence (`BCA30203`).

The example student account belongs to **Madhurima Mondal**, BCA 2025 SEC B, Group 1, Semester III. Other active students can sign in using their seeded student ID and the shared demonstration student password. These public demo passwords are intentionally not production credentials.

## Batch and Student Configuration

The application contains a preconfigured roster of **560 fictional students**, distributed across 28 initial BCA batch sections. Each section has 20 students, divided equally into two groups.

| Admission year | Initial sections | Students per section | Total students | Default semester |
| --- | --- | ---: | ---: | --- |
| BCA 2023 | A–G | 20 | 140 | VII |
| BCA 2024 | A–G | 20 | 140 | V |
| BCA 2025 | A–G | 20 | 140 | III |
| BCA 2026 | A–G | 20 | 140 | I |
| **Total** | **28 sections** | | **560** | |

The initial dataset also includes **56 groups**, **28 fictional faculty members**, **8 semesters** and **54 curriculum course entries**. These are demonstration counts, not actual university enrolment figures.

Each student record includes a student ID, Bengali name, demonstration roll and registration numbers, batch, group, semester, curriculum track, language, demo email and account status.

### Example student record

| Field | Value |
| --- | --- |
| Student ID | BCA2025B001 |
| Name | Madhurima Mondal |
| Roll number | DEMO-BCA2025B001 |
| Registration number | DEMO-REG-BCA2025B001 |
| Batch | BCA 2025 SEC B |
| Group | Group 1 |
| Semester | III |
| Email | bca2025b001@example.com |

Student names are seeded in `script.js` so the initial roster remains consistent across fresh installations. Administrators can manage local student records without changing the source file.

## Academic Curriculum

The course database follows the supplied **Brainware University BCA 2024 curriculum**, used as a shared demonstration curriculum across the four admission years. Semester VIII supports both Honours and Honours with Research tracks. Courses include their codes, lecture/tutorial/practical hours, credits and course types.

### Example: Semester III

| Course code | Course name | L–T–P | Credits |
| --- | --- | --- | ---: |
| BCA30104 | Data Structure and Algorithm | 3–1–0 | 4 |
| BCA39105 | Data Structure and Algorithm Lab | 0–0–4 | 2 |
| BCA39106 | Python Lab | 0–0–4 | 2 |
| BCA30203 | Artificial Intelligence | 3–1–0 | 4 |
| BCA30001 | Vedic Mathematics | 3–0–0 | 3 |
| AEC00006 | Modern Indian Language | 2–0–0 | 2 |
| BCA37002 | Internet and Web Technologies | 2–0–2 | 3 |

Modern Indian Language includes Hindi, Bengali, Alternative English and MOOC alternatives in the student configuration. Module and class-number limits are demonstration settings, not verified lecture schedules.

## Attendance Workflow

1. Sign in as Administrator or Staff.
2. Open **Academics → Entry → Attendance Entry**.
3. Select the batch and semester, then the course and module.
4. Select the class type (Theory, Practical, Tutorial or Project, where applicable), group, class number and date.
5. Click **Show** to load eligible students.
6. Tick students who are present or use the bulk marking controls.
7. Review the live summary and add remarks if required.
8. Save and confirm the attendance submission.
9. Use **Attendance Modify** for previously recorded sessions or open the reports to review results.

Saved attendance is available to other permitted demonstration roles when they sign in using the same browser and site origin.

## Reports and Calculations

Attendance percentages are calculated from eligible attendance records, not from fixed sample statistics.

```text
Absent Students = Total Students - Present Students
Class Attendance (%) = (Present Students / Total Students) × 100
Overall Attendance (%) = (Total Attended / Total Eligible Classes) × 100
```

For example, if 17 out of 20 students are present, the class attendance is **85.00%**. Overall attendance uses the total number of attended and eligible class records rather than averaging subject percentages. When no records exist, the interface displays `Not Available`.

The default demonstration eligibility threshold is **75%**. Below that threshold, attendance of at least 65% is shown as a warning, and lower attendance is flagged as low. The administrator can change the eligibility threshold. These are not verified official university examination regulations.

Reports can be filtered by academic criteria and dates, exported as CSV or printed through the browser. Choose **Save as PDF** in the print dialog to save a PDF copy.

## Technology Stack

| Technology | Purpose |
| --- | --- |
| HTML5 | Application entry point and page structure |
| CSS3 | Institutional styling, layout and responsive design |
| Vanilla JavaScript | Interface rendering, events, validation, calculations and record management |
| LocalStorage | Persistent academic data within the browser |
| SessionStorage | Temporary demo login state when Remember Me is disabled |
| SVG | Portal icons |
| Blob and browser print APIs | CSV/text downloads and printable reports |

No React, Node.js, Express, PHP, MySQL, SQLite, npm or external application server is required.

## Project Structure

```text
Student-Attendance-Management-System/
├── index.html
├── styles.css
├── script.js
├── README.md
└── media/
    ├── bwu-logo.jpg
    ├── login-campus.jpg
    ├── campus-main.jpg
    ├── campus-wide.webp
    ├── campus-hero.png
    └── campus-engineering.webp
```

- `index.html` — Entry point for the single-page application.
- `styles.css` — Login, portal, dashboard, forms, tables, responsive and print styling.
- `script.js` — Seed data, local data operations, role checks, hash-based navigation and all interactive functionality.
- `media/` — Supplied university logo and campus photographs.
- `README.md` — Project documentation.

## Getting Started

### Requirements

A modern browser such as Google Chrome, Microsoft Edge or Firefox. Visual Studio Code is optional.

### Method 1: Run directly

1. Download the repository using **Code → Download ZIP**.
2. Extract the downloaded folder.
3. Keep `index.html`, `styles.css`, `script.js` and `media/` together.
4. Open `index.html` in your browser.
5. Sign in using a demo account.

Direct `file://` access depends on the browser's storage policy. If data does not persist or the application fails to load, use Method 2.

### Method 2: Run using VS Code Live Server

1. Open the project folder in Visual Studio Code.
2. Install the optional **Live Server** extension.
3. Right-click `index.html` and select **Open with Live Server**.
4. Use the local address opened by the extension.

Alternatively, if Python 3 is already installed, run `python -m http.server 8000` from the project folder and open `http://localhost:8000`.

Always use the same address and browser profile to retain saved demo records.

## Demonstration Walkthrough

For an academic presentation, follow this sequence:

1. Sign in as Administrator to show the initial student, batch and course configuration.
2. Sign out and sign in as John Doe (`john_doe`).
3. Open Attendance Entry and select BCA 2025 SEC B, Semester III, Artificial Intelligence, Theory and All Groups.
4. Select an unused class number and valid date, then click Show.
5. Mark 17 students present, including `BCA2025B001`, and save the record.
6. Show the attendance summary (17 present, 3 absent, 85.00%).
7. Sign out and sign in as `BCA2025B001` to verify the student's personal attendance.
8. Sign back in as the administrator and review the saved session and reports.

The initial attendance history is empty. Create attendance entries before demonstrating populated reports.

## Data Storage and Architecture

```text
HTML entry point + CSS presentation
                |
        JavaScript interface
                |
   Local data operations and role checks
                |
      Browser LocalStorage
```

The application is a single-page website with hash-based navigation. Views such as the portal, dashboard and attendance page are generated dynamically in JavaScript. The internal `api()` function simulates data operations locally; it does not send network requests to a backend.

The seeded data includes students, staff, batches, groups, courses and faculty assignments. Additional local records store attendance sessions, lecture plans, text resources, feedback, activity history and settings.

The main LocalStorage key is `bwu-sams-offline-v1`. Once changes are saved, they persist across refreshes in the same browser and origin. The demo login state is stored separately in SessionStorage or LocalStorage, depending on Remember Me.

### Resetting demonstration data

Sign in as Administrator, open Settings and select **Reset demo data**. Confirm the prompt to restore the initial dataset. This deletes local changes, saved attendance, lecture plans and other locally stored academic records. Export important demo reports first.

## GitHub Pages Deployment

This project can be hosted as a static website without a backend.

1. Create a new GitHub repository.
2. Upload the project files and complete `media/` folder to the repository root.
3. Open the repository's **Settings → Pages**.
4. Select **Deploy from a branch** as the source, choose the default branch (usually `main`) and `/ (root)` as the folder.
5. Save the configuration and open the published URL shown by GitHub when deployment is ready.

The `index.html` file must be at the root of the chosen publishing directory. A published demo remains browser-local: visitors do not share a database with one another. Publish supplied branding and media only if you have permission to do so.

## Testing and Limitations

The original JavaScript checks covered initial roster generation, student counts, attendance saving, editing, deletion, duplicate prevention and simulated role-scoped reports. Browser-level interaction and exact visual matching were not independently verified in the original test environment. Manual browser testing is recommended before presentation.

Suggested manual checks:

- Verify all three login roles and invalid login handling.
- Confirm that each initial section contains 20 students.
- Confirm that group selection and dependent course options load appropriate records.
- Save attendance and reload the page to verify persistence.
- Verify that duplicate class submissions do not create duplicate records.
- Check the student view, CSV export and print layout.
- Test mobile navigation and the layout on different screen sizes.

### Important limitations

- No real backend, central database, secure authentication or server-side role enforcement.
- Demo credentials and data are visible in JavaScript and browser developer tools. Client-side checks can be bypassed.
- Records are local to one browser profile and origin; different devices and users do not automatically synchronise.
- Clearing browser data, changing the site address or resetting demo data may remove access to saved records.
- The academic resource module is text-based, rather than a full document upload service.
- Attendance eligibility rules, faculty assignments, class schedules and student identities are fictional demonstration data.
- The application must not be used for actual university records, real credentials or official attendance decisions.

## Future Enhancements

Potential improvements beyond the current frontend-only scope include a secure backend with database authentication, multi-device synchronisation, server-enforced permissions, attendance notifications, timetable integration, richer analytics, automated backups and accessible production-grade deployment. These features are proposed, not implemented in this version.

## Contributing

Suggestions and improvements are welcome. Fork the repository, create a feature branch, make changes and submit a pull request describing the improvement. Keep the existing academic interface, avoid introducing real student data, and test the affected features before proposing changes.

## Developer

**Soumik Roy**  
Bachelor of Computer Applications (Honours)  
Department of Computational Sciences  
Brainware University, West Bengal, India

- Role: Project Developer
- Focus: Frontend development, JavaScript logic, academic data organisation and UI design

## Acknowledgements and Usage Notice

The academic interface is inspired by Brainware University's information system, and the course configuration is based on the supplied BCA 2024 curriculum. The university name, logo and campus photographs belong to their respective rights holders. Their inclusion does not imply endorsement or affiliation with the official university information system.

This repository is intended for academic learning and demonstration. No open-source licence has been selected in this README; reuse and redistribution remain subject to applicable rights and permissions, particularly for third-party media.

---

<p align="center"><strong>Student Attendance Management System (SAMS) — Version 1.0</strong><br>Designed &amp; Developed by Soumik Roy<br>Academic Web Development Project</p>
