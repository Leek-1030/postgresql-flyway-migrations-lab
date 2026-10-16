\# Flyway Versioned Database Migrations Lab



\## Objective

Use Flyway to manage database schema changes through versioned SQL migration files.



\## Tools Used

\- PostgreSQL 18

\- Flyway Community Edition

\- PowerShell

\- SQL migration scripts



\## Project Structure

```text

flyway-lab/

├── flyway.toml

├── README.md

└── sql/

&#x20;   ├── V1\_\_core\_tables.sql

&#x20;   ├── V2\_\_audit\_log.sql

&#x20;   └── V3\_\_categories.sql

```



\## Migration Files

\- \*\*V1\_\_core\_tables.sql:\*\* Defines the core students and orders tables.

\- \*\*V2\_\_audit\_log.sql:\*\* Defines the audit log table and auditing trigger.

\- \*\*V3\_\_categories.sql:\*\* Defines the categories table and its parent relationship.



\## Configuration

The `flyway.toml` file contains the database connection settings and the location of the SQL migration scripts. The database password should be supplied securely through an environment variable rather than committed to the repository.



\## Verification

Use Flyway's `info` command to inspect migration status before applying changes.



```powershell

flyway -configFiles="$env:USERPROFILE\\flyway-lab\\flyway.toml" info

```



\*\*Important:\*\* Verify the migration status and protect existing database data before running migrations.



\## Conclusion

This lab demonstrates how versioned SQL scripts can help organize and track database schema changes.



