# PeerBooks Architecture

## Purpose

This document defines the official architecture for PeerBooks Version 1.0.

All future development must align with this architecture unless a documented architectural decision supersedes it.

## System Architecture

PeerBooks will be developed as a cloud-based multi-company SaaS platform.

The system shall consist of:

1. Frontend Application
2. Backend Services
3. Database Layer
4. Authentication Layer
5. Reporting Layer

## Frontend

Version 1.0 shall use a web-based user interface accessible through modern browsers.

The frontend must support:

- Desktop devices
- Tablets
- Mobile browsers

The frontend shall be designed as a business application rather than a marketing website.

Approved Frontend Stack:

- Next.js
- TypeScript
- Tailwind CSS
- ShadCN UI

## Backend

Business logic shall be executed on the server side.

Responsibilities include:

- Authentication
- Authorization
- Data validation
- Financial calculations
- Reporting calculations

No critical accounting logic shall rely solely on browser execution.

Approved Backend Services:

- Supabase Authentication
- Supabase Database
- Supabase Row Level Security

## Hosting

Approved Hosting Platforms:

- Frontend: Vercel
- Backend Services and Database: Supabase

## Database

The official database platform is:

Supabase PostgreSQL

All production business data shall reside within the database.

Browser storage may only be used for:

- User preferences
- Temporary caching
- Non-critical settings

Accounting records must never rely on browser-only storage.

## Multi-Company Architecture

Every business record must belong to a company.

Examples:

- Customers
- Vendors
- Products
- Sales
- Purchases
- Expenses
- Journal Entries

All application queries must respect company boundaries.

A company must never have access to records belonging to another company.

## Authentication

Version 1.0 authentication method:

- Email and Password

Future versions may add:

- Google Login
- Microsoft Login

## User Roles

Version 1.0 shall support:

- Owner
- Administrator
- Accountant
- Sales User
- Viewer

Permissions shall be role-based.

## Reporting

Version 1.0 reports:

- Trial Balance
- Profit and Loss Statement
- Balance Sheet

Reports must use accounting records stored within the official database.

## AI Strategy

Version 1.0 prioritizes accounting accuracy.

AI capabilities are considered secondary.

Initial AI capabilities may include:

- Suggestions
- Insights
- Explanations

AI must not replace accounting controls.

## Guiding Principle

Build a reliable accounting platform first.

Add intelligence only after accounting reliability has been proven.
