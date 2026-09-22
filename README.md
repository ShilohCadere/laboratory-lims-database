# Laboratory LIMS Database

## At a Glance

- Requirements-driven Oracle SQL laboratory information management system (LIMS).
- Models sample traceability, workflow tracking, audit logging, and structured laboratory data.
- Demonstrates relational database design, data integrity, and workflow automation.
- Simulates laboratory operations using a normalized database schema and synthetic data.

---

## Overview

Laboratory LIMS Database is a portfolio project that models the core data infrastructure supporting laboratory operations. Beginning with documented business requirements, the project translates laboratory workflows into a normalized Oracle SQL database supporting sample traceability, workflow management, audit logging, and structured data access.

The repository emphasizes relational database design, data integrity, and laboratory informatics while using synthetic data within a simulated regulated laboratory environment.

---

## Why This Project Exists

Laboratory operations depend on accurate tracking of samples, projects, instruments, personnel, and supplies throughout the testing lifecycle. Maintaining those relationships requires more than storing data—it requires enforcing business rules, preserving traceability, and supporting consistent workflow management.

This project demonstrates that process.

Using Oracle SQL, the database models laboratory workflows through normalized relational design, primary and foreign key relationships, automated key generation, audit tracking, and query abstraction.

The focus is not a specific laboratory discipline. Instead, the project demonstrates how relational database architecture supports laboratory operations, traceability, and downstream analytical workflows.

---

## System Architecture

Laboratory LIMS Database models the data layer supporting laboratory operations. Core laboratory entities are represented independently while maintaining relationships through normalized relational design.

```
Projects
     │
     ▼
Samples
     │
     ├──── Instruments
     │
     ├──── Employees
     │
     └──── Supplies
            │
            ▼
Views / Queries
```

An entity relationship diagram is included in `docs/LIMS_ERD.png`.

---

## Repository Structure

```text
laboratory-lims-database/
├── oracle_lims_schema.sql   # Schema, sequences, triggers, views, indexes, and sample data
├── LIMS Requirements.docx   # Documented business and workflow requirements
├── docs/
│   └── LIMS_ERD.png         # Entity relationship diagram
├── LICENSE
└── README.md
```

The implementation is consolidated in a single Oracle SQL script so the complete schema and supporting database objects can be reviewed and executed together. Requirements and data-model documentation are kept separately to preserve the connection between laboratory workflow needs and database design.

---

## Current Capabilities

Current functionality includes:

- Modeling laboratory projects, samples, instruments, employees, and supplies.
- Enforcing relational integrity through primary and foreign keys.
- Generating surrogate keys using Oracle sequences.
- Tracking record history through database triggers.
- Simplifying common queries using database views.
- Improving query performance through indexing.
- Supporting laboratory workflow traceability through normalized relationships.

---

## Example Data Model

Core entities include:

### Projects

Laboratory testing requests and workflow status.

### Samples

Materials tracked throughout laboratory processing.

### Instruments

Equipment supporting laboratory workflows.

### Employees

Personnel responsible for laboratory activities.

### Supplies

Materials supporting sample preparation and analysis.

The included records are synthetic demonstration data intended solely to illustrate database behavior.

---

## Execution

Execute `oracle_lims_schema.sql` within an Oracle database environment to create the schema, supporting database objects, and demonstration dataset.

---

## Example Outputs

Successful execution creates a laboratory information management data model including:

### Database Schema

Normalized relational tables supporting laboratory workflows.

### Automation

Sequences and triggers supporting key generation and audit tracking.

### Query Views

Simplified access to laboratory workflow information.

### Validation Queries

Representative queries demonstrating sample traceability, workflow status, and operational reporting.

---

## Design Decisions

Several architectural decisions intentionally shape this project.

### Requirements-Driven Design

The schema was developed from documented laboratory business requirements before implementation.

### Normalized Relational Design

Entities are separated to minimize redundancy while preserving data integrity.

### Automated Database Behavior

Sequences and triggers automate key generation and audit tracking rather than relying on application logic.

### Query Abstraction

Views simplify common laboratory queries while insulating downstream consumers from schema complexity.

---

## Testing

The database is validated through execution of schema creation scripts, integrity constraints, automated database objects, and representative workflow queries demonstrating correct system behavior.

---

## Future Improvements

Planned future development includes:

- Expanding representative query examples.
- Developing a REST API for programmatic access.
- Extending role-based access controls.
- Continuing schema refinement as laboratory workflows evolve.

Future development will continue to prioritize maintainable database architecture, laboratory traceability, and relational data integrity.

---

## Technologies Used

Oracle SQL • Relational Database Design • Sequences • Triggers • Views • Indexes

---

## Author

**Shiloh Cadere**

Bioinformatics analyst focused on genomics QC, analytical review, workflow development, and reproducible bioinformatics software.
