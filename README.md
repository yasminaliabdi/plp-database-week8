# Audit Logging, Category Trees, and Safe Migrations Lab

## What I Did

- **Step 1:** Built a reusable audit log using a PostgreSQL trigger that records INSERT, UPDATE, and DELETE operations as JSONB.
- **Step 2:** Tested the audit trail by updating and deleting rows, then verified the changes were logged.
- **Step 3:** Modeled a hierarchical category tree using a self-referencing table and a recursive CTE.
- **Step 4:** Applied versioned migrations using Flyway (V1, V2, V3).
- **Step 5:** Implemented least-privilege security with read and write roles.

## Screenshots

| File | Description |
|------|-------------|
| `screenshot1_audit_trail.png` | Audit log showing INSERT, UPDATE, DELETE captured |
| `screenshot2_category_tree.png` | Recursive CTE output showing the category hierarchy |
| `screenshot3_flyway_info.png` | Flyway migration history (3 migrations applied) |
| `screenshot4_roles.png` | Database roles (app_read, app_write, api) |

## Key Concepts

- **Audit Trigger:** Captures every change automatically, regardless of which user or app made it.
- **Recursive CTE:** Walks parent-child relationships in a self-referencing table.
- **Flyway:** Manages schema changes as versioned migration files.
- **Least Privilege:** Grants only the permissions each role actually needs.
