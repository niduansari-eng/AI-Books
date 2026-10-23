# Decision 001

Date: 2026-10-21

Subject: Initial Target Market

Decision:

PeerBooks will initially target:

- Small and Medium Enterprises (SMEs)
- Trading Businesses
- Manufacturing Businesses
- Service Businesses

Excluded from Version 1.0:

- Advanced textile export workflows
- Export documentation management
- Letter of Credit workflows

Reason:

Export-focused functionality significantly increases product complexity and is not required for the first launch.

# Decision 002

Date: 2026-10-21

Subject: Core Problem Being Solved

Decision:

PeerBooks will focus on replacing:

- Spreadsheet-based accounting
- Manual bookkeeping
- Disconnected business records
- Expensive accounting software

Reason:

These are the most common operational challenges faced by SMEs.

# Decision 003

Date: 2026-10-21

Subject: Version 1.0 MVP Scope

Decision:

Version 1.0 must include:

- Login
- Company Setup
- User Management
- Sales
- Purchases
- Expenses
- Inventory
- Trial Balance
- Profit and Loss Statement
- Balance Sheet

Reason:

These represent the minimum requirements for a usable accounting platform.

# Decision 004

Date: 2026-10-21

Subject: Product Strategy

Decision:

PeerBooks will prioritize:

1. Strong Accounting Foundation
2. Business Intelligence
3. AI Assistance

Reason:

Reliable accounting functionality must be established before advanced AI features are introduced.

# Decision 005

Date: 2026-10-22

Subject:
Roadmap and MVP Alignment

Observation:
The roadmap currently places Sales, Purchases, Inventory, and Financial Statements in later phases.

The MVP document requires these modules for Version 1.0.

Decision:
The MVP requirements take precedence.

Sales, Purchases, Inventory, Trial Balance, Profit and Loss Statement, and Balance Sheet are mandatory components of Version 1.0.

Action:
Architecture and future roadmap revisions must align with the MVP document.

Reason:
A customer cannot operate a complete accounting system without these modules.

# Decision 006

Date: 2026-10-24

Subject: Frontend Framework

Decision:

PeerBooks Version 1.0 will use Next.js as the official frontend framework.

Reason:

Next.js supports the approved architecture, works natively with Vercel, supports server-side execution, and aligns with long-term SaaS scalability requirements.

# Decision 007

Date: 2026-10-24

Subject: UI Framework

Decision:

PeerBooks Version 1.0 will use Tailwind CSS and ShadCN UI as the official frontend UI framework.

Reason:

This combination provides rapid development, modern SaaS user experience, and long-term flexibility.

# Decision 008

Date: 2026-10-24

Subject: Hosting Architecture

Decision:

Frontend hosting platform:

- Vercel

Backend and database platform:

- Supabase

Reason:

This architecture aligns with the approved SaaS architecture and simplifies deployment, scalability, and maintenance.

# Decision 009

Date: 2026-10-24

Subject:
Company Ownership Assignment

Decision:

The first user creating a new company automatically receives the Owner role.

This automatic assignment occurs only once per company.

All future users must be invited or assigned roles by authorized users.

Reason:

Every company must begin with a clearly designated owner responsible for administration and governance.
