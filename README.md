# MIST 4610 GROUP 8 Project-2

## Team Name:
CRN:39217 Group 8

## Team Members:
1. Vishal Ramajayam: [@vishalramajayam-art](https://github.com/vishalramajayam-art)
2. Bhavya Siva: [@bhavyasiva](https://github.com/bhavyasiva)
3. Sheshasri Mallibhatti: [@sheshasrimallibhatti-dot](https://github.com/sheshasrimallibhatti-dot)
4. Huzaifah Malik: [@huzaifahmalik](https://github.com/huzaifahmalik)

---

## Problem Description
The objective of this project is to create and set up a relational database for the everyday operations of a tutoring and learning center.  The Student is the central entity in this model. They are enrolled in different academic subjects and given a tutoring plan.  The tutoring center sets up a lot of lessons in classrooms with tutors who are also experts in certain subjects. Additionally, the system keeps track of students, their parents or guardians, tutors, subjects, tutoring plans, scheduled sessions, classroom locations, and academic progress through tests and reports.  It also keeps track of payments and assessments to show both academic and financial activity.  We hope that this database will help the tutoring center make decisions and run more smoothly.

---

## Data Model
Explanation of Data Model:
This database is meant to help run a tutoring center by keeping track of students, their parents, tutors, subjects, tutoring plans, scheduled sessions, payments, and grades. The student entity is the most important part of the model. It is linked to a parent or guardian who is in charge of enrollment and payment. Also, each student is in a specific plan that sets the costs and the number of tutoring sessions they can have. Tutors teach sessions in a classroom and link them to a subject. A bridge entity connects students to the sessions they attend, which keeps track of attendance. The model also keeps track of students' academic progress by connecting them to tests and progress reports that show how they are doing over time. Additionally, payment records capture financial transactions made by guardians on behalf of the student. The model does not keep track of things like tutor pay, detailed curriculum content, real-time scheduling conflicts, messaging/communication logs, or external school data that isn't related to tutoring operations. Overall, this design helps a tutoring center with both academic and administrative tasks. It lets you see how many students are participating, how much work the tutors have, how much demand there is for each subject, and financial performance of the center. 


<img width="962" height="1312" alt="MIST 4610 Project 2" src="https://github.com/user-attachments/assets/14c5fe7d-82a2-4b29-be8b-0069960be94f" />


---

## Data Dictionary 

<img width="559" height="429" alt="image" src="https://github.com/user-attachments/assets/3a4565f0-088b-4040-bded-e0c94885462d" />

<img width="587" height="534" alt="image" src="https://github.com/user-attachments/assets/115515bb-3038-45c3-aa2d-663f7b94dd4e" />

<img width="571" height="547" alt="image" src="https://github.com/user-attachments/assets/a9f0a85a-8250-4fed-9b34-ffdd6a72a0f4" />

<img width="618" height="287" alt="image" src="https://github.com/user-attachments/assets/e89c65e5-bdf4-4f1f-87d7-870d59a518c6" />

<img width="611" height="456" alt="image" src="https://github.com/user-attachments/assets/c8532f59-f436-4b9f-8d33-b7bd3705cb32" />

<img width="574" height="497" alt="image" src="https://github.com/user-attachments/assets/31efe8a7-5280-461d-8c47-334b1f071c7f" />

<img width="566" height="404" alt="image" src="https://github.com/user-attachments/assets/474d9650-ca50-4fef-a8cd-0cf9d4842a2a" />

<img width="574" height="435" alt="image" src="https://github.com/user-attachments/assets/fa8b2701-ae09-4c21-b128-708a967e6907" />

<img width="563" height="523" alt="image" src="https://github.com/user-attachments/assets/43c13b6d-07e8-4631-b43a-5e9357c91dcc" />

<img width="558" height="440" alt="image" src="https://github.com/user-attachments/assets/f34e7595-5fee-4dd3-8d0d-25afbb705965" />

<img width="568" height="354" alt="image" src="https://github.com/user-attachments/assets/928a4540-228f-4b5c-b223-1d879db6789a" />

## Queries


| Feature                | Query 1 | Query 2 | Query 3 | Query 4 | Query 5 | Query 6 | Query 7 | Query 8 | Query 9 | Query 10 |
|------------------------|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:--------:|:--------:|
| multiple table join     |    X    |    X    |    X    |    X    |         |    X    |    X    |    X    |    X     |          |
| subquery               |         |         |         |         |    X    |         |         |         |          |          |
| GROUP BY              |    X    |    X    |    X    |    X    |         |         |         |         |          |          |
| GROUP BY with HAVING   |         |    X    |    X    |    X    |         |         |         |         |          |          |
| multi condition WHERE  |    X    |         |         |         |         |    X    |         |    X    |          |          |
| built-in functions     |    X    |    X    |    X    |    X    |    X    |         |         |         |    X     |          |

1. Write a query to list each student’s first name and last name, their guardian’s first name and last name, and the highest payment amount made by that student. Only include students whose status is 'Active' and who have made at least one payment greater than 200. Group the results by student and guardian, and sort the results from the highest payment to the lowest.
   
<img width="466" height="428" alt="query 1" src="https://github.com/user-attachments/assets/29c409cb-b52f-4dad-a7cc-f5d3c249b4cd" />

Query 1 helps staff identify each active student who has made a high payment of over 200. It shows the student’s and guardian’s names along with the largest payment amount. This allows employees to quickly find top-paying active students and their guardians.

2. Write a query to show each tutor’s first name, last name, specialty, and the total number of sessions they have taught. Only include tutors who have taught at least 3 sessions. Group the results by tutor, and sort so that tutors with the highest number of sessions appear first, and then by tutor name.
   
<img width="491" height="423" alt="query 2" src="https://github.com/user-attachments/assets/1633df42-3bd0-414a-b2b3-81f57e2975e5" />

Query 2 shows which tutors have taught at least 3 sessions, along with their specialty and total sessions taught. This helps management recognize experienced tutors and assign classes more effectively.

3. Write a query to list each plan’s name and session_limit along with the total amount paid by all students on that plan. Only include plans where the total paid is greater than 1000 and where session_limit is at least 4. Group the results by plan, and order by the total paid in descending order.
   
<img width="473" height="430" alt="query 3" src="https://github.com/user-attachments/assets/4011e758-c844-44e7-b328-8fb2d3eae28a" />

Query 3 displays each tutoring plan’s name, session limit, and the total payments made by students under that plan. It highlights plans bringing in more than 1000 in revenue and those offering 4 or more sessions, helping administrators track profitable plans.

4. Write a query to list each classroom’s room_name and capacity, the total number of sessions that took place in that classroom, and the number of distinct tutors who taught in that classroom. Only include classrooms where at least 3 different tutors have taught. Group the results by classroom, and order the results by the number of distinct tutors (highest first), then by room_name.
   
<img width="482" height="428" alt="query 4" src="https://github.com/user-attachments/assets/7d48a379-057b-4ffb-a68b-fe7d2767d4ed" />

Query 4 lists classrooms with their capacity, total sessions, and number of distinct tutors	who have taught there. It filters for classrooms where 3 or more tutors have taught, helping optimize space and scheduling.

5. Write a query to find all students with status 'Active' whose most recent assessment score is below 70. For each of these students, return the student’s first name, last name, the assessment_date of their most recent assessment, and the score from that same assessment. Use a subquery to identify the most recent assessment per student. Order the final output by score from lowest to highest, then by student name.

<img width="608" height="427" alt="query 5" src="https://github.com/user-attachments/assets/063b1dca-3fdb-4384-afee-6f36edb6fa8c" />

Query 5 finds all active students whose latest assessment score is below 70. It shows their most recent score and date, allowing staff to identify students needing academic support.

6. Write a query to list all trainer–trainee tutor pairs where one tutor is being trained by another tutor. For each pair, return the trainer’s first and last name, the trainee’s first and last name, and the trainee’s specialty. Only include pairs where the trainer and trainee have the same specialty. Sort the results by the trainer’s last name and then the trainee’s last name.
   
<img width="465" height="427" alt="query 6" src="https://github.com/user-attachments/assets/3aaebc85-7a8b-4ac3-84e4-af517fb80eee" />

Query 6 lists trainer to trainee tutor pairs where both share the same specialty. This makes it easy to see mentorship relationships and ensure proper training alignment among tutors.

7. Write a query to return every student’s first name, last name, and the plan_name of the plan that student is currently enrolled in.
   
<img width="472" height="428" alt="query 7" src="https://github.com/user-attachments/assets/04d535d9-6052-41cb-8f8c-18d804716b74" />

Query 7 displays every student with their first name, last name, and the name of the plan they’re enrolled in. It provides a quick overview of which plan each student is on.

8. Write a query to return the first name, last name, and phone number of every guardian who has at least one student whose status is 'Inactive'. Each guardian should only appear once in the results.
   
<img width="468" height="428" alt="query 8" src="https://github.com/user-attachments/assets/ed2cbb94-994c-45de-9517-657e10a3f837" />

Query 8 shows the names and phone numbers of guardians who have at least one inactive student. This helps staff contact families regarding inactive enrollments

9. Write a query to list all sessions, showing the session_date, the subject_name taught in that session, the tutor’s first name and last name, and the classroom’s room_name. Order the results by session_date from earliest to latest.
    
<img width="473" height="425" alt="query 9" src="https://github.com/user-attachments/assets/3c7be101-c7d0-44fb-a602-24677562dff2" />

Query 9 lists all tutoring sessions with the date, subject, tutor name, and classroom. It helps employees quickly check scheduling details and past session records.

10. Write a query to list each progress report, showing the student’s first name, last name, and the improvement_level recorded on that report.
    
<img width="470" height="428" alt="query 10" src="https://github.com/user-attachments/assets/4a29974a-38d9-450c-a346-4d4cc591e337" />

Query 10 shows each student’s name along with their recorded improvement level from progress reports. This allows staff to easily track and discuss student progress.




---
