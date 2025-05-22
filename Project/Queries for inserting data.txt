Insert Sample Data:

INSERT INTO STUDENTS (StudentID, FirstName, LastName, DateOfBirth, Email, PhoneNumber, Address, Department, Semester)
VALUES
(57288, 'Sharaiz', 'Romee', TO_DATE('1993-09-05', 'YYYY-MM-DD'), 'sharaiz.romee@gmail.com', '03001234567', 'Lahore, Pakistan', 'Computer Science', '4th'),
(1, 'Ali', 'Khan', TO_DATE('2001-12-05', 'YYYY-MM-DD'), 'ali.khan@example.com', '03111234567', 'Islamabad, Pakistan', 'Computer Science', '4th'),
(2, 'Sara', 'Ahmed', TO_DATE('2002-09-23', 'YYYY-MM-DD'), 'sara.ahmed@example.com', '03211234567', 'Karachi, Pakistan', 'Computer Science', '4th');

INSERT INTO COURSES (CourseID, CourseName, Instructor, CreditHours, CourseType, Department)
VALUES
(101, 'Database Systems', 'Mr. Ihtisham-Ullah', 3, 'Core', 'Computer Science'),
(102, 'Computer Architecture', 'Dr. Raza', 3, 'Core', 'Computer Science');

INSERT INTO ENROLLMENTS (EnrollmentID, StudentID, CourseID, EnrollmentDate, EnrollmentStatus)
VALUES
(1, 57288, 101, TO_DATE('2024-09-01', 'YYYY-MM-DD'), 'Active'),
(2, 57288, 102, TO_DATE('2024-09-01', 'YYYY-MM-DD'), 'Active'),
(3, 1, 101, TO_DATE('2024-09-01', 'YYYY-MM-DD'), 'Active'),
(4, 1, 102, TO_DATE('2024-09-01', 'YYYY-MM-DD'), 'Active'),
(5, 2, 101, TO_DATE('2024-09-01', 'YYYY-MM-DD'), 'Active'),
(6, 2, 102, TO_DATE('2024-09-01', 'YYYY-MM-DD'), 'Active');

INSERT INTO GRADES (GradeID, StudentID, CourseID, Grade, Semester, GPA, Remarks)
VALUES
(1, 57288, 101, 'A', 'Fall 2024', 4.0, 'Excellent'),
(2, 57288, 102, 'A-', 'Fall 2024', 3.7, 'Very Good'),
(3, 1, 101, 'B+', 'Fall 2024', 3.3, 'Good performance'),
(4, 1, 102, 'A-', 'Fall 2024', 3.7, 'Very Good'),
(5, 2, 101, 'A', 'Fall 2024', 4.0, 'Excellent'),
(6, 2, 102, 'B+', 'Fall 2024', 3.3, 'Good performance');
