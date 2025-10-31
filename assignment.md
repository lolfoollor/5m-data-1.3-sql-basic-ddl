# Assignment

## Brief

Write the SQL statements for the following questions.

## Instructions

Paste the answer as SQL in the answer code section below each question.

### Question 1

Write the SQL statement to create a unique index on the `email` column of the `students` table in the `lesson` schema.

Answer:

```sql
CREATE UNIQUE INDEX students_email_idx ON lesson.students(email);

```

### Question 2

Write the SQL statement to alter the `teachers` table in the `lesson` schema to add a new column `subject` of type `VARCHAR`.

Answer:

```sql
BEGIN TRANSACTION; -- or BEGIN

ALTER TABLE lesson.teachers 
ADD COLUMN subject VARCHAR;

COMMIT; -- either or
ROLLBACK;
```

### Question 3

Write the SQL statement to update the `email` of the teacher with the name 'John Doe' to 'john.doe@school.com' in the teachers table of the `lesson` schema.

Answer:

```sql
BEGIN TRANSACTION; -- or BEGIN

UPDATE lesson.teachers
SET email = 'john.doe@example.com'
WHERE name = 'John Doe';

COMMIT; -- either or
ROLLBACK;

-- You may use SELECT * FROM lesson.teachers WHERE name = 'John Doe'; to check before updating. 

```

## Submission

- Submit the URL of the GitHub Repository that contains your work to NTU black board.
- Should you reference the work of your classmate(s) or online resources, give them credit by adding either the name of your classmate or URL.
