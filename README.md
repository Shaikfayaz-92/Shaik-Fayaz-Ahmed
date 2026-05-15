 Technical Analysis: Optimizing SQL Query Logic

*Objective:* To identify and resolve common logical errors in relational database queries.

*Problem Statement:* A query failed to execute because it attempted to reference a column alias within the same SELECT statement where it was defined.

*Technical Resolution:* In standard SQL (specifically Oracle and MySQL), column aliases cannot be referenced in the WHERE or SELECT clauses of the same level. To resolve this, I refactored the logic using a Common Table Expression (CTE) to ensure the alias was materialized before being called. This approach improves code readability and prevents execution errors.
