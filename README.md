# HCP Commercial Analytics & Prescription Opportunity Analysis

A SQL-based commercial analytics project focused on connecting clinical activity with prescription behavior to identify high-value healthcare providers (HCPs), missed opportunities, and actionable sales-force priorities.

## Business Context

The project analyzes healthcare data collected over an 18-month period to understand how clinical signals translate into prescribing behavior.

The core business problem is:

> Healthcare providers may identify patients with potential treatment needs, but not all providers subsequently prescribe the relevant treatment.

The analysis connects clinical alerts, prescription activity, and healthcare account affiliations to identify:

- HCPs and accounts with high prescription and alert activity
- HCPs receiving strong clinical signals but generating few or no prescriptions
- Accounts with low prescription activity relative to their HCP base
- HCPs and accounts that should be prioritized by the sales team

The overall goal is to connect **clinical activity with prescribing behavior** and translate the findings into a clear, data-driven action plan.

## Dataset Overview

The analysis uses three interconnected datasets linked primarily through `HCP_ID`:

| Dataset | Rows | Purpose |
|---|---:|---|
| **Alerts** | 9,537 | Clinical signals indicating potential treatment needs at the HCP level |
| **Sales** | 5,917 | Prescription activity across HCPs and therapies |
| **Affiliation** | 216 | Mapping of HCPs to hospitals, clinics, and healthcare accounts |

### Alerts
Contains clinical alert information such as:
- Alert ID
- Alert Date
- HCP ID
- Lab Result

### Sales
Contains prescription-level information such as:
- Prescription ID
- Prescription Date
- HCP ID
- Drug Name
- Drug ID
- Prescription Volume

### Affiliation
Maps healthcare providers to their associated accounts using:
- HCP ID
- Account ID
- Account Name

## Key Analysis

- Identified HCPs with the highest clinical activity.
- Analyzed prescription behavior following clinical signals.
- Identified HCPs with strong clinical activity but limited prescription activity.
- Compared product and competitor prescription share.
- Measured prescription growth before and after key clinical signals.
- Segmented HCPs into **New Starters, Growers, and Non-Responders**.
- Identified account-level commercial opportunities.
- Recommended sales-force prioritization based on commercial potential.

## Tech Stack

**SQL | PostgreSQL | CTEs | Window Functions | Joins | Aggregations**
