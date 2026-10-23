# PeerBooks Database Design

## Purpose

This document defines the official database design for PeerBooks Version 1.0.

The database platform is Supabase PostgreSQL.

All business records shall be stored within the official database.

## Core Principle

Every business record belongs to a company.

Every transactional table must contain:

company_id

Company data must always remain isolated from other companies.

## Master Tables

### companies

Stores registered companies.

Key Fields:

- id
- company_name
- registration_number
- tax_number
- created_at

### users

Stores application users.

Key Fields:

- id
- company_id
- role_id
- full_name
- email
- created_at

### roles

Stores security roles.

Roles:

- Owner
- Administrator
- Accountant
- Sales User
- Viewer

### customers

Customer master records.

Key Fields:

- id
- company_id
- customer_code
- customer_name
- contact_details

### vendors

Vendor master records.

Key Fields:

- id
- company_id
- vendor_code
- vendor_name
- contact_details

### products

Product master records.

Key Fields:

- id
- company_id
- product_code
- product_name
- cost_price
- sale_price

### chart_of_accounts

Official chart of accounts.

Key Fields:

- id
- company_id
- account_code
- account_name
- account_type

## Transaction Tables

### sales

Sales invoice header.

Key Fields:

- id
- company_id
- customer_id
- invoice_number
- invoice_date
- total_amount

### sales_items

Sales invoice lines.

Key Fields:

- id
- sales_id
- product_id
- quantity
- unit_price

### purchases

Purchase invoice header.

Key Fields:

- id
- company_id
- vendor_id
- invoice_number
- invoice_date
- total_amount

### purchase_items

Purchase invoice lines.

Key Fields:

- id
- purchase_id
- product_id
- quantity
- unit_cost

### expenses

Expense transactions.

Key Fields:

- id
- company_id
- expense_date
- account_id
- amount

### journal_entries

Journal entry header.

Key Fields:

- id
- company_id
- entry_number
- entry_date

### journal_lines

Journal entry details.

Key Fields:

- id
- journal_entry_id
- account_id
- debit
- credit

## Security Model

Every business table shall contain company_id.

All business queries must filter by company_id.

A company must never access records belonging to another company.

Child tables such as sales_items, purchase_items, and journal_lines inherit company ownership through their parent records and therefore do not require a direct company_id field.

## Row Level Security

Supabase Row Level Security (RLS) shall be enabled.

Users shall only access records associated with their company.

RLS policies shall be considered mandatory for all business tables.

## Naming Rules

Tables:

- lowercase
- plural form

Primary Keys:

- id

Foreign Keys:

- table_name_id

Dates:

- *_date

Timestamps:

- created_at
- updated_at

## Indexing Principles

Indexes shall be created on:

- company_id
- customer_code
- vendor_code
- product_code
- account_code
- invoice_number

Indexes shall prioritize business search operations and reporting.
