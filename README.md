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

| Feature / Query Type      | Query 1 | Query 2 | Query 3 | Query 4 | Query 5 |
|---------------------------|:-------:|:-------:|:-------:|:-------:|:-------:|
| Multiple table join       |    x    |    x    |    x    |    x    |    x    |
| Left join                 |         |    x    |         |    x    |         |
| Inner join                |    x    |         |    x    |         |    x    |
| Group By / Aggregation    |    x    |    x    |    x    |    x    |    x    |
| Subquery                  |         |         |    x    |         |         |
| CASE logic                |         |         |         |    x    |         |

1. Using an inner join between the student, guardian, and payment tables, produce a report of active students and their guardians that shows each student’s maximum payment amount, but only for students who have made at least one payment greater than 200, ordered from highest to lowest maximum payment.
atus is 'Active' and who have made at least one payment greater than 200. Group the results by student and guardian, and sort the results from the highest payment to the lowest.

<img width="263" height="299" alt="MIST 4610 query 1" src="https://github.com/user-attachments/assets/018e6633-d293-4d17-9cb7-b9670280fc37" />
<img width="551" height="313" alt="MIST 4610 query 1 answers" src="https://github.com/user-attachments/assets/b2eb27a9-1617-4c6c-b2da-994585add27b" />

Query 1 helps staff see which active students have made large payments (over 200). It lists the student and guardian names along with each student’s highest payment so employees can quickly focus on top-paying families.

2. Using a left outer join from guardians to their students and payments, create a monthly billing summary that shows, for each guardian and each calendar month, the total amount paid for all of their students. Group by the year and month of the payment date so you can see separate rows per month, and include guardians even if they have no payments. Order the result by guardian and then by year and month.

<img width="341" height="416" alt="MIST 4610 query 2" src="https://github.com/user-attachments/assets/f8219d8f-d6b4-40d0-a6b6-a8ac6c1a1f4d" />
<img width="548" height="309" alt="MIST 4610 query 2 answers" src="https://github.com/user-attachments/assets/42a42eb4-2a8a-4a8c-aa03-8a43cc970bed" />

Query 2 summarizes how much each guardian pays per month across all of their students. This makes it easy for the office to review monthly revenue by family, spot unusually high or low months, and follow up on billing trends.

3. Using an inner join between the tutor and session tables, list all tutors whose hourly rate is higher than the average hourly rate for their specialty and who have taught at least 2 sessions. For each tutor, show their name, specialty, hourly rate, and the total number of sessions they have taught. Order the results by specialty and then by hourly rate in descending order.

<img width="356" height="412" alt="MIST 4610 query 3" src="https://github.com/user-attachments/assets/6bad3edc-e2f7-49e1-84ae-da6ac046ae38" />
<img width="542" height="311" alt="MIST 4610 query 3 answers" src="https://github.com/user-attachments/assets/aec2b58f-f32c-457f-ac33-599f4cccbf85" />

Query 3 identifies tutors who charge more than the average rate for their specialty and who also teach many sessions. This helps management recognize top-earning, in-demand tutors and decide how to allocate popular instructors.

4. Using a left outer join between guardians, their students, and payments, create a spending summary that shows how much each guardian has paid in total for all of their students. Classify each guardian’s total spending with a CASE expression (for example, “Low”, “Medium”, “High”). Order the results by total spending from highest to lowest.

<img width="481" height="402" alt="MIST 4610 query 4" src="https://github.com/user-attachments/assets/ea3989ae-c15d-4e11-8a29-daed5ec93c1d" />
<img width="545" height="312" alt="MIST 4610 query 4 answers" src="https://github.com/user-attachments/assets/989eaddc-98de-4d8c-b729-92275b77c795" />

Query 4 shows how much each guardian has paid in total and classifies them into spending levels (such as Low, Medium, or High). This lets the center quickly see which families are light users versus heavy users and tailor communication or promotions accordingly.

5. Create a report that lists each student who has made at least one payment. For each student, show the student’s first name, last name, their guardian’s first and last name, and the total amount the student has paid. Sort the results by total amount paid in descending order.

<img width="392" height="361" alt="MIST 4610 query 5" src="https://github.com/user-attachments/assets/0c14aa4f-dbc9-43f4-ab7f-a69a295e9992" />
<img width="541" height="310" alt="MIST 4610 query 5 answers" src="https://github.com/user-attachments/assets/19647cab-12ab-410c-8997-9674a93cb670" />

Query 5 shows how much each student has paid in total and pairs that with the guardian’s name. This helps staff quickly see which students generate the most revenue, review family payment histories, and prioritize follow-up with high- or low-paying accounts.

---
## Visualizations
<img width="1285" height="650" alt="dashboard_screenshot" src="https://github.com/user-attachments/assets/37c42a62-876e-4e97-a148-e48e0db00cf5" />

<img width="740" height="639" alt="visualization1" src="https://github.com/user-attachments/assets/95584880-1be0-417f-8a3c-734f708f7306" />

### Total Revenue by Plan Type

- Purpose: This chart shows the total revenue generated by each tutoring plan, to show which plans bring in the highest financial contribution to the tutoring center.
  
- Relevance: Helps management identify which plans bring in the most revenue and also helps them decide where to focus pricing and refine marketing strategies. 

<img width="787" height="725" alt="visualization2" src="https://github.com/user-attachments/assets/19bd7703-5ed6-4649-a38e-807d790c1eee" />

### Tutors by Subject Specialty

- Purpose: This visualization displays how tutors are distributed across different subjects, and the number of instructors available in each speciality.
  
- Relevance: Helps management see overview of staffing within the center. Also reveals staffing balance across different subjects, which helps management determine hiring needs and ensure adequate coverage for high-demand areas. 

<img width="787" height="665" alt="visualization3" src="https://github.com/user-attachments/assets/8294f161-120f-4d34-bd34-7c1dff36da83" />

### Student Improvement Rate by Plan

- Purpose: This chart shows the percentage of students demonstrating significant or moderate academic improvement within each tutoring plan.
  
- Relevance: Helps management evaluate which plans are the most effective, which then they can further make adjustments to their curriculum and recommendations for families seeking better academic outcomes. 

