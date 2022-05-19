# splitwise
This is an expense sharing application where you can add your expenses and split it among different people. The application keeps balances between people as in who owes how much to whom.

**Below is the functional description of this application:**

- User should be able to enter the expense he paid for friends and the amount should be split amongst friends.
- The Splitting of expense is of the following types:
  - Split Equally: This case should handle the edge cases like recurring decimal digits like 100/3 =33.33333...333 in optimised way
  - Split Unequally:
    - User should be able to add the exact amount pertaining to every expense. The sum total of the amounts entered should match the total amount spent by the user.
    - User should be able to have option for percentage wise splitting. The sum total of the percentages should be equal to 100%.

**Requirements**

- User creation: Each user created should have a userId, name, email and mobile number
- Expense addition: Could either be EQUAL, EXACT or PERCENT. Expense in the format: EXPENSE <user-id-of-person-who-paid> <no-of-users> <space-separated-list-of-users> <EQUAL/EXACT/PERCENT> <space-separated-values-in-case-of-non-equal>
- Show balances for all: SHOW
- Show balances for a single user: SHOW <user-id>
  

**Some of the conditions to consider while designing this application:**
  
- The percent and amount provided could have decimals upto two decimal places.
- In case of percent, you need to verify if the total sum of percentage shares is 100 or not.
- In case of exact, you need to verify if the total sum of shares is equal to the total amount or not.
- The amount should be rounded off to two decimal places. Say if User1 paid 100 and amount is split equally among 3 people. Assign 33.34 to first person and 33.33 to others.
  
  Source: [work@tech](https://workat.tech/)
