# 01 - Organisation Profile: TechBook Security Corp

> Status: DRAFT v0.1 | Owner: Head of Security | Review: quarterly
> Assumptions marked (A) are fictional design choices and can be changed.

## 1. Company overview
- **Name:** TechBook Security Corp (trading as "TechBook")
- **Business:** B2B SaaS platform giving small independent retailers (bookstores, stationery and gift shops) cloud inventory, point-of-sale and an online storefront.
- **Size:** 50 employees, plus a small number of contractors (A)
- **HQ:** Melbourne, Australia; hybrid and remote-first (A)
- **Customers:** about 1,200 small retailers (A)
- **Hosting:** Microsoft Azure; identity and email on Microsoft 365 / Entra ID (A)

## 2. Mission and security objectives
Protect the confidentiality, integrity and availability of customer retail data and the platform that runs it.
1. Customer data stays confidential and segregated per tenant.
2. The platform is available during retailer trading hours (target 99.9%).
3. Payment data never touches TechBook systems (card processing is handled by a third-party payment provider).
4. Security is demonstrable to customers (audit-ready evidence).

## 3. Core business processes
| # | Process | Owner | Key systems | Data handled |
|---|---------|-------|-------------|--------------|
| 1 | Product development and release | CTO | Git, CI/CD, Azure | Source code, secrets |
| 2 | Platform operations (hosting, monitoring) | DevOps lead | Azure, monitoring | Customer data, logs |
| 3 | Customer onboarding and support | Head of Customer Success | CRM, helpdesk | Customer contacts, tenant data |
| 4 | Sales and billing | COO | CRM, billing system | Contracts, invoices |
| 5 | Hiring and offboarding | HR Manager | HRIS, Entra ID | Employee PII |
| 6 | Finance and payroll | Finance Manager | Accounting, payroll | Financial records |
| 7 | Security and compliance | Head of Security | SIEM, ticketing | Logs, risk and audit records |

## 4. Organisation and headcount (50)
| Department | Headcount | Roles |
|-----------|-----------|-------|
| Executive | 3 | CEO, CTO, COO |
| Engineering | 20 | 1 Engineering Manager, 7 Backend, 4 Frontend, 3 QA, 3 DevOps/SRE, 2 Data |
| Product and Design | 5 | Head of Product, 2 Product Managers, 2 Designers |
| Security and Compliance | 3 | Head of Security (CISO-lite, reports to CTO), Security Engineer, GRC Analyst |
| IT | 2 | IT Manager, IT Support |
| Customer Success and Support | 8 | Head of CS, 2 Onboarding, 5 Support |
| Sales and Marketing | 6 | Head of Sales, 3 Sales, 2 Marketing |
| Finance | 2 | Finance Manager, Accountant |
| HR | 1 | HR Manager |
| Legal | 0 | Outsourced to external counsel |
| **Total** | **50** | |

## 5. Reporting lines
- CEO: COO, CTO
- CTO: Engineering Manager, Head of Product, Head of Security (with a direct line to the CEO for risk escalation)
- COO: Head of Sales, Head of CS, Finance Manager, HR Manager, IT Manager

## 6. Regulatory and framework drivers (A)
- Australian Privacy Act 1988 and the Notifiable Data Breaches scheme
- ASD Essential Eight (target maturity level 2)
- ISO/IEC 27001 (target certification) and SOC 2 Type II (customer demand)
- Design principles: Microsoft Well-Architected Security pillar, Zero Trust

## 7. Crown jewels (initial)
1. Customer tenant databases (retailer inventory, sales, end-customer data)
2. Production Azure environment and its secrets
3. Source code and CI/CD pipeline
4. Entra ID tenant (identity is the control plane)
5. Employee HR and financial records

## 8. Out of scope for now
Physical security detail, detailed vendor contracts. These will be added in later phases.

## 9. Next documents
02 Asset inventory | 03 Data classification | 04 Information security policy | 05 Risk register | 06 Tool approval process | 07 Access control and IAM design | 08 Network architecture | 09 Incident response plan
