# Ex-No-4-Creating-Procedures-using-PL-SQL
## AIM: To create a procedure using PL/SQL.
# Steps:
Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
Create a procedure named as insert_employee data.
Inside the procdure block, write the query for inserting the values into the employee table.
End the procedure.
Call the insert_employee data procedure to insert the values into the employee table.
Display the employee table
# Program:
```
SQL> CREATE TABLE ep(
     empid NUMBER,
     empname VARCHAR(10),
     dept VARCHAR(10),
     salary NUMBER
    );
CREATE OR REPLACE PROCEDURE emp_data AS
    BEGIN
    INSERT INTO ep(empid,empname,dept,salary)
    values(1,'SHAKTHI','MD',10000000);
    values(1,'ABISHEK','MD',10000000);
    INSERT INTO ep(empid,empname,dept,salary)
    values(2,'ARUN','HR',500000);
    values(2,'DEVA','HR',500000);
    INSERT INTO ep(empid,empname,dept,salary)
    values(3,'DHANUSH','IT',200000);
    values(3,'RAGAV','IT',200000);
    COMMIT;
   FOR emp_rec IN (SELECT * FROM ep)LOOP
   DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
   ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
   END LOOP;
   END;
  /
```
# Output:
![image](https://github.com/imthiyas19/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/120353416/939b6f3f-c8f1-4f50-9e38-f1fd6bbdbd00)

Result:
THE PROGRAM HAS BEEN IMPLEMENTED SUCCESSFULLY
