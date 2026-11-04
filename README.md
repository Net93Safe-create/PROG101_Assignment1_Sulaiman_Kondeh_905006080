## PROG101_Assignment1_Sulaiman_Kondeh_905006080
This is assignment 1 for Programming Logic and Design about a School Attendance System in S/L 
Project: School Attendance System (SAS)
Student: Sulaiman Kondeh      Student ID: 905006080
Course: PROG101 — Principles of Programming Logic and Design
Institution: Limkokwing University of Creative Technology, Sierra Leone
Examiner: Elijah Fullah

## PROBLEM DESCRIPTION
Many schools need a dependable way to record daily student attendance. When attendance is written only in paper
registers, records may be difficult to search, totals can take time to calculate, and registers may be misplaced or
damaged. Teachers may also find it difficult to identify repeated lateness or absence quickly, especially when several
classes are involved.
The proposed School Attendance Management System is a simple logical solution for recording and reviewing
attendance. It allows an authorised teacher or attendance officer to select a class and date, view the registered
students, and mark each student as Present, Absent, or Late. The system checks that required information is entered,
prevents an attendance record from being saved twice for the same student and date, and stores the result for later
reporting.
The project is a logical design rather than a fully deployed school information system. It does not automatically know
whether a student is physically in class. The teacher remains responsible for checking attendance and entering accurate
information.

## COMMUNITY IMPACT
The proposed system could benefit students, teachers, school administrators, and parents or guardians. Teachers
would have a consistent process for recording attendance, while administrators could review class summaries and
identify attendance patterns that may need attention. Students could benefit when schools identify absence or lateness
early and follow up through appropriate school procedures.
A searchable attendance record could reduce the time spent adding figures from paper registers and preparing routine
summaries. It may also improve accountability because each attendance entry is associated with a student, class, and
date.
The system cannot solve every cause of absenteeism. It cannot replace communication with families, transport support,
health services, or school policies. Its value depends on accurate data entry, responsible access, staff training, and
regular backups. Student information must be kept private and viewed only by authorised people.

## SDG ALIGNMENT
The project mainly supports Sustainable Development Goal 4 (SDG 4): Quality Education. SDG 4 aims to ensure
inclusive and equitable quality education and promote lifelong learning opportunities for all. An organised attendance
record can help a school monitor participation and notice patterns of absence that may require follow-up. This supports
school-level planning, although the system alone cannot guarantee improved attendance or learning outcomes.
The project can also relate to SDG 16: Peace, Justice and Strong Institutions through clearer record-keeping and
accountability in school administration. This connection is indirect: reliable records can support transparent
administrative processes when information is entered and managed responsibly.

## OPEN SOURCE JUSTIFICATION
The proposed system could be developed as Open Source Software so that schools, students, and local developers
can inspect how it works, learn from the design, and contribute improvements. Open access to the source code can
reduce dependence on a single developer and allow the system to be adapted to different school needs, subject to the
chosen software licence.
For Sierra Leone, an open-source approach could support local learning and collaboration. Computing students could
practise improving validation, reports, usability, and data backup. Schools would still need to consider device
availability, staff training, maintenance, privacy, and the cost of operating the system. Open source does not
automatically mean that implementation and support are free.

## ALGORITHM AND PSEUDOCODE
PSEUDOCODE – SCHOOL ATTENDANCE MANAGEMENT SYSTEM
MAIN PROGRAM
BEGIN
DECLARE choice AS INTEGER
REPEAT
DISPLAY "SCHOOL ATTENDANCE MANAGEMENT SYSTEM"
DISPLAY "1. Register Student"
DISPLAY "2. Mark Attendance"
DISPLAY "3. View Attendance Report"
DISPLAY "4. Exit"
INPUT choice
IF choice = 1 THEN
CALL RegisterStudent
ELSE IF choice = 2 THEN
CALL MarkAttendance
ELSE IF choice = 3 THEN
CALL ViewAttendanceReport
ELSE IF choice = 4 THEN
DISPLAY "Thank you for using the system"
ELSE
DISPLAY "Invalid choice. Please select 1 to 4"
END IF
UNTIL choice = 4
END
MODULE RegisterStudent
BEGIN
INPUT studentID
INPUT studentName
INPUT className
IF studentID = EMPTY OR studentName = EMPTY OR className = EMPTY THEN
DISPLAY "Please complete all required fields"
ELSE IF studentID already exists THEN
DISPLAY "Student ID already registered"
ELSE
SAVE studentID, studentName, className
DISPLAY "Student registered successfully"
END IF
END

MODULE MarkAttendance
BEGIN
INPUT staffID
IF staffID is not authorised THEN
DISPLAY "Access denied"
ELSE
INPUT className
INPUT attendanceDate
LOAD students in className
IF no students are found THEN
DISPLAY "No students registered for this class"
ELSE
FOR EACH student IN studentList
DISPLAY studentID, studentName
DISPLAY "Enter P for Present, A for Absent, L for Late"
INPUT status
WHILE status is not P AND status is not A AND status is not L
DISPLAY "Invalid status. Enter P, A, or L"
INPUT status
END WHILE
IF attendance record already exists for studentID and attendanceDate THEN
DISPLAY "Duplicate attendance record - not saved"
ELSE
END IF
SAVE studentID, className, attendanceDate, status, staffID
END FOR
END IF
DISPLAY "Attendance processing completed"
END IF
END
MODULE MarkAttendance
BEGIN
INPUT className
INPUT startDate
INPUT endDate
SEARCH attendance records for className between startDate and endDate
IF no matching records are found THEN
DISPLAY "No attendance records found"
ELSE
COUNT Present records
COUNT Absent records
COUNT Late records
DISPLAY attendance details
DISPLAY Present total, Absent total, Late total
END IF
END

## FLOWCHART
Flowchart 1:Main program and menu navigation
