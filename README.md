# Clinical LIMS Database

## Recruiter Summary

A relational Oracle SQL database designed to model laboratory sample tracking, workflow management, audit logging, and structured data access within a simulated clinical genomics environment.

This project demonstrates relational schema design, sample traceability, metadata management, automated key generation, audit tracking, and query abstraction for laboratory data workflows.

## What This Project Demonstrates

* Designing relational database schemas from business requirements
* Modeling laboratory entities including projects, samples, instruments, employees, and supplies
* Enforcing primary key and foreign key relationships for data integrity
* Using Oracle sequences for automated key generation
* Implementing triggers for audit tracking and record management
* Creating views to simplify access to structured laboratory data
* Applying indexes to support frequent query patterns

## System Context

The database represents the data infrastructure layer of a laboratory information management system. It supports structured tracking of samples, projects, instruments, employees, and supplies across laboratory workflows.

The design focuses on traceability, auditability, and data integrity in workflows where sample status, metadata, and operational records must remain consistent across processing steps.

## Data Model Overview

Core entities include:

* **Projects** — sequencing or laboratory requests
* **Samples** — biological materials linked to projects
* **Instruments** — laboratory processing and sequencing equipment
* **Employees** — operational users and processing roles
* **Supplies** — laboratory inventory and materials

Key relationships include:

* A project can contain multiple samples
* A sample belongs to one project
* Instruments can be associated with laboratory processing activity
* Employees are linked to operational and workflow records
* Supplies support inventory and workflow tracking

## Core System Features

### Relational Schema Design

The database uses normalized relational tables with primary and foreign key constraints to maintain consistency across laboratory entities.

### Automated Key Management

Oracle sequences are used to generate consistent surrogate keys across core tables.

### Audit Tracking

Triggers support automatic tracking of record creation, modification timestamps, and user attribution.

### Query Abstraction

Views provide simplified access to structured data for common workflow entities, including projects, samples, instruments, employees, and supplies.

### Indexing

Indexes support frequently accessed query paths, including sample tracking, foreign key joins, and workflow-related lookups.

## Example Workflow

A typical usage flow:

1. A project is created for a laboratory or sequencing request.
2. Samples are registered under the project.
3. Samples are associated with laboratory processing records.
4. Instruments and employees are linked to workflow activity.
5. Data is queried through structured views for downstream QC, reporting, and review.

## Technology Stack

**Oracle SQL** • **Relational Database Design** • **Sequences** • **Triggers** • **Views** • **Indexes**

## Design Goals

This project emphasizes:

* Traceable sample and workflow state management
* Structured relational data modeling
* Auditability for operational records
* Data integrity across laboratory entities
* Compatibility with downstream QC and reporting workflows

## Future Enhancements

* REST API layer for programmatic database access
* Integration with Python-based QC workflow tools
* Expanded role-based access control
* Additional schema normalization review
* Example ERD and sample query output

## Author

**Shiloh Cadere**
Bioinformatics Analyst specializing in genomics QC, data validation, workflow traceability, and laboratory data systems.
