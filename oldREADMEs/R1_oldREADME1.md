# Frugal Burn Tracker

A lightweight web application for analyzing **burn rate, financial runway, expenses, income, and potential cost savings**.

The Frugal Burn Tracker is designed to answer a simple question:

> **How long can the available cash last at the current rate of spending?**

It also provides a simple way to explore how reducing discretionary spending could extend financial runway.

---

## Overview

The Frugal Burn Tracker provides a simple dashboard for entering financial information and analyzing the resulting burn rate and runway.

The application supports:

* Current cash/bank balance
* Recurring and variable expenses
* Essential vs. discretionary expenses
* Multiple expense frequencies
* Optional income streams
* Monthly burn-rate calculations
* Financial runway calculations
* Projected cash-zero date
* "Frugal Potential" / lean-runway analysis
* Basic what-if analysis by pausing expenses
* Multiple currencies
* Sample/demo data
* Automated tests for calculation and application behavior

The application is intentionally lightweight and uses **Flask, SQLite, HTML, and CSS**, without a JavaScript framework.

---

## Key Features

### Financial Runway

The dashboard calculates the estimated financial runway based on available cash and the current burn rate.

Runway can be expressed in:

* Months
* Days
* Projected cash-zero date

The calculation uses an average month length of **30.4375 days** for month/day conversion.

### Burn Rate Analysis

The application provides several views of monthly spending:

* **Gross Burn** — total monthly expenditure
* **Essential Burn** — spending classified as essential
* **Discretionary Burn** — spending classified as non-essential

This makes it possible to distinguish between unavoidable spending and spending that may potentially be reduced.

### Frugal Potential

The application includes a simple "Frugal Potential" analysis.

This estimates how much additional runway could potentially be obtained if discretionary expenses were eliminated.

This is intended as a **what-if analysis**, rather than a recommendation that all discretionary spending should actually be eliminated.

### Expense Management

Expenses can be:

* Added
* Categorized as essential or discretionary
* Assigned different frequencies
* Paused/resumed for what-if analysis
* Deleted

Supported frequencies include:

* Daily
* Weekly
* Monthly
* Annual

The application normalizes these frequencies for monthly burn-rate calculations.

### Income

Optional income streams can be entered and incorporated into the financial analysis.

### Demo Data

The application includes tools for loading sample data so that the dashboard can be explored without entering financial information manually.

---

## Technology Stack

| Component            | Technology        |
| -------------------- | ----------------- |
| Programming Language | Python            |
| Web Framework        | Flask             |
| Database             | SQLite            |
| Frontend             | HTML5 / CSS3      |
| Styling              | Custom CSS        |
| Testing              | Python test suite |
| Dependencies         | Flask             |

The project deliberately avoids large frameworks and unnecessary dependencies.

---

## Project Structure

```text
PORTFOLIO01_FrugalBurnTracker_FlaskSQLite_WebApp__public/
│
├── app.py
├── calculations.py
├── database.py
├── schema.sql
├── requirements.txt
├── test_app.py
├── README.md
│
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── expenses.html
│   ├── income.html
│   └── settings.html
│
└── static/
    └── style.css
```

### Core Python Files

**`app.py`**

Contains the Flask application, routes, form handling, validation, and application-level logic.

**`calculations.py`**

Contains the financial calculation engine, including burn-rate and runway calculations.

**`database.py`**

Provides the SQLite database layer and database operations.

**`schema.sql`**

Defines the SQLite database schema.

**`test_app.py`**

Contains automated tests for the calculation engine and Flask application.

**`requirements.txt`**

Contains the application's Python dependency requirements.

---

## Running the Application

### 1. Install Python

Python 3 is required.

Check whether Python is installed:

```bash
python --version
```

On some systems, you may need:

```bash
python3 --version
```

### 2. Clone the Repository

```bash
git clone https://github.com/delphicventurescode/PORTFOLIO01_FrugalBurnTracker_FlaskSQLite_WebApp__public.git
```

Then enter the project directory:

```bash
cd PORTFOLIO01_FrugalBurnTracker_FlaskSQLite_WebApp__public
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

Using a virtual environment is recommended for normal development:

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
venv\Scripts\activate
```

Then install the dependencies:

```bash
pip install -r requirements.txt
```

### 4. Start the Application

Run:

```bash
python app.py
```

The Flask development server should provide a local address, typically:

```text
http://127.0.0.1:5000
```

Open that address in a web browser.

---

## Running the Tests

The project includes an automated test suite.

Run:

```bash
python -m unittest test_app.py
```

The tests cover the application's calculation logic and Flask routes.

---

## Database

The application uses **SQLite** as its database.

The database structure includes information relating to:

* Application settings
* Expenses
* Income

SQLite was selected because it provides a simple, portable database without requiring a separate database server.

For a small application or prototype, this keeps the technical architecture deliberately simple.

---

## Design Philosophy

The Frugal Burn Tracker follows a few simple principles:

### Keep It Simple

The application is intended to provide useful financial analysis without requiring a complicated software stack.

### Focus on Runway

The central metric is financial runway: the relationship between available cash and the rate at which that cash is being consumed.

### Separate Essential and Discretionary Spending

Not all spending has the same character. Separating essential from discretionary expenses makes it easier to explore potential cost reductions.

### Make What-If Analysis Easy

The ability to pause expenses allows users to experiment with different spending scenarios without permanently deleting the underlying expense.

---

## Development Approach

This project was developed using **Google Antigravity**, an AI-powered coding agent.

The development process involved:

1. Defining the application's requirements.
2. Providing the requirements to Google Antigravity.
3. Having the agent design and implement the application.
4. Reviewing the generated project and its output.
5. Running and testing the resulting application.
6. Iteratively directing changes to the application.

The project therefore serves not only as a demonstration of a Flask/SQLite application, but also as an example of **AI-assisted software development and human-directed coding-agent workflows**.

The objective was to demonstrate how a relatively complete functional web application can be developed rapidly from a clearly defined set of requirements using an AI coding agent.

---

## Portfolio Context

**Portfolio Project #01**

**Project:** Frugal Burn Tracker
**Architecture:** Flask + SQLite
**Frontend:** HTML/CSS
**Development Tool:** Google Antigravity
**Purpose:** Burn-rate and financial-runway analysis

This project is part of a portfolio exploring practical applications of software, automation, and AI-assisted development.

---

## Important Note

This application is intended as a **software demonstration and financial-analysis tool**.

It is not intended to provide financial, investment, accounting, tax, or other professional financial advice.

Financial calculations should be independently verified before being used for consequential decisions.

---

## License

This repository is primarily a portfolio demonstration.

Unless otherwise specified in the repository, the contents should be considered **for demonstration and evaluation purposes**.
