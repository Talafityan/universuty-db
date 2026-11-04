# Database Schema Fixes

The original university database schema contained 12 design mistakes.

1. Changed `FullName` to `full_name` for consistent naming.
2. Added a primary key to `students.id`.
3. Added a unique constraint to `students.email`.
4. Changed `date_of_birth` from varchar to date.
5. Changed `credit_hours` from varchar to integer.
6. Removed the redundant `instructor_name` column from courses.
7. Removed the incorrect `student_id` column from courses.
8. Changed `enrollments.student_id` from varchar to integer.
9. Corrected the department-course relationship.
10. Corrected the enrollment-course foreign key to reference `courses.id`.
11. Added a unique constraint on `(student_id, course_id)` in enrollments.
12. Added the missing relationship between instructors and departments.

All identified schema issues have been corrected.