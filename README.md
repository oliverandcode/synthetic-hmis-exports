# Synthetic HMIS Export
Version: 1.0.0

## Purpose
This repository contains mock datasets (no potentially sensitive information) 
to test HMIS data analysis. All persons (participants/clients, government 
employees, and non-profit workers), projects, and organizations referenced 
within these datasets are entirely fictional. 

These datasets are intended to mimic actual HUD HMIS exports without exposing 
potentially sensitive information. They are designed for testing and 
demonstration purposes. No information in this repository represents real 
people, organizations, projects, addresses, phone numbers, or HMIS records. 
Counties and CoC codes are real. In some cases, celebrity names have been used 
to explicitly signal that the records here do not represent real people. 

### Example Use Cases
- Unit testing
- Integration testing
- Ingestion testing
- Parser development
- Query development
- Analytics development
- Demonstrations

## Data Characteristics
- No potentially sensitive information
- 100% fictional persons, projects, and organizations
- Real counties, CoC codes, and eligibility requirements
- Minimal mock dataset guidelines:
    - Compliant with 2026 HMIS Data Standards
    - Los Angeles County setting (CoC CA-600)
    - 1 fictional organization
    - 5 fictional projects
    - 5 fictional participants
    - 5 users
        - 2 "special" users: Admin & InternalAPI
        - 3 fictional workers in the supportive housing sector
    - Internally consistent foreign keys / data relationships
    - No intentional errors or edge cases

### V1.0.0: Scaffolding *** <!-- <= current version -->
- **NEW:** Documentation of fictional profiles (persons, projects, and organizations)
- **NEW:** Canonical registry of fictional data
    - Designed to optimize re-generating datasets for new schemas
- Minimal synthetic export batch phase 1: *Foundational Metadata*
    - **NEW:** Export.csv (ExportID needed for ALL other CSVs)

### V1.0.1: Expand Minimal Dataset
- Documentation of fictional profiles
- Canonical registry of fictional data
- Minimal synthetic export batch phase 2: *Administration*
    - Export.csv
    - **NEW:** Organization.csv
    - **NEW:** User.csv
    - Upstream requirement for both:
        - ONLY ExportID from Export.csv

## Project Structure

synthetic-hmis-exports/
├── mock_datasets/
│   └── HUD-2026/
│       └──minimal/
│           ├── Export.csv
│           ├── Organization.csv
│           └── User.csv
├── canonical_registry/
│       └──minimal/
│           ├── canonical_entities.csv
│           ├── organization_profile.md
│           ├── project_profiles.md
│           ├── user_profiles.md
│           └── participant_profiles.md
├── LICENSE
└── README.md
