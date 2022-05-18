# splitwise
This is an expense sharing application where you can add your expenses and split it among different people. The application keeps balances between people as in who owes how much to whom.

Below is the functional description of this application:

Let's say you live with 3 other friends.

You: User1 (id: u1)
Other friends: User2 (u2), User3 (u3), User4 (u4)

This month's electricity bill was Rs. 1000. Now you can just go to the app and add that you paid 1000 by selecting all the 4 people and then select split equally.

Input: u1 1000 4 u1 u2 u3 u4 EQUAL

For this transaction, everyone owes 250 to User1. The app should update the balances in each of the profiles accordingly.
User2 owes User1: 250 (0+250)
User3 owes User1: 250 (0+250)
User4 owes User1: 250 (0+250)

Now, It is the sale on e-commerce application and there is an offer on your card. You buy a few stuffs for User2 and User3 as they asked you to. The total amount for each person is different.

Input: u1 1250 2 u2 u3 EXACT 370 880

For this transaction, User2 owes 370 to User1 and User3 owes 880 to User1. The app should update the balances in each of the profiles accordingly.

User2 owes User1: 620 (250+370)
User3 owes User1: 1130 (250+880)
User4 owes User1: 250 (250+0)


Now, you go out with your flatmates and take your brother/sister along with you. User4 pays and everyone splits equally. You owe for 2 people.

Input: u4 1200 4 u1 u2 u3 u4 PERCENT 40 20 20 20

For this transaction, User1 owes 480 to User4, User2 owes 240 to User4 and User3 owes 240 to User4. The app should update the balances in each of the profiles accordingly.

User1 owes User4: 230 (250-480)
User2 owes User1: 620 (620+0)
User2 owes User4: 240 (0+240)
User3 owes User1: 1130 (1130+0)
User3 owes User4: 240 (0+240)

**Requirements**

1. User creation: Each user should have a userId, name, email and mobile number
2. Expense addition: Could either be EQUAL, EXACT or PERCENT. Expense in the format: EXPENSE <user-id-of-person-who-paid> <no-of-users> <space-separated-list-of-users> <EQUAL/EXACT/PERCENT> <space-separated-values-in-case-of-non-equal>
3. Show balances for all: SHOW
4. Show balances for a single user: SHOW <user-id>
  

Some of the conditions to consider while designing this application:
  
1. The percent and amount provided could have decimals upto two decimal places.
2. In case of percent, you need to verify if the total sum of percentage shares is 100 or not.
3. In case of exact, you need to verify if the total sum of shares is equal to the total amount or not.
4. The amount should be rounded off to two decimal places. Say if User1 paid 100 and amount is split equally among 3 people. Assign 33.34 to first person and 33.33 to others.
  
  Source: [work@tech](https://workat.tech/)
