<h1> Applying Filters To SQL Queries </h1>

 
<h2>Project Description</h2>
<i>This scenario is based on a fictional company:</i>
<br>
<br>

My organization is working to make their system more secure. It is my job to ensure the system is safe, investigate all potential security issues, and update employee computers as needed. The following steps provide examples of how I used SQL with filters to perform security-related tasks.

<h2> Retrieve after hours failed login attempts </h2>

A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.

<img src="https://i.ibb.co/TwzB8SD/SQL-Image-1-in-order.png" alt="SQL-Image-1-in-order" border="0">

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an OR operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition is <b>login_date = '2022-05-09',</b> which filters for logins on 2022-05-09. The second condition is <b>login_date = '2022-05-08'</b>, which filters for logins on 2022-05-08.

<h2> Retrieve login attempts on specific dates </h2>

A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.

<img src="https://i.ibb.co/YdtT2KM/SQL-Image-2.png" alt="SQL-Image-2" border="0">

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08. First, I started by selecting all data from the <b>log_in_attempts table</b>. Then, I used a <b>WHERE</b> clause with an <b>OR</b> operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition is <b>login_date = '2022-05-09'</b>, which filters for logins on 2022-05-09. The second condition is <b>login_date = '2022-05-08'</b>, which filters for logins on 2022-05-08.

<h2> Retrieve login attempts outside of Mexico </h2>

After investigating the organization’s data on login attempts, I believe there is an issue with the login attempts that occurred outside of Mexico. These login attempts should be investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico. 

<img src="https://i.ibb.co/YthSLm6/SQL-Image-3.png" alt="SQL-Image-3" border="0">

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred in countries other than Mexico. First, I started by selecting all data from the <b>log_in_attempts</b> table. Then, I used a <b>WHERE</b> clause with NOT to filter for countries other than Mexico. I used <b>LIKE</b> with <b>MEX%</b> as the pattern to match because the dataset represents Mexico as <b>MEX</b> and <b>MEXICO</b>. The percentage sign (%) represents any number of unspecified characters when used with <B>LIKE</B>. 

<h2> Retrieve employees in Marketing </h2>

My team wants to update the computers for certain employees in the Marketing department. To do this, I have to get information on which employee machines to update.

The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Marketing department in the East building.

<img src="https://i.ibb.co/VtFF0MP/SQL-Image-4.png" alt="SQL-Image-4" border="0">

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Marketing department in the East building. First, I started by selecting all data from the <b>employees</b> table. Then, I used a <b>WHERE</b> clause with <b>AND</b> to filter for employees who work in the Marketing department and in the East building. I used <b>LIKE</b> with <b>East%</b> as the pattern to match because the data in the <b>office</b> column represents the East building with the specific office number. The first condition is the <b>department = 'Marketing'</b> portion, which filters for employees in the Marketing department. The second condition is the <b>office LIKE 'East%'</b> portion, which filters for employees in the East building.

<H2> Retrieve employees in Finance or Sales </H2>

The machines for employees in the Finance and Sales departments also need to be updated. Since a different security update is needed, I have to get information on employees only from these two departments.

The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Finance or Sales departments.


<img src="https://i.ibb.co/9rP6qwL/SQL-Image-5.png" alt="SQL-Image-5" border="0">

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Finance and Sales departments. First, I started by selecting all data from the employees table. Then, I used a <b>WHERE</b> clause with <b>OR</b> to filter for employees who are in the Finance and Sales departments. I used the <b>OR</b> operator instead of <b>AND</b> because I want all employees who are in either department. The first condition is <b>department = 'Finance'</b>, which filters for employees from the Finance department. The second condition is <b>department = 'Sales'</b>, which filters for employees from the Sales department.

<H2> Retrieve all employees not in IT </H2>

My team needs to make one more security update on employees who are not in the Information Technology department. To make the update, I first have to get information on these employees.

The following demonstrates how I created a SQL query to filter for employee machines from employees not in the  Information Technology department.

<img src="https://i.ibb.co/713YJC4/SQL-Image-6.png" alt="SQL-Image-6" border="0">

The first part of the screenshot is my query, and the second part is a portion of the output. The query returns all employees not in the Information Technology department. First, I started by selecting all data from the <b>employees</b> table. Then, I used a <b>WHERE</b> clause with <b>NOT</b> to filter for employees not in this department.

<H2>Summary</H2>

I applied filters to SQL queries to get specific information on login attempts and employee machines. I used two different tables, <b>log_in_attempts</b> and <b>employees</b>. I used the <b>AND</b>, <b>OR</b>, and <b>NOT</b> operators to filter for the specific information needed for each task. I also used <b>LIKE and the percentage sign (%) wildcard to filter for patterns.
