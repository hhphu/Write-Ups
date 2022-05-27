 ## [Day 01] - Save the gifts!

### Objectives
Learn about IDOR vulnerability, how to find and exploit IDOR vulnerabilities.

### [Resources](https://tryhackme.com/room/adventofcyber3)

### Walkthrough
1. After finding Santa's account, what is their position in the company?
When "Your Activity" tab is clicked, it displays default user_id=11. When trying to change the user_id from 1 to 20, Iget all information about Santa, whose user_id=1

![image](./images/d1q1.png)
<details>
  <Summary>Answer</Summary>
  The Boss!
</details>

----------

2. After finding McStocker's account, what is their position int he 
company?
Continue trying user_id from 1 to 20, I get McStocker's account, whose user_id=3

![image](./images/d1q2.png)

<details>
  <Summary>Answer</Summary>
  Build Manager
</details>

----------

3. After finding the account responsible for tampering, what is their position in the company?
Similarly, I get the user_id=9

![image](./images/d1q3.png)

<details>
  <Summary>Answer</Summary>
  Build Manager
  Mischief Manager
</details>


----------

4. What is the received flag when McSkidy fixes the Invetory Management System?
On the Grinch activity page, I notice that there are "Revert" buttons. After reverting everything, I get the flag.

![image](./images/d1q4.png)

<details>
  <Summary>Answer</Summary>
  Build Manager
  THM{AOC_IDOR_2B34BHI3}
</details>



[Day 02 >>](../Day%2002%20-%20Elf%20HR%20Problems/README.md)
