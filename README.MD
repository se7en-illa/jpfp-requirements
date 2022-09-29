# junior phase final project

## BACK END:

<details>
<summary>Tier 1: All Campuses and Students (26/59):</summary>

### *seed*
- [ ] Write a function which sync's and seeds your database when your application starts
### *campus*
- [ ] Write a route to serve up all campuses
**Write a `campuses` model with the following information:**
    - [ ] name - not empty or null
    - [ ] imageUrl - with a default value
    - [ ] address - not empty or null
    - [ ] description - extremely large text
### *students*
- [ ] Write a route to serve up all students
**Write a `students` model with the following information:**
    - [ ] firstName - not empty or null
    - [ ] lastName - not empty or null
    - [ ] email - not empty or null; must be a valid email
    - [ ] imageUrl - with a default value
    - [ ] gpa - decimal between 0.0 and 4.0
- [ ] Students may be associated with at most one campus. 
- [ ] Likewise, campuses may be associated with many students
</details>

<details>
<summary>Tier 2: Single Student and Single Campus (10/59):</summary>

*campus*
- [ ] Write a route to serve up a single campus (based on its id), including that campuses' students
*students*
- [ ] Write a route to serve up a single student (based on their id), including that student's campus
</details>

<details>
<summary>Tier 3: Adding a Campus and Adding a Student (8/59):</summary>
*campus*
- [ ] Write a route to add a new campus
*student*
- [ ] Write a route to add a new student
</details>

<details>
<summary>Tier 4: Removing a Campus and Removing a Student (6/59):</summary>
*campus*
- [ ] Write a route to remove a campus (based on its id)
*student*
- [ ] Write a route to remove a student (based on their id)
</details>

<details>
<summary>Tier 5: Updating a Campus and Updating a Student (9/59):</summary>

*campus*
- [ ] Write a route to update an existing campus
*student*
- [ ] Write a route to update an existing student
</details>

## FRONT END:

<details>
<summary>Tier 1: All Campuses and Students (26/59):</summary>

*campus*
- [ ] Write a component to display a list of all campuses (at least their names and images)
- [ ] Write a campuses sub-reducer to manage campuses in your Redux store
- [ ] Display the all-campuses component when the url matches `/campuses`
*students*
- [ ] Write a component to display a list of all students (at least their names)
- [ ] Write a students sub-reducer to manage students in your Redux store
- [ ] Display the all-students component when the url matches `/students`
*navbar*
- [ ] Add a links to the navbar that can be used to navigate to the all-campuses view and the all-students view
</details>

<details>
<summary>Tier 2: Single Student and Single Campus (10/59):</summary>

*single campus*
**Write a component to display a single campus with the following information:**
   - [ ] The campus's name, image, address and description
   - [ ] A list of the names of all students in that campus (or a helpful message if it doesn't have any students)
   - [ ] Display the appropriate campus's info when the url matches /campuses/:campusId
- [ ] Clicking on a campus from the campuses view should navigate to show that campus
- [ ] Clicking on the name of a student in the campus view should navigate to show that student in the student view
*single student*
**Write a component to display a single student with the following information:**
    - [ ] The student's full name, email, image, and gpa
    - [ ] The name of their campus (or a helpful message if they don't have one)
- [ ] Display the appropriate student when the url matches `/students/:studentId`
- [ ] Clicking on a student from the students view should navigate to show that student
- [ ] Clicking on the name of a campus in the student view should navigate to show that campus in the campus view
</details>

<details>
<summary>Tier 3: Adding a Campus and Adding a Student (8/59):</summary>

*campus*
- [ ] Write a component to display a form for adding a new campus that contains inputs for at least the name and address.
- [ ] Display this component as part of the campuses view, alongside the list of campuses
**Submitting the form with a valid name/address should:**
    - [ ] Make an AJAX request that causes the new campus to be persisted in the database
    - [ ] Add the new campus to the list of campuses without needing to refresh the page
*student*
- [ ] Write a component to display a form for adding a new student that contains inputs for at least first name, last name and email
- [ ] Display this component as part of the students view, alongside the list of students
**Submitting the form with a valid first name/last name/email should:**
    - [ ] Make an AJAX request that causes the new student to be persisted in the database
    - [ ] Add the new student to the list of students without needing to refresh the page
</details>

<details>
<summary>Tier 4: Removing a Campus and Removing a Student (6/59):</summary>

*campus*
- [ ] In the campuses view, include an X button next to each campus
**Clicking the X button should:**
    - [ ] Make an AJAX request that causes that campus to be removed from database
    - [ ] Remove the campus from the list of campuses without needing to refresh the page
*student*
- [ ] In the students view, include an X button next to each student
**Clicking the X button should:**
    - [ ] Make an AJAX request that causes that student to be removed from database
    - [ ] Remove the student from the list of students without needing to refresh the page
</details>

<details>
<summary>Tier 5: Updating a Campus and Updating a Student (9/59):</summary>

**campus**
- [ ] Write a component to display a form updating at least a campus's name and address
- [ ] Display this component as part of the campus view

*Submitting the form with valid data should:*
    - [ ] Make an AJAX request that causes that campus to be updated in the database
    - [ ] Update the campus in the current view without needing to refresh the page

- [ ] In the campus view, display an Unregister button next to each of its students, which removes the student from the campus (in the database as well as this view)
     *hint: the student is still in the database but is no longer associated with the campus*

**student**
- [ ] Write a component to display a form updating a student
- [ ] Display this component as part of the student view

*Submitting the form with valid data should:*
    - [ ] Make an AJAX request that causes that student to be updated in the database
    - [ ] Update the student in the current view without needing to refresh the page
</details>

## EXTRA CREDIT:

<details>
<summary>Finishing Touches:</summary>

- [ ] If a user attempts to add a new student or campus without a required field, a helpful message should be displayed
- [ ] If a user attempts to access a page that doesn't exist (ex. `/potato`), a helpful "not found" message should be displayed
- [ ] If a user attempts to view a student/campus that doesn't exist, a helpful message should be displayed
- [ ] Whenever a component needs to wait for data to load from the server, a "loading" message should be displayed until the data is available
- [ ] Overall, the app is spectacularly styled and visually stunning
</details>


<details>
<summary>Ordering:</summary>

- [ ] Create option for students to be ordered based on lastName on all-students view
- [ ] Create option for students to be ordered based on GPA on all-students view
- [ ] Create option for campuses to be ordered based on number of enrolled students on all-campuses view
</details>

<details>
<summary>Filtering:</summary>

- [ ] Create a filter on all-students view to only show students who are not registered to a campus
- [ ] Create a filter on the all-campuses view to only show campuses that do not have any registered students
</details>


<details>
<summary>Seeding & Pagination:</summary>

- [ ] Seed 100+ students and 100+ campuses
- [ ] Implement _front-end_ pagination for the students view (e.g. `/students?page=1` renders the first ten students, and `/students?page=2` renders students 11-20)
- [ ] Implement _front-end_ pagination for the campuses view (e.g. `/campuses?page=1` renders the first ten campuses, and `/campuses?page=2` renders campuses 11-20)
- [ ] Implement _back-end_ pagination for students (e.g. `/api/students?page=1` returns the first ten students' data, and `/api/students?page=2` returns students 11-20)
- [ ] Implement _back-end_ pagination for campuses (e.g. `/api/campuses?page=1` returns the first ten campuses' data, and `/api/campuses?page=2` returns campuses 11-20)
</details>