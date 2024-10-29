# Database Design

This project provides a MongoDB database design for the Database Design Program. The structure includes collections for users, topics, tasks, attendance, CodeKata scores, company drives, and mentors, allowing for efficient management and querying of student information, program details, and analytics.

## Table of Contents
- [Project Overview](#project-overview)
- [Collections](#collections)
  - [Users](#users)
  - [Attendance](#attendance)
  - [CodeKata](#codekata)
  - [Company Drives](#company-drives)
  - [Mentors](#mentors)
  - [Tasks](#tasks)
  - [Topics](#topics)
- [Queries](#queries)

---

## Project Overview

The Database is designed to store and manage data related to student progress, attendance, tasks, topics covered, CodeKata practice, mentor assignments, and company placement drives. This data structure supports complex queries that provide insights into the progress and participation of students.

## Collections

### Users
This collection stores information about the students in the Database Design.
- `user_id`: Unique identifier for the user
- `name`: Full name of the user
- `age`: Age of the user
- `course`: Program/course enrolled by the user

### Attendance
This collection keeps track of attendance records for each user.
- `user_id`: ID of the user
- `topic_id`: ID of the topic
- `attended`: Boolean indicating if the user attended
- `percentage`: Attendance percentage

### CodeKata
This collection records each user's progress in CodeKata.
- `user_id`: ID of the user
- `std_id`: Standard ID for the user (MongoDB ObjectID)
- `total_qn`: Total questions available
- `completed`: Questions completed by the user

### Company Drives
This collection contains data about placement drives hosted by various companies.
- `company_name`: Name of the company
- `date`: Date of the drive
- `no_of_attended`: Number of attendees
- `students_appeared`: List of user IDs who attended

### Mentors
This collection lists mentors and the number of mentees assigned to each.
- `mentor_name`: Name of the mentor
- `mentees_count`: Number of mentees assigned to this mentor

### Tasks
This collection records tasks assigned to users along with submission status.
- `task_id`: Unique task ID
- `user_id`: ID of the user assigned to the task
- `task`: Task description
- `due_date`: Task due date
- `submitted`: Boolean indicating if the task was submitted
- `attendance`: Attendance status

### Topics
This collection stores information about topics covered in the program.
- `topic_id`: Unique topic ID
- `topic`: Topic name
- `month`: Month when the topic was taught

## Queries

The database includes various queries to fetch information, such as:
1. Topics and tasks taught in October
2. Company drives held between October 15 and October 31, 2020
3. Students who attended each company drive
4. Total problems solved by each user in CodeKata
5. Mentors with more than 15 mentees
6. Users who were absent and did not submit tasks between October 15 and October 31, 2020

The complete queries are documented in `MongoDB-Database Design.pdf`.
