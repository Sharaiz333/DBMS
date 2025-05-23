CREATE TABLE STUDENTS (
    StudentID INT PRIMARY KEY,
    FirstName VARCHAR2(50),
    LastName VARCHAR2(50),
    DateOfBirth DATE,
    Email VARCHAR2(100)
);

CREATE TABLE COURSES (
    CourseID INT PRIMARY KEY,
    CourseName VARCHAR2(100),
    Instructor VARCHAR2(100)
);

CREATE TABLE ENROLLMENTS (
    EnrollmentID INT PRIMARY KEY,
    StudentID INT,
    CourseID INT,
    EnrollmentDate DATE,
    FOREIGN KEY (StudentID) REFERENCES STUDENTS(StudentID),
    FOREIGN KEY (CourseID) REFERENCES COURSES(CourseID)
);

CREATE TABLE GRADES (
    GradeID INT PRIMARY KEY,
    StudentID INT,
    CourseID INT,
    Grade CHAR(2),
    Semester VARCHAR2(20),
    FOREIGN KEY (StudentID) REFERENCES STUDENTS(StudentID),
    FOREIGN KEY (CourseID) REFERENCES COURSES(CourseID)
);


SQL Commands for Table Enhancement:
Add New Columns:
ALTER TABLE STUDENTS
ADD (
    PhoneNumber VARCHAR2(15),
    Address VARCHAR2(255),
    Department VARCHAR2(100),
    Semester VARCHAR2(20)
);

ALTER TABLE COURSES
ADD (
    CreditHours NUMBER(2),
    CourseType VARCHAR2(50),
    Department VARCHAR2(100)
);

ALTER TABLE ENROLLMENTS
ADD (
    EnrollmentStatus VARCHAR2(20)
);

ALTER TABLE GRADES
ADD (
    GPA NUMBER(3,2),
    Remarks VARCHAR2(255)
);
