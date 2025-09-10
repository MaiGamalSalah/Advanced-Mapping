# API-TASK2

### 1. Advanced Mapping
- Add a new entity `Instructor` (id, name, email).
- Map it:
    - **One-to-Many** with `Course` (an instructor can teach many courses).
- Add endpoints to:
    - Assign an instructor to a course.
    - Get all courses for an instructor.
    - ### 2. Add JPQL Queries
- In the `CourseRepository`:
    - Write a JPQL query to **find courses by title keyword** (case-insensitive, ordered by title).
- In the `StudentRepository`:
    - Write a JPQL query to **find students enrolled in a given course title**.
    - 
### 3. Add Criteria API
- In the `StudentService`:
    - Implement a method using **Criteria API** that finds students whose last name starts with a given letter.
- Expose this through a new REST endpoint:  
  `GET /students/search?lastNameStart=A`
   4. Transaction Management
- Create a method in `EnrollmentService` (or inside `StudentService`) that:
    - Enrolls a student in multiple courses **within a single transaction**.
    - Rollback the transaction if any course does not exist.
